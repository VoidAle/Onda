<p align="center"><img src="assets/onda.png" width="96" alt="Onda"></p>
<h1 align="center">Onda</h1>
<p align="center">Un lettore musicale minimale e fluido, senza account. Per Windows, macOS e Linux.</p>
<p align="center">
  <a href="https://github.com/VoidAle/Onda/releases/latest/download/Onda-Setup.exe"><b>Scarica per Windows</b></a> ·
  <a href="https://github.com/VoidAle/Onda/releases/latest/download/Onda-macOS.dmg"><b>macOS</b></a> ·
  <a href="#linux"><b>Linux</b></a> ·
  <a href="https://github.com/VoidAle/Onda/releases/latest">Novità</a> ·
  <a href="https://discord.gg/SE4Q9gt3j">Segnala un bug</a>
</p>

---

Onda cerca e riproduce musica dal catalogo di YouTube Music e da SoundCloud, insieme ai tuoi file audio. Playlist, preferiti e statistiche restano sul tuo computer: niente account, niente pubblicità, niente registrazione.

Dalla **0.6.0** Onda è stata riscritta da zero: è più leggera, si apre prima, fa partire i brani più in fretta e funziona anche su macOS e Linux.

| Sistema | File | Stato |
| --- | --- | --- |
| Windows 10 e 11 (64 bit) | [Onda-Setup.exe](https://github.com/VoidAle/Onda/releases/latest/download/Onda-Setup.exe) | Stabile |
| macOS 10.15 o successivo (Apple Silicon e Intel) | [Onda-macOS.dmg](https://github.com/VoidAle/Onda/releases/latest/download/Onda-macOS.dmg) | Sperimentale |
| Linux 64 bit (Ubuntu 22.04+, Debian 12+, Fedora…) | [.deb](https://github.com/VoidAle/Onda/releases/latest/download/Onda-Linux.deb) · [.rpm](https://github.com/VoidAle/Onda/releases/latest/download/Onda-Linux.rpm) · [AppImage](https://github.com/VoidAle/Onda/releases/latest/download/Onda-Linux.AppImage) | Sperimentale |

**Sperimentale** significa che la versione per quel sistema viene compilata e avviata in automatico a ogni release, ma non è ancora stata usata a lungo su computer veri. Se qualcosa non va, [scrivimi su Discord](#segnalare-un-bug): mi aiuti a renderla stabile.

Serve sempre una connessione Internet, tranne per i brani scaricati e per i tuoi file.

## Windows

1. Scarica **[Onda-Setup.exe](https://github.com/VoidAle/Onda/releases/latest/download/Onda-Setup.exe)** e aprilo.
2. Segui la procedura. Onda si installa solo per il tuo utente, senza permessi di amministratore, e compare nel menu Start e sul Desktop.
3. Per disinstallarla: *Impostazioni → App → App installate → Onda → Disinstalla*.

**Se avevi Onda 0.2.x:** installa la 0.6.0 come una versione nuova. L'installazione rimuove da sola la vecchia Onda, così non ne restano due. Al primo avvio la nuova Onda importa playlist, preferiti, recenti, tagli dei brani, cronologia d'ascolto e brani scaricati. I dati della versione precedente in `%LOCALAPPDATA%\OndaPlayer` non vengono modificati né cancellati. La vecchia Onda non propone questo aggiornamento da sola: va scaricato una volta da qui.

### Windows blocca il file?

Onda non è firmata digitalmente, perché la firma richiede un certificato a pagamento. Per questo Windows può chiedere una conferma.

- **«Windows ha protetto il PC» (SmartScreen):** scegli *Ulteriori informazioni → Esegui comunque*.
- **«Un criterio di controllo delle applicazioni ha bloccato questo file»:** prima di aprirlo fai tasto destro su **Onda-Setup.exe** → *Proprietà* → spunta **Sblocca** → *OK*. In alternativa, da PowerShell nella cartella del download: `Unblock-File .\Onda-Setup.exe`.
- **Smart App Control attivo:** può bloccare comunque i programmi non firmati. L'unica via è disattivarlo in *Sicurezza di Windows → Controllo app e browser → Smart App Control*.

## macOS

> Versione sperimentale.

1. Scarica **[Onda-macOS.dmg](https://github.com/VoidAle/Onda/releases/latest/download/Onda-macOS.dmg)**, aprilo e trascina **Onda** nella cartella **Applicazioni**.
2. Apri Onda dalla cartella Applicazioni. Al primo avvio macOS dice che non può verificare lo sviluppatore, perché Onda non è registrata presso Apple (serve un abbonamento a pagamento). Per aprirla:
   - **macOS 15 Sequoia o successivo:** chiudi l'avviso, poi vai in *Impostazioni di Sistema → Privacy e sicurezza*, scorri in basso e premi **Apri comunque** accanto a Onda. Conferma con la password.
   - **macOS 14 o precedente:** tasto destro (o Ctrl+clic) su Onda → **Apri** → **Apri**.
3. Basta farlo la prima volta.

Se compare **«Onda è danneggiata e non può essere aperta»**, apri il Terminale ed esegui:

```sh
xattr -dr com.apple.quarantine /Applications/Onda.app
```

Il comando toglie solo il contrassegno «scaricato da Internet»; poi Onda si apre normalmente. Per disinstallarla, trascina Onda dalla cartella Applicazioni nel Cestino.

## Linux

> Versione sperimentale. Serve un sistema a 64 bit (x86_64) con WebKitGTK 4.1: Ubuntu 22.04 o successivo, Debian 12 o successivo, Linux Mint 21 o successivo, Fedora e derivate.

**Ubuntu, Debian, Linux Mint** — scarica [Onda-Linux.deb](https://github.com/VoidAle/Onda/releases/latest/download/Onda-Linux.deb), poi nella cartella del download:

```sh
sudo apt install ./Onda-Linux.deb
```

**Fedora** — scarica [Onda-Linux.rpm](https://github.com/VoidAle/Onda/releases/latest/download/Onda-Linux.rpm), poi:

```sh
sudo dnf install ./Onda-Linux.rpm
```

**Qualsiasi distribuzione (AppImage, senza installazione)** — scarica [Onda-Linux.AppImage](https://github.com/VoidAle/Onda/releases/latest/download/Onda-Linux.AppImage), poi:

```sh
chmod +x Onda-Linux.AppImage
./Onda-Linux.AppImage
```

Se l'AppImage non parte e cita FUSE, installa `libfuse2` (su Ubuntu 24.04: `sudo apt install libfuse2t64`).

Con .deb e .rpm Onda compare nel menu delle applicazioni. Per disinstallarla: `sudo apt remove onda` oppure `sudo dnf remove onda`. L'icona nell'area di notifica dipende dall'ambiente desktop: su GNOME serve l'estensione *AppIndicator*.

## Aggiornare

Onda 0.6 non si aggiorna ancora da sola. Quando esce una versione nuova, la trovi nella pagina [Novità](https://github.com/VoidAle/Onda/releases/latest) e nel [server Discord](https://discord.gg/SE4Q9gt3j). Scarica il file per il tuo sistema e installalo sopra quello che hai: playlist, preferiti e impostazioni restano al loro posto.

## Cosa fa

- **Cerca** brani, artisti e album nel catalogo di YouTube Music mentre scrivi, e brani su SoundCloud. Le pagine di artisti e album mostrano brani, uscite e artisti simili.
- **Incolla un link** nella ricerca: un brano, un album o una playlist di YouTube o YouTube Music, un brano o un set di SoundCloud, una playlist, un album o un brano di Spotify. Onda lo apre: puoi riprodurlo subito o salvarlo come playlist.
- **Ascolta** con coda, *Riproduci dopo*, casuale, ripetizione e autoplay. Quando la musica finisce, Onda continua con brani simili. Da ogni brano può partire una radio.
- **Vista di ascolto** a tutta finestra, con copertina grande e testo sincronizzato quando disponibile. Un clic su una riga porta la canzone a quel punto.
- **Per te**: al primo avvio un breve questionario (lingua, tema, generi, artisti e brani preferiti) crea la playlist *Per te*. La Home propone brani e artisti da scoprire. Puoi chiedere di non consigliare più un brano o un artista.
- **Playlist**: crea, riordina trascinando, cerca all'interno, seleziona più brani insieme, rimuovi i duplicati, scegli una copertina. Puoi condividerle come file `.onda`.
- **Importa** playlist da link di YouTube, YouTube Music, SoundCloud e Spotify (pubbliche, senza account), o da file `.onda`, CSV (anche da Exportify), TXT con righe `Artista - Titolo`, XML (iTunes/XSPF) e M3U. I brani non trovati vengono elencati.
- **Ascolto offline**: scarica brani o intere playlist e riproducili senza Internet.
- **I miei brani**: aggiungi i tuoi file audio (MP3, M4A, AAC, FLAC, WAV, OGG, OPUS, WEBM) con *Carica brani* o trascinandoli sulla finestra. Vengono copiati in Onda; gli originali non si toccano.
- **Taglia inizio e fine** di qualsiasi brano dal menu **⋯**, per saltare i silenzi lunghi. Il file non viene modificato.
- **Mini-player** sempre in primo piano, con il testo che scorre (Ctrl+M, scorciatoia modificabile).
- **In sottofondo**: icona nell'area di notifica con i comandi, musica che continua quando chiudi la finestra, avvio all'accesso al computer, se lo vuoi.
- **Wrapped**: minuti ascoltati, brani e artisti più ascoltati per mese, anno o da sempre, con un'immagine verticale da condividere.
- **Preferiti** e **Recenti**, timer di spegnimento, dissolvenza a inizio e fine brano, controlli multimediali della tastiera e di sistema, attività su Discord (disattivabile).
- **Temi** Scuro, Chiaro, Nero (per schermi OLED) e Notte; opzione *Riduci animazioni*. Interfaccia in italiano e inglese (alcuni testi restano in italiano).
- **Backup e ripristino** di libreria, statistiche e impostazioni in una cartella, da *Impostazioni → Dati*.

### Ancora da portare dalla versione 0.2

Queste funzioni della vecchia Onda non sono ancora nella 0.6.0: aggiornamento automatico, link `onda://` e codici di condivisione, tavolozza comandi (Ctrl+K), video nella vista di ascolto, *Trova da un file*, *Esporta file*, import diretto da Apple Music (il file XML esportato funziona) e i temi colorati. Arriveranno nelle prossime versioni.

## Privacy

- Nessun account Onda e nessuna registrazione. Nessuna statistica d'uso inviata.
- Playlist, preferiti, cronologia, statistiche e impostazioni restano sul tuo computer, nella cartella dati di Onda:
  - Windows: `%LOCALAPPDATA%\app.onda.player`
  - macOS: `~/Library/Application Support/app.onda.player`
  - Linux: `~/.local/share/app.onda.player`
- Ricerche, riproduzione e testi vengono chiesti ai rispettivi servizi esterni (YouTube Music, SoundCloud, LRCLIB). I link Spotify che importi vengono letti dalla pagina pubblica di Spotify. Onda non invia altro.
- I file che aggiungi in *I miei brani* restano sul tuo computer. Per la radio da un tuo brano Onda usa solo titolo e artista.
- Il *rapporto errori* (*Impostazioni*) raccoglie gli ultimi errori della sessione e si copia negli appunti. Non viene inviato da nessuna parte: controllalo prima di condividerlo.

## Segnalare un bug

Scrivimi sul [server Discord](https://discord.gg/SE4Q9gt3j) o in privato (ID `1007318097985798144`). Indica:

- la versione di Onda (*Impostazioni → Informazioni*) e il sistema operativo;
- i passaggi per riprodurre il problema e cosa ti aspettavi;
- il titolo, l'artista o il link del brano, se riguarda riproduzione o testi;
- il rapporto errori e uno screenshot, se utili, senza dati personali.

## Limiti

Catalogo, riproduzione e testi dipendono da servizi esterni: la disponibilità può cambiare e non tutti i brani hanno un testo sincronizzato. Su SoundCloud alcune etichette offrono solo anteprime di 30 secondi. Sono possibili bug e rallentamenti di rete.

Per verificare un download, confronta il suo SHA256 con il file `SHA256SUMS.txt` della release.

Questo repository distribuisce **il programma e la documentazione**: il codice sorgente non è pubblicato. Onda include [yt-dlp](https://github.com/yt-dlp/yt-dlp) (licenza Unlicense); gli altri componenti di terze parti conservano le proprie licenze.

---

## English

**Onda** is a minimal, fluid music player for **Windows, macOS and Linux**, with no account. It plays the YouTube Music catalogue, SoundCloud and your own audio files. Version 0.6.0 is a full rewrite: lighter, faster to open and quicker to start playback.

**Download:** [Windows (Onda-Setup.exe)](https://github.com/VoidAle/Onda/releases/latest/download/Onda-Setup.exe) · [macOS (Onda-macOS.dmg)](https://github.com/VoidAle/Onda/releases/latest/download/Onda-macOS.dmg) · Linux [.deb](https://github.com/VoidAle/Onda/releases/latest/download/Onda-Linux.deb) / [.rpm](https://github.com/VoidAle/Onda/releases/latest/download/Onda-Linux.rpm) / [AppImage](https://github.com/VoidAle/Onda/releases/latest/download/Onda-Linux.AppImage). The macOS and Linux builds are **experimental**: they are built and launched automatically for each release, but have not yet seen much real-world use.

- **Windows 10/11 (64-bit):** run Onda-Setup.exe. It installs for your user only (no admin rights). If you had Onda 0.2.x, the installer removes it and the new Onda imports your playlists, favorites, history, trims and downloads on first launch; the old data in `%LOCALAPPDATA%\OndaPlayer` is left untouched. Onda is not code-signed: on SmartScreen choose *More info → Run anyway*; if an app control policy blocks it, right-click the file → *Properties* → *Unblock* before opening.
- **macOS 10.15+ (Apple Silicon and Intel):** drag Onda to Applications. Onda is not notarized: on macOS 15+ open it once, then go to *System Settings → Privacy & Security → Open Anyway*; on older versions right-click → *Open*. If macOS says the app is damaged, run `xattr -dr com.apple.quarantine /Applications/Onda.app`.
- **Linux x86_64 with WebKitGTK 4.1** (Ubuntu 22.04+, Debian 12+, Fedora): `sudo apt install ./Onda-Linux.deb`, `sudo dnf install ./Onda-Linux.rpm`, or make the AppImage executable and run it (needs `libfuse2`).

**Updates:** Onda 0.6 does not update itself yet. Download the new version from the [releases page](https://github.com/VoidAle/Onda/releases/latest) and install it over the old one; your data stays.

**Features:** live search of YouTube Music and SoundCloud, paste a YouTube/SoundCloud/Spotify link to open it, queue, shuffle, repeat, autoplay and radio, full-window listening view with synced lyrics, a first-run taste quiz that builds a *For you* playlist, playlists with drag-and-drop reordering, multi-select, de-duplication, custom covers and `.onda` file sharing, playlist import from links and CSV/TXT/XML/M3U files, offline downloads, your own audio files, per-track start/end trimming, a floating mini player with lyrics (Ctrl+M), tray icon and background playback, Wrapped listening stats with a shareable image, sleep timer, fades, media keys, optional Discord activity, four themes and an Italian/English interface.

**Privacy:** no account, no telemetry. Your library and settings stay on your computer. Searches, playback and lyrics go only to the respective services (YouTube Music, SoundCloud, LRCLIB).

**Bugs:** report them on [Discord](https://discord.gg/SE4Q9gt3j) with the Onda version, your operating system, the steps to reproduce and the affected song or link.

This is a binary-only release: the source code is not published in this repository. Onda bundles [yt-dlp](https://github.com/yt-dlp/yt-dlp) (Unlicense); other third-party components keep their own licenses.
