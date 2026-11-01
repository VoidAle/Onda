<p align="center"><img src="assets/onda.png" width="96" alt="Onda"></p>
<h1 align="center">Onda</h1>
<p align="center">Un lettore musicale per Windows: minimale, fluido e senza account.</p>
<p align="center">
  <a href="https://github.com/VoidAle/Onda/releases/download/v0.1.0-beta.8/Onda-0.1.0-beta.8-windows-x64-final.zip"><b>Scarica Onda 0.1.0-beta.8</b></a> ·
  <a href="https://github.com/VoidAle/Onda/releases/tag/v0.1.0-beta.8">Novità</a> ·
  <a href="https://discord.gg/SE4Q9gt3j">Segnala un bug</a>
</p>

---

## Installazione

1. Scarica **Onda-0.1.0-beta.8-windows-x64-final.zip** dalla [pagina della release](https://github.com/VoidAle/Onda/releases/tag/v0.1.0-beta.8).
2. Estrai lo ZIP in una cartella a tua scelta.
3. Avvia **Onda.exe**. Non serve installare Python, Node.js o altro.

Se ti basta il programma, nella stessa pagina trovi anche **Onda.exe** da solo, senza licenze e checksum.

**Requisiti:** Windows 10 o 11 a 64 bit e una connessione Internet. La beta non è firmata digitalmente, quindi Windows può mostrare un avviso di SmartScreen: scegli *Ulteriori informazioni → Esegui comunque*.

**Aggiornare:** chiudi Onda, estrai la nuova versione e sostituisci `Onda.exe`. Playlist, preferiti e impostazioni restano al loro posto. L'app controlla da sola le nuove versioni (si può disattivare in *Impostazioni → Aggiornamenti*).

## Cosa fa

- **Cerca** brani, artisti, album e playlist nel catalogo YouTube Music, anche mentre scrivi.
- **Ascolta** con coda, casuale, ripetizione e suggerimenti simili che continuano la musica quando finisce la playlist.
- **Vista di ascolto** con copertina grande, testo sincronizzato quando disponibile e videoclip facoltativo.
- **Playlist locali**: crea, riordina trascinando, cerca all'interno, rimuovi i duplicati, scegli un'immagine, condividi con un codice o un file `.onda`.
- **Importa** playlist da YouTube Music, Spotify, Apple Music e file CSV, TXT o XML.
- **Ascolto offline**: scarica brani o intere playlist e riproducili senza Internet.
- **Wrapped**: i minuti realmente ascoltati e le classifiche di brani, artisti e album, per mese, anno o da sempre.
- **Preferiti** e **Recenti**, timer di spegnimento, controlli multimediali di Windows e attività su Discord (disattivabile).
- **Temi**: Chiaro, Scuro, Oceano, Aurora, Foresta, Tramonto, Rosa, Lilla, Avana, Sabbia e uno personale con il colore che scegli. Interfaccia in italiano e inglese.

Per riprodurre un brano clicca sulla sua copertina; il resto della riga lo seleziona. Il menu **⋯** raccoglie le altre azioni. Con *Riduci le animazioni* (Impostazioni → Aspetto) ogni movimento viene disattivato.

## Importare una playlist

Apri **Playlist → Importa playlist**. Puoi provare con il [CSV di esempio](examples/playlist.csv).

| Origine | Come fare |
| --- | --- |
| YouTube / YouTube Music | Incolla il link di una playlist pubblica o non in elenco e premi **Apri link**. |
| Spotify e altri servizi | Scegli un file CSV esportato, con le colonne `Track Name` e `Artist Name(s)` oppure `Titolo` e `Artista`. La durata è facoltativa. |
| Apple Music / iTunes | Scegli una playlist esportata in XML o TXT con titoli e artisti. |
| Testo semplice | Un file TXT con una riga `Artista - Titolo` per ogni brano. |

Onda cerca ogni titolo su YouTube Music e mostra le corrispondenze: quelle dubbie restano deselezionate e puoi controllarle a mano, mentre i brani non trovati compaiono nel riepilogo. Premendo **Importa** nasce una nuova playlist locale; la playlist di partenza e le tue playlist esistenti non vengono toccate.

I link di Spotify e Apple Music non si importano direttamente, perché servirebbe il collegamento autorizzato ai tuoi account: usa il file esportato. Nessun audio viene scaricato da quei servizi, vengono lette solo le informazioni dei brani. Sono supportati file fino a 10 MB e playlist fino a 5.000 brani.

## Privacy

- Nessun account Onda e nessuna registrazione.
- Playlist, preferiti, cronologia, statistiche e impostazioni restano sul tuo computer, in `%LOCALAPPDATA%\OndaPlayer`.
- Ricerche, riproduzione e testi sono richieste ai rispettivi servizi esterni (YouTube Music, LRCLIB). Onda non invia altro.
- *Impostazioni → Assistenza → Esporta rapporto errori* crea uno ZIP in locale, con versione, sistema e log recenti, senza dati della tua libreria. Non viene inviato da nessuna parte: controllalo prima di condividerlo.

## Segnalare un bug

Scrivimi sul [server Discord](https://discord.gg/SE4Q9gt3j) o in privato (ID `1007318097985798144`), anche da *Impostazioni → Segnala un bug su Discord*. Indica:

- la versione di Onda e di Windows;
- i passaggi per riprodurre il problema e cosa ti aspettavi;
- il titolo, l'artista o il link del brano, se riguarda riproduzione o testi;
- uno screenshot, se utile, senza dati personali.

## Limiti della beta

Catalogo, riproduzione e testi dipendono da servizi esterni: la disponibilità può cambiare e non tutti i brani hanno un testo sincronizzato. Onda non inventa i tempi mancanti. Sono possibili bug e rallentamenti di rete.

Questo repository distribuisce **il programma e la documentazione**: il codice sorgente non è pubblicato. I componenti di terze parti conservano le proprie licenze, incluse nello ZIP.

---

## English

**Onda** is a minimal, fluid Windows music player with no account required. It is currently in beta.

**Install:** download **Onda-0.1.0-beta.8-windows-x64-final.zip** from the [release page](https://github.com/VoidAle/Onda/releases/tag/v0.1.0-beta.8), extract it and run **Onda.exe**. The standalone **Onda.exe** is also attached to the release. Windows 10/11 (64-bit) and an Internet connection are required; no Python or Node.js needed. The beta is not code-signed, so SmartScreen may ask for confirmation (*More info → Run anyway*). To update, close Onda and replace `Onda.exe`: your data stays in `%LOCALAPPDATA%\OndaPlayer`.

**Features:** search the YouTube Music catalogue, queue and autoplay, an immersive listening view with synced lyrics and optional video, local playlists (reorder, search, de-duplicate, share with a code or a `.onda` file), playlist import from YouTube Music, Spotify, Apple Music and CSV/TXT/XML files, offline downloads, Wrapped listening statistics, favorites and history, sleep timer, Windows media controls, optional Discord activity, eleven themes and an Italian/English interface (*Settings → Language*). *Reduce animations* turns off all motion.

**Privacy:** no account, no telemetry. Library and settings stay on your computer. Searches, playback and lyrics go to the respective third-party services only.

**Bugs:** report them on [Discord](https://discord.gg/SE4Q9gt3j) with the app version, Windows version, reproduction steps and the affected song or link.

This is a binary-only release: the source code is not published in this repository. Third-party components keep their own licenses, included in the ZIP.
