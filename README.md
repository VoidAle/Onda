<p align="center"><img src="assets/onda.png" width="88" alt="Onda"></p>
<h1 align="center">Onda · Windows beta</h1>
<p align="center">Un lettore musicale minimale, con playlist, testi e controlli Windows.</p>
<p align="center"><a href="https://github.com/VoidAle/Onda/releases/tag/v0.1.0-beta.7">Scarica la beta</a> · <a href="[https://discord.gg/yAZKCjnS8]">Segnala un bug su Discord</a></p>

## Installazione

1. Apri la [release 0.1.0-beta.7](https://github.com/VoidAle/Onda/releases/tag/v0.1.0-beta.7).
2. Scarica **Onda-0.1.0-beta.7-windows-x64-final.zip** ed estrai il contenuto.
3. Avvia **Onda.exe**. Non serve installare Python o Node.js.

Richiede Windows 10/11 a 64 bit e una connessione Internet. La beta non e firmata digitalmente.
Il pacchetto contiene le licenze dei componenti di terze parti e il file SHA256SUMS.txt.

## Cosa puoi fare

- Cercare brani, artisti, album e playlist nel catalogo YouTube Music.
- Aprire il profilo di un artista e sfogliare le uscite, con copertine e scorrimento animato.
- Creare playlist locali, scegliere il casuale, gestire la coda e continuare con suggerimenti.
- Salvare i **Preferiti** con il cuore o dal menu **⋯** di un brano.
- Riaprire **Recenti**, la cronologia dei brani realmente avviati.
- Aprire la vista di ascolto con copertina e testo sincronizzato quando disponibile.
- Impostare il **timer di spegnimento** dal simbolo orologio o da Impostazioni: allo scadere la musica va in pausa.
- Scegliere tema chiaro/scuro, Italiano/English, dimensione del testo e movimento ridotto.
- Usare i controlli multimediali di Windows.

Per riprodurre un brano clicca sulla sua copertina. Il resto della riga seleziona il brano.
Il casuale si attiva prima del Play; il menu **⋯** raccoglie le altre azioni.

## Importare playlist

Apri **Playlist → Importa playlist**. Puoi provare anche il [CSV di esempio](examples/playlist.csv).

- **YouTube / YouTube Music:** incolla il link di una playlist pubblica o non in elenco e premi **Apri link**.
- **Spotify e altri servizi:** scegli un file CSV esportato, con colonne `Track Name` e `Artist Name(s)` oppure `Titolo` e `Artista`. La durata e facoltativa; `Duration (ms)` e riconosciuta.
- **Apple Music / iTunes:** scegli una playlist esportata in XML o TXT con titoli e artisti.
- **TXT semplice:** una riga `Artista - Titolo` per ogni brano.

Onda cerca i titoli su YouTube Music e mostra le corrispondenze. Le versioni dubbie sono deselezionate;
puoi verificarle e selezionarle manualmente. I brani non trovati restano nel riepilogo.
Scegli un nome e premi **Importa**: viene creata una nuova playlist locale, mantenendo ordine e duplicati selezionati.
La playlist originale e le playlist Onda esistenti non vengono modificate. Puoi annullare prima di salvare.

**Limite attuale:** i link Spotify e Apple Music non vengono importati direttamente; servono i file esportati.
Il collegamento autorizzato a questi account non e ancora disponibile. Nessun audio Spotify/Apple Music viene scaricato:
la funzione importa l'elenco dei brani e trova corrispondenze nel catalogo di Onda.
Sono supportati file fino a 10 MB e playlist fino a 5.000 voci leggibili.

## Segnalare un bug

Scrivimi su **[Discord](https://discord.com/users/1007318097985798144)** (ID: `1007318097985798144`).
Il collegamento apre il profilo: la possibilita di inviare messaggi dipende dalle impostazioni di Discord.
Puoi aprirlo anche da **Impostazioni → Segnala un bug su Discord**.

Per aiutarmi a riprodurre il problema, indica:

- versione di Onda e versione di Windows;
- passaggi eseguiti e comportamento atteso;
- titolo/artista o link del brano, se riguarda la riproduzione o i testi;
- uno screenshot, se utile, evitando dati personali.

## Correzioni nella beta 0.1.0-beta.5

Il cambio brano invalida i testi precedenti anche durante le animazioni. Il testo segue subito gli spostamenti nella barra temporale, avanti e indietro.

## Stato della beta

Sono possibili bug e ritardi di rete. Catalogo, riproduzione e testi dipendono da servizi esterni:
la disponibilita puo cambiare e alcuni testi non hanno timestamp. Onda preferisce testi sincronizzati
compatibili con la versione del brano, senza inventare i tempi mancanti.

Non e richiesto un account Onda. Playlist, preferiti, cronologia e impostazioni sono salvati
localmente in `%LOCALAPPDATA%\OndaPlayer`. Il pacchetto distribuito non contiene librerie personali.
Le ricerche e le richieste di riproduzione/testi vengono inviate ai rispettivi servizi esterni.

Questo repository distribuisce **il programma e la documentazione**; il codice sorgente di Onda non e pubblicato.
I componenti di terze parti conservano le proprie licenze, incluse nel pacchetto.

## English

Onda is a minimal Windows music player, currently in beta. Download the ZIP from
[Releases](https://github.com/VoidAle/Onda/releases/tag/v0.1.0-beta.7), extract it, and run **Onda.exe**.
Windows 10/11 x64 and an Internet connection are required. No Python or Node.js installation is needed.

Features include artist profiles, albums, local playlists, favorites, listening history, a sleep timer,
lyrics when available, album artwork, Windows media controls, light/dark themes and an English interface.
Change the language in **Settings → Language**.

Report bugs via **[Discord]([https://discord.gg/yAZKCjnS8])** and include the app version,
Windows version, reproduction steps, and the affected song/link. Messaging availability depends on Discord settings.
This is a binary-only beta release; source code is not published in this repository.

Playlist imports: YouTube/YouTube Music public or unlisted links; exported CSV/TXT/XML files from Spotify, Apple Music and other services. Direct Spotify/Apple Music account integration is not available yet. Review matches before saving; uncertain matches are unchecked. Source order and selected duplicates are preserved.

## Aggiornamento beta.5

Solo copertine, vista testo senza sidebar con riga attiva visibile, card Home proporzionate, Discord automatico con logo/brano e pulsante download. Nessun ID o portale sviluppatori richiesto agli utenti.

Recenti e playlist: gestione robusta di metadati vecchi/non validi e navigazione senza texture offscreen. Nessuna cancellazione della cronologia. In caso di errore i dettagli rimangono localmente in `%LOCALAPPDATA%\OndaPlayer\errors.log`.


## Novità beta.6

- Controllo aggiornamenti automatico all’avvio e ogni 6 ore, con avviso nell’app e pulsante download. Include le nuove beta; quando Onda sarà stabile seguirà soltanto le versioni stabili. Si può disattivare in Impostazioni → Aggiornamenti.
- Il download si apre nel browser sullo ZIP ufficiale GitHub. Chiudi Onda, estrai lo ZIP e sostituisci l’eseguibile: nessun riavvio forzato o installazione silenziosa. Playlist, preferiti e cronologia restano in OndaPlayer.
- Ricerca dentro le playlist per titolo, artista o album, anche senza accenti; trascina i brani per riordinarli e salvare l’ordine. Il riordino è disponibile con ricerca vuota. La coda già avviata conserva il suo ordine.
- Duplicati: pulsante con conteggio, rimozione su conferma e annullamento durante la sessione. La verifica usa l’identità del brano, senza confondere remix o live omonimi.
- Impostazioni → Assistenza → Esporta rapporto errori: ZIP locale con versione, sistema e log recenti, senza playlist, preferiti, cronologia o impostazioni. Identificativi comuni oscurati; controlla il contenuto prima di condividerlo. Nessun invio automatico.
- Barra superiore nera come la navigazione. Testi con stati distinti: sincronizzato, semplice, strumentale, non disponibile o servizio temporaneamente irraggiungibile.

Questa versione resta in beta e non introduce registrazione o account.


## Correzione beta.7 — Preferiti e liste corte

Corretto un blocco dell’interfaccia aprendo Preferiti o altre liste con pochi brani: lo spazio sotto il player causava un ciclo continuo di ridimensionamento della scrollbar. Lo spazio finale ora appartiene al contenuto della lista, senza fascia opaca e senza alterare il numero dei brani.
La navigazione è accodata fuori dal clic Windows; Preferiti e Recenti si aprono direttamente e non avviano la preparazione audio automatica. Le chiamate ai controlli multimediali Windows sono accodate e protette dalla rientranza COM.
Il rapporto errori include anche log locali dei blocchi prolungati, senza invio automatico. Playlist e preferiti conservati.
