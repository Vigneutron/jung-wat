# jung-wat

Word association test after C. G. Jung's method (1904–1909, published list 1910), running entirely in the browser.

**Live app: https://vigneutron.github.io/jung-wat/**

This repository holds the deployable build — a single `index.html` — published via GitHub Pages by the workflow in `.github/workflows/pages.yml`. Relatedness between stimulus and response is scored on the visitor's device by an open-source embedding model (`all-MiniLM-L6-v2`, Apache-2.0, via transformers.js); the app sends nothing to any server of ours. In mic mode the browser's own speech recognition is used, which in Chrome/Safari involves the browser vendor's servers; typing mode keeps everything on the device.

This is not a diagnostic instrument.
