# r0b5k3f0.github.io

A polished GitHub Pages landing page for **r0b5k3f0**.

- Single-file static homepage (`index.html`)
- Custom `404.html`
- No external CDN, images, or fonts required
- Responsive layout with accessible reduced-motion support

Visit: https://r0b5k3f0.github.io/

## Favicons

SVG favicon set:

- `/favicon.svg` — default neon R favicon
- `/favicons/favicon-orb.svg`
- `/favicons/favicon-diamond.svg`
- `/favicons/favicon-circuit-r.svg`
- `/favicons/favicon-terminal.svg`
- `/favicons/favicon-mask.svg`
- `/favicons/preview.html` — icon preview gallery

## Tools

- `/tools/video-converter/` — browser-only FFmpeg WebAssembly video converter. It runs entirely as a static GitHub Pages app and uses ffmpeg.wasm in the user's browser.
- `/tools/python-lab/` — browser-only Python IDE powered by Pyodide/WebAssembly.
- `/tools/jupyter/lab/` — JupyterLite notebook environment with Python (Pyodide) kernel.


### FFmpeg assets

The converter vendors the single-thread ffmpeg.wasm runtime under `/tools/video-converter/vendor/ffmpeg/` so the tool does not depend on third-party CDN scripts for normal operation. The page also implements its own small `fetchFile` / `toBlobURL` helpers to avoid the broken UMD global issue in `@ffmpeg/util`. External CDNs remain as fallback sources only.


### Python / Jupyter assets

- Python Lab loads Pyodide from a public static CDN and executes code locally in the browser.
- JupyterLite is built as static assets under `/tools/jupyter/`; notebooks and user files are stored in the browser by JupyterLite.
