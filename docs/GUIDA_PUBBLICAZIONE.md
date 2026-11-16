# Pubblicazione del sito — ArchiFaro

Il sito risiede in **`/docs`** nel repository pubblico [Iannaman/ArchiFaro](https://github.com/Iannaman/ArchiFaro). I sorgenti del programma Windows **non vanno caricati** qui.

## GitHub Pages

Il workflow **`.github/workflows/pages.yml`** esegue la pubblicazione dal ramo `main` e dalla cartella `docs`.

1. Apri **[Settings → Pages](https://github.com/Iannaman/ArchiFaro/settings/pages)**.
2. In **Build and deployment → Source**, seleziona **GitHub Actions** e salva. Questa operazione è necessaria se non è già selezionata.
3. Apri **[Actions](https://github.com/Iannaman/ArchiFaro/actions)**, seleziona **Pubblica il sito ArchiFaro** e lancia **Run workflow**, se non è già in esecuzione.
4. Dopo un deploy riuscito, controlla il collegamento indicato da Pages, normalmente **https://iannaman.github.io/ArchiFaro/**.

Non affermare che il sito sia online finché il deploy non risulta concluso e la pagina non risponde correttamente.

## Link ai download (non ancora pubblicati)

Apri `docs/index.html` e trova `SITE_CONFIG`. Il campo `projectUrl` è già impostato al repository. Quando avrai pubblicato in **Releases** gli asset collaudati, inserisci in `installerUrl` e `portableUrl` i link ufficiali esatti. Fino ad allora i pulsanti dichiarano *In arrivo*.

## Licenza

La licenza MIT in `docs/LICENSE` riguarda soltanto il sito. Nessun sorgente Go, installer o ZIP applicativo viene pubblicato automaticamente da questo workflow.
