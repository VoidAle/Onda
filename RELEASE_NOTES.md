# Onda 0.1.0-beta.8

- Nuovo **Wrapped**: minuti di ascolto effettivi (i salti nella barra non contano) e classifiche di brani, artisti e album per mese, anno o da sempre, con riproduzione dei tuoi preferiti. Tutto resta sul computer.
- **Velocità**: connessioni a YouTube Music riutilizzate invece di riscaricare la pagina iniziale a ogni richiesta; ricerca artista e discografia in parallelo; audio dei videoclip preparato in anticipo; link audio validi per ore; ricerca mentre scrivi più leggera; impostazioni e traduzione dell’interfaccia senza ricalcoli inutili.
- **Ricerca**: con una ricerca in italiano i brani omonimi in altre scritture (es. hindi, tamil, arabo) scendono in fondo; salgono quelli con tutte le parole cercate e degli artisti che ascolti di più.
- **Animazioni**: il brano scorre a sinistra quando vai avanti e a destra quando torni indietro; dissolvenza nel cambio tema; menu arrotondati e animati con icone.
- **Temi**: Chiaro, Scuro, Oceano, Aurora, Foresta, Tramonto, Rosa, Lilla, Avana, Sabbia e Personale (scegli il colore e lo sfondo chiaro o scuro).
- **Playlist**: immagine personalizzata, condivisione tramite codice da incollare o file .onda (“Apri playlist condivisa”), nuova finestra “Salva in playlist” con ricerca e creazione rapida.
- **Ascolto offline**: scarica un brano, una playlist o una raccolta; i brani scaricati partono subito, anche senza Internet.
- **Videoclip facoltativo**: pulsante nella vista di ascolto e opzione nelle Impostazioni; disattivato resta la copertina dell’album.
- Corretto: a volte la finestra non si riduceva a icona (anche dalla barra delle applicazioni). Player e barra laterale più compatti; link per le segnalazioni sul server Discord.
- L’eseguibile pubblico non contiene più il codice di test interno.
- **Più fluida e più bella**: scorrimento delle liste più leggero (le copertine non vengono più ridimensionate a ogni fotogramma), sfondo animato che non consuma risorse quando non serve, dissolvenza nell’apertura della finestra e nel cambio pagina, effetto vetro più curato su player e vista di ascolto (riflesso sul bordo alto e bordo luminoso), pulsanti che reagiscono alla pressione, maniglie di scrollbar e slider che si illuminano al passaggio del mouse. Con “Riduci le animazioni” tutto resta statico.
- Corretto: chiudendo l’app durante un caricamento di rete poteva restare un processo invisibile; ora si chiude entro 20 secondi.
- Corretto: le copertine che non si caricavano per un errore di rete restavano vuote fino al riavvio; ora vengono riprovate.
- Corretto: il volume viene salvato anche se lo cambi con tastiera o rotellina.
- Corretto: collegare o scollegare un dispositivo audio non interrompe più la musica se l’uscita scelta non cambia.
- Corretto: testi non trovati per brani senza durata nota; rinomina ed eliminazione di playlist non più soggette a errori con menu non aggiornati.
- **Sicurezza**: i codici di playlist condivisa hanno ora un limite di dimensione (8 MB, 5000 brani) contro codici costruiti per esaurire la memoria.
- I file di log diagnostici vengono mantenuti entro circa 512 KB. Il nome predefinito nel saluto è “Ascoltatore”.

Scarica **Onda-0.1.0-beta.8-windows-x64-final.zip**, estrailo e avvia Onda.exe. Le beta precedenti rilevano questa versione dal controllo aggiornamenti. Chiudi la vecchia copia prima di sostituirla. Windows 10/11 x64. Dati locali conservati, sorgenti privati, nessuna registrazione.

# Onda 0.1.0-beta.7

