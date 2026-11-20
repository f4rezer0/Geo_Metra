# Modelli 3D Geo_metra

Visualizzatore dei modelli 3D fotogrammetrici realizzati dall'APS FareZero Makers Fab Lab nel laboratorio Geo_metra del progetto "Manduria: la Forma dell'Acqua" (POC Puglia 2021-2027).

Contiene due modelli, elaborati con WebODM da riprese con drone DJI:

| Modello | Foto | Volo |
|---|---|---|
| Chiesa di San Pietro Mandurino | circa 143 | 13/10/2026 |
| Torre Borraco | circa 227 | 13/10/2026 |

## Cosa c'è

| File | Contenuto |
|---|---|
| `index.html` | pagina pubblica con i due modelli |
| `app.html` | app per tablet a schermo intero, con blocco a PIN (installabile come PWA) |
| `sw.js`, `manifest.json` | funzionamento offline e installazione |
| `*.glb` | i modelli 3D (circa 37 MB in totale) |
| `assets/` | logo e icone |
| `GUIDA-TABLET.md` | come installare e usare l'app sul tablet |

L'app è pubblicata su `https://farezero.org/3d-models/` (pagina `app.html` per i tablet).

## Provarla in locale

I service worker funzionano solo su `localhost` o HTTPS, quindi non aprire i file con doppio clic:

```
python3 -m http.server 8000
```

poi apri `http://localhost:8000/app.html`.

## Aggiornare i modelli

1. Sostituisci i file `.glb` (stesso nome).
2. In `sw.js` cambia il numero di versione, per esempio da `fz3d-v3` a `fz3d-v4`: i tablet scaricano la nuova versione al collegamento successivo.
3. Aggiorna le schede informative (foto, data del volo) in `app.html` e `index.html`.

## Librerie esterne

L'app carica due librerie da CDN, citate nella privacy policy del sito:

- model-viewer 3.5.0 (Google, Apache 2.0) da unpkg
- qrcode.js 1.0.0 (MIT) da cdnjs

Dopo il primo caricamento restano nella cache del tablet e l'app funziona offline.

## Licenza

Da definire: non è ancora stata scelta una licenza per codice e modelli.
