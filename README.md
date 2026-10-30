<p align="center"><img src="assets/onda.png" width="88" alt="Onda"></p>
<h1 align="center">Onda · Windows beta</h1>
<p align="center">Un lettore musicale minimale, con playlist, testi e controlli Windows.</p>
<p align="center"><a href="https://github.com/VoidAle/Onda/releases/tag/v0.1.0-beta.1">Scarica la beta</a> · <a href="https://discord.com/users/1007318097985798144">Segnala un bug su Discord</a></p>

## Installazione

1. Apri la [release 0.1.0-beta.1](https://github.com/VoidAle/Onda/releases/tag/v0.1.0-beta.1).
2. Scarica **Onda-0.1.0-beta.1-windows-x64.zip** ed estrai il contenuto.
3. Avvia **Onda.exe**. Non serve installare Python o Node.js.

Richiede Windows 10/11 a 64 bit e una connessione Internet. La beta non e firmata digitalmente.
Il pacchetto contiene le licenze dei componenti di terze parti e il file SHA256SUMS.txt.

## Cosa puoi fare

- Cercare brani, artisti, album e playlist nel catalogo YouTube Music.
- Aprire il profilo di un artista e sfogliare le uscite, con copertine e scorrimento animato.
- Creare playlist locali, scegliere il casuale, gestire la coda e continuare con suggerimenti.
- Salvare i **Preferiti** con il cuore o dal menu **⋯** di un brano.
- Riaprire **Recenti**, la cronologia dei brani realmente avviati.
- Aprire la vista di ascolto con copertina/video e testo sincronizzato quando disponibile.
- Impostare il **timer di spegnimento** dal simbolo orologio o da Impostazioni: allo scadere la musica va in pausa.
- Scegliere tema chiaro/scuro, Italiano/English, dimensione del testo e movimento ridotto.
- Usare i controlli multimediali di Windows.

Per riprodurre un brano clicca sulla sua copertina. Il resto della riga seleziona il brano.
Il casuale si attiva prima del Play; il menu **⋯** raccoglie le altre azioni.

## Segnalare un bug

Scrivimi su **[Discord](https://discord.com/users/1007318097985798144)** (ID: `1007318097985798144`).
Il collegamento apre il profilo: la possibilita di inviare messaggi dipende dalle impostazioni di Discord.
Puoi aprirlo anche da **Impostazioni → Segnala un bug su Discord**.

Per aiutarmi a riprodurre il problema, indica:

- versione di Onda e versione di Windows;
- passaggi eseguiti e comportamento atteso;
- titolo/artista o link del brano, se riguarda la riproduzione o i testi;
- uno screenshot, se utile, evitando dati personali.

## Stato della beta

Sono possibili bug e ritardi di rete. Catalogo, riproduzione, video e testi dipendono da servizi esterni:
la disponibilita puo cambiare e alcuni testi non hanno timestamp. Onda preferisce testi sincronizzati
compatibili con la versione del brano, senza inventare i tempi mancanti.

Non e richiesto un account Onda. Playlist, preferiti, cronologia e impostazioni sono salvati
localmente in `%LOCALAPPDATA%\OndaPlayer`. Il pacchetto distribuito non contiene librerie personali.
Le ricerche e le richieste di riproduzione/testi vengono inviate ai rispettivi servizi esterni.

Questo repository distribuisce **il programma e la documentazione**; il codice sorgente di Onda non e pubblicato.
I componenti di terze parti conservano le proprie licenze, incluse nel pacchetto.

## English

Onda is a minimal Windows music player, currently in beta. Download the ZIP from
[Releases](https://github.com/VoidAle/Onda/releases/tag/v0.1.0-beta.1), extract it, and run **Onda.exe**.
Windows 10/11 x64 and an Internet connection are required. No Python or Node.js installation is needed.

Features include artist profiles, albums, local playlists, favorites, listening history, a sleep timer,
lyrics when available, optional video artwork, Windows media controls, light/dark themes and an English interface.
Change the language in **Settings → Language**.

Report bugs via **[Discord](https://discord.com/users/1007318097985798144)** and include the app version,
Windows version, reproduction steps, and the affected song/link. Messaging availability depends on Discord settings.
This is a binary-only beta release; source code is not published in this repository.