- Corretto il blocco/crash aprendo Preferiti e altre liste con pochi brani: eliminato il ciclo di ridimensionamento della scrollbar. Spazio sotto l’ultimo brano mantenuto nel contenuto della lista, senza fascia opaca.
- Preferiti e Recenti si aprono direttamente, senza passare dalla Home e senza avviare estrazioni audio automatiche.
- Navigazione accodata fuori dall’evento del clic e uscita dalla vista testo senza catture intermedie della pagina.
- Scritture dei controlli multimediali Windows accodate e protette dalle chiamate COM durante input sincrono, con retry limitato degli errori.
- Diagnostica locale dei blocchi prolungati inclusa nel rapporto errori esportabile. Nessun invio automatico.
- Test: 60 clic Qt tra Preferiti e Recenti, liste vuote/corte/lunghe, scorrimento dell’ultimo brano, coda e file originali invariati. Riproduzione del vecchio ciclo con oltre 19.000 variazioni di scrollbar in quattro secondi; comportamento corretto senza il ciclo.

Scarica **Onda-0.1.0-beta.7-windows-x64-final.zip**, estrailo e avvia Onda.exe. La beta.6 rileva questa versione attraverso il controllo aggiornamenti. Per aggiornare chiudi la vecchia copia prima di sostituirla. Windows 10/11 x64. Dati locali conservati, sorgenti privati, nessuna registrazione.

# Onda 0.1.0-beta.6

- Controllo automatico aggiornamenti all’avvio e ogni sei ore, avviso non invasivo e pulsante per scaricare lo ZIP dal repository ufficiale. Controllo manuale nelle Impostazioni; gestione degli errori di rete senza bloccare l’ascolto. Nessun token o account richiesto.
- Ricerca interna alle playlist, riordino dei brani trascinandoli e salvataggio dell’ordine. Rimozione duplicati basata sull’identità del brano, con conteggio, conferma e annullamento nella sessione.
- Esportazione volontaria di un rapporto errori ZIP: versione, sistema e log limitati/oscurati, senza dati della libreria né invio automatico.
- Barra superiore nera, senza fascia grigia in navigazione; sfondo copertina continuo nella vista testo.
- Stati dei testi espliciti e gestione robusta dei timestamp non validi. Conservate le correzioni Recenti/playlist, copertine e Discord della beta.5.
- Verifiche su indici delle playlist filtrate, persistenza del riordino, errori di salvataggio, coda invariata durante le modifiche, aggiornamenti beta/stabili/offline e rapporti errori.

Scarica **Onda-0.1.0-beta.6-windows-x64-final.zip**, estrai i file e avvia Onda.exe. Per aggiornare chiudi prima la vecchia copia; playlist, preferiti e cronologia restano sul computer. Windows 10/11 x64. Versione ancora beta, senza registrazione. Codice sorgente privato.

# Onda 0.1.0-beta.5

- Corretta la gestione di metadati vecchi o non validi aprendo Recenti e playlist; caricamento liste senza effetti grafici offscreen e selezioni transitorie. Cronologia e playlist originali preservate.
- Vista testo immersiva: sidebar nascosta, sfondo copertina continuo fino alla barra superiore.
- Riga cantata sempre disegnata, senza layer grafici per riga che potevano farla sparire nello scorrimento. Bordi del testo sfumati e fonte spostata in alto, senza taglio inferiore.
- Copertine Home quadrate con spazio dedicato a titolo e artista, verificate a 1180/1440/1920 px.
- Solo copertine, nessun video o regolazione manuale dei tempi.
- Associazione dei vecchi videoclip alla versione audio ufficiale compatibile, per usare audio, testo e copertina della stessa versione. Verificati Tommaso, Mattone e Il tempo cura.
- Disattivando il casuale si resta nella playlist e si prosegue dal brano attuale. Player flottante senza fascia opaca; controlli inferiori senza tooltip.
- Discord automatico: scheda Sta ascoltando Onda con logo, titolo, artista, avanzamento e pulsante Scarica Onda. Nessun Application ID o Developer Portal da configurare nell'app. Richiede Discord desktop e condivisione attivita abilitata; si puo disattivare nelle Impostazioni. Nessun token bot richiesto.

Scarica Onda-0.1.0-beta.5-windows-x64-final.zip, estrailo e avvia Onda.exe. Windows 10/11 x64 e Internet. Preferiti, playlist e cronologia locali conservati. Licenze e checksum inclusi. Codice sorgente dell'app non pubblicato.
