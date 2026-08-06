# POLI INVENT

Caccia al tesoro in realtà aumentata sugli inventori del Politecnico.
Inquadri un'immagine e compare il modello 3D dell'invenzione + una scheda descrittiva.
Tutto statico, ospitabile gratis su GitHub Pages.

## I file

| File | A cosa serve | Chi lo usa |
|---|---|---|
| **`index.html`** | Il **visore**: fotocamera, riconosce le immagini, mostra 3D + descrizione | i visitatori, dal telefono |
| **`studio.html`** | Lo **studio**: prepari le opere e generi i file | tu, dal computer |
| **`manifest.json`** | I collegamenti immagine→modello→descrizione (già pronto con 8 opere) | — |
| **`targets.mind`** | Le 8 immagini compilate | — |
| **`models/`** | I modelli `.glb` (opera00.glb … opera07.glb) — **da caricare tu** | — |

## Novità di questa versione
- **Descrizione in AR**: ogni opera ha un testo che compare inquadrando (lo scrivi nello Studio).
- **Caricamento uno-alla-volta**: i modelli si scaricano solo quando inquadri la loro immagine
  (così l'app regge anche con modelli pesanti, senza scaricare tutto all'avvio).

## Pubblicare
1. Crea una repo GitHub (es. `POLI-INVENT`), pubblica.
2. Carica: `index.html`, `studio.html`, `manifest.json`, `targets.mind`, e i modelli in `models/`.
3. Settings → Pages → branch `main` / root.
4. Visore: `https://TUONOME.github.io/POLI-INVENT/` · Studio: `.../studio.html`.

## Aggiungere / modificare opere
Apri `studio.html` **dal sito**, aggiungi o modifica le opere (immagine, modello, descrizione,
posizione X/Y/Z, rotazione, luci), poi **⚙ compila targets.mind** + **⬇ manifest.json** e ricarichi
questi due file (+ eventuali nuovi `.glb` in `models/`).

## Regole d'oro
1. Le opere si contano **da 0** (1ª = target 0).
2. Il file dei collegamenti deve chiamarsi **`manifest.json`**.
3. Immagini bersaglio **dettagliate e contrastate**.
4. Dopo ogni upload **aspetta 1–2 minuti** (GitHub Pages non pubblica all'istante).
5. Modelli `.glb` **leggeri** (max ~2 MB l'uno se puoi): caricano molto più in fretta sul telefono.
