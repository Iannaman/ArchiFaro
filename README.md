# ArchiFaro — Sito ufficiale (Beta 5.0.28)

**Dai una rotta ai tuoi documenti.**

Questo repository contiene **solo il sito statico** di ArchiFaro per GitHub Pages. La Beta 5.0.28 per Windows è un'applicazione locale: raccogli i file nella cartella **Da Smistare**, scegli un documento, visualizzi l'anteprima e puoi richiedere l'analisi locale. ArchiFaro suggerisce nome, categoria e destinazione solo quando ci sono indizi sufficienti. L'utente corregge la proposta e **conferma esplicitamente** prima di qualsiasi rinomina o spostamento.

![Anteprima della landing](assets/mare-faro.webp)

## Contenuto

- `index.html` — pagina completa con CSS e JS incorporati
- `assets/mare-faro.webp` — illustrazione del faro e delle onde
- `assets/dashboard-5.0.28.webp` — anteprima UI della release (dati dimostrativi)
- `assets/grafo-v5.0.26.webp` — esempio del grafo documentale, disponibile anche nella 5.0.28
- `assets/archifaro-icon.webp` e `assets/favicon.ico` — identità visiva
- `.nojekyll` — pubblicazione GitHub Pages senza processamento Jekyll
- `GUIDA_PUBBLICAZIONE.md` — istruzioni e configurazione link
- `LICENSE` e `LICENZA_SITO.md` — condizioni dei **soli file del sito**

## Pubblicazione rapida

1. Crea un repository pubblico GitHub, per esempio `ArchiFaro` o `ArchiFaro-Sito`.
2. **Estrai lo ZIP** e carica i file al livello principale del repository, inclusi `index.html` e `assets/`.
3. Apri **Settings → Pages → Build and deployment**: scegli **Deploy from a branch** → `main` → `/(root)` → **Save**.
4. Attendi l'esito della pubblicazione e visita il link mostrato da GitHub Pages.
5. Configura `SITE_CONFIG` in `index.html` per link a repository e release.

Per tutti i dettagli vedi [GUIDA_PUBBLICAZIONE.md](GUIDA_PUBBLICAZIONE.md).

## Download Beta

I pulsanti sono predisposti, ma restano in stato **in preparazione** finché non vengono inseriti link pubblici reali dopo il collaudo Windows. Non caricare eseguibili non collaudati come se fossero definitivi.

## Compatibilità

Sito statico responsive, senza dipendenze CDN né backend. Il software presentato richiede Windows 10/11 x64. L'applicazione è separata dal sito e non viene eseguita da GitHub Pages.

## Licenza

MIT **solo per i file del sito**. Non si applica al codice applicativo né ai binari del software ArchiFaro.
