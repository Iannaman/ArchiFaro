# ArchiFaro — Dai una rotta ai tuoi documenti

**ArchiFaro** è un'applicazione locale per Windows 10/11 x64 che aiuta a organizzare archivi personali e professionali con un percorso semplice, assistito e controllato.

**Stato:** Beta gratuita · **Versione descritta:** 5.0.28 · **Piattaforma:** Windows x64 · **Codice applicativo:** proprietario, non pubblicato.

🌊 **[Scopri il sito ArchiFaro](https://iannaman.github.io/ArchiFaro/)**

## Come funziona

1. **Raccogli:** porta i documenti nella Inbox **Da Smistare** tramite le azioni disponibili nel programma.
2. **Esamina:** visualizza l'anteprima. Se desideri, avvia **Analizza contenuto**: le regole locali propongono categoria, soggetto, data, nome o cartella quando riconoscono indizi sufficienti.
3. **Verifica:** modifica le proposte; trasferirle nei campi non sposta alcun file.
4. **Archivia:** dopo anteprima dell'operazione, controllo collisioni e **conferma esplicita**, ArchiFaro rinomina o sposta il documento.

La scansione del grafo e della dashboard non cambia i file. L'analisi non utilizza AI generativa, cloud o telemetria. PDF testuali supportati in via sperimentale; non è disponibile OCR generalizzato.

## Funzionalità

- Inbox **Da Smistare** e suggerimenti di classificazione.
- Strutture di archivio **Essenziale, Completo e Personalizzato**.
- Anteprime di formati supportati e analisi locale su richiesta.
- Dashboard, grafo categorie, segnalazioni e controlli duplicati.
- Ricerca, gestione dei nomi, backup e ripristino.
- Modalità privacy **Normale, Riservata e Dettagliata**.
- Versioni Windows **Installabile** e **Portable**.

## Download Beta

Sono disponibili i pacchetti **Beta 5.0.28** per Windows 10/11 x64, attualmente come allegati pubblici nella descrizione della [release `v5.0.28-beta`](https://github.com/Iannaman/ArchiFaro/releases/tag/v5.0.28-beta):

- **[Installabile (.zip)](https://github.com/user-attachments/files/34923762/ArchiFaro_5.0.28_Installabile.zip)** — contiene il setup da estrarre.
- **[Portable (.zip)](https://github.com/user-attachments/files/34923760/ArchiFaro_5.0.28_Portable.zip)** — avvio senza installazione, dopo estrazione.
- **[Checksum SHA-256](https://github.com/user-attachments/files/34923757/ArchiFaro_5.0.28_SHA256SUMS.txt)** — per verificare i pacchetti scaricati.

> **Beta / pre-release:** gli eseguibili non sono firmati digitalmente e il collaudo completo in un ambiente Windows reale non è ancora concluso. Prima dell'utilizzo su un archivio importante, prova il programma su una copia di dati DEMO.

Questi link puntano ad **allegati nel testo della release**, non alla sezione GitHub *Assets*. Per una distribuzione stabile e gestibile è preferibile caricare i medesimi ZIP anche come asset ufficiali della release.

## Sito web

La cartella [`docs/`](docs/) contiene la landing page statica pubblicata con GitHub Pages e gli asset SVG originali. Non sono necessari server, database, CDN o installazioni di Node.

## Feedback e sicurezza

Apri un [Issue](https://github.com/Iannaman/ArchiFaro/issues/new) per segnalazioni e suggerimenti. **Non condividere documenti reali, dati personali, percorsi privati o backup negli Issues.**

## Licenze e sorgenti

Questo repository contiene **il sito e la documentazione**, non i sorgenti Go dell'applicazione. I file nella cartella **`docs/`** sono distribuiti alle condizioni della [licenza MIT del sito](docs/LICENSE), limitatamente al materiale di cui il progetto detiene i diritti. **Questa licenza non si estende al programma Windows, ai suoi sorgenti o agli eseguibili.** Le condizioni del software saranno definite separatamente prima della distribuzione.

© 2026 ArchiFaro · iannaman
