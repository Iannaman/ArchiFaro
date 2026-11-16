# Pubblicare il sito ArchiFaro su GitHub Pages

## A. Caricamento immediato (repository dedicato al sito)

1. Vai su https://github.com/new e crea un repository **Public**, per esempio `ArchiFaro-Sito`.
2. Estrai `ArchiFaro_Sito_GitHub_Pages_5.0.28.zip` sul PC.
3. Nel repository: **Add file → Upload files**. Carica `index.html`, `assets/`, `.nojekyll`, `README.md`, `LICENSE` e gli altri file **dopo aver estratto lo ZIP**. GitHub non pubblica automaticamente il contenuto di uno ZIP caricato come singolo file.
4. Salva nel ramo `main`.
5. Vai su **Settings → Pages** → **Build and deployment** → **Source: Deploy from a branch** → **Branch: main** → **Folder: /(root)** → **Save**.
6. Dopo il deploy, GitHub mostrerà l'indirizzo del sito. Un esempio per il repository `iannaman/ArchiFaro-Sito` è `https://iannaman.github.io/ArchiFaro-Sito/` (l'indirizzo dipende dal nome effettivo).
7. Controlla da PC e telefono che immagini, fasi interattive, bottoni e favicon siano visibili.

## B. Se vuoi usare il repository principale `ArchiFaro`

Puoi mettere **solo** `index.html` e `assets/` in una cartella `/docs` del repository pubblico e impostare GitHub Pages su `main` + `/docs`. Documentazione e programma possono restare in repository differenti. Evita di rendere pubblici i sorgenti Go se non vuoi ancora aprirli.

## C. Attivare i download dopo il collaudo

Apri `index.html` con un editor e cerca questa configurazione nella parte finale:

```javascript
const SITE_CONFIG = Object.freeze({
  projectUrl: "",   // URL del repository pubblico
  installerUrl: "", // link completo ZIP installabile
  portableUrl: ""   // link completo ZIP portable
});
```

Inserisci URL **già pubblicati e accessibili senza autenticazione**. Esempio da adattare ai nomi reali:

```javascript
const SITE_CONFIG = Object.freeze({
  projectUrl: "https://github.com/iannaman/ArchiFaro",
  installerUrl: "https://github.com/iannaman/ArchiFaro/releases/download/v5.0.28-beta/ArchiFaro_5.0.28_Installabile.zip",
  portableUrl: "https://github.com/iannaman/ArchiFaro/releases/download/v5.0.28-beta/ArchiFaro_5.0.28_Portable.zip"
});
```

**Gli indirizzi dell'esempio non sono stati verificati né indicano una release già pubblicata.** Verifica il nome del repository, il tag e i nomi effettivi degli asset prima di salvarli.

Una volta riempiti i campi e fatto commit del file, il sito aggiorna i pulsanti. Finché i campi sono vuoti, il sito dichiara che il download è in preparazione anziché rimandare a un URL inesistente.

### Pubblicare la Beta nelle GitHub Releases

Dopo la verifica su Windows reale, crea una **pre-release** con tag `v5.0.28-beta` e allega:

- `ArchiFaro_5.0.28_Installabile.zip`
- `ArchiFaro_5.0.28_Portable.zip`
- `ArchiFaro_5.0.28_SHA256SUMS.txt`

I file `.exe` non sono firmati digitalmente. Non invitare gli utenti a disattivare SmartScreen o l'antivirus.

## D. Pubblicare il sito senza pubblicare il codice Go

Struttura raccomandata:

```
ArchiFaro-Sito (pubblico)        — index.html, assets/, guide, Issues/feedback
ArchiFaro-App (privato)         — sorgenti Go, frontend desktop, test, build
ArchiFaro (pubblico opzionale)  — README, guide e GitHub Releases dei binari
```

Puoi usare anche solo due repository, uno pubblico e uno privato. MIT si applica ai file del sito, non al software desktop. Prima della distribuzione della Beta definisci termini d'uso del programma e informazioni minime sul trattamento dati (se in futuro introdurrai servizi online).

## E. Modifiche al sito

Il sito si aggiorna con un nuovo commit su `main`. Il CSS e JavaScript sono incorporati in `index.html` e le immagini sono tutte locali sotto `/assets`.

**Controllo prima del lancio:** lingua e refusi; badge beta; URL del progetto; segnalazione bug; collegamenti agli asset; supporto a schermi stretti; no link inattivi spacciati per funzionanti; messaggi corretti sull'analisi facoltativa e sugli spostamenti solo dopo conferma.
