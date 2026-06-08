# PDF Toolkit

A small collection of **free, fast, privacy-first PDF tools** that run entirely in your browser. No uploads, no sign-up, no watermarks — your files never leave your device.

🔗 **Live:** _add your Cloudflare Pages URL here_

## Tools

| Tool | File | What it does |
|------|------|--------------|
| 📄 **PDF Page Remover** | `remove.html` | Preview every page, tap the ones you don't need, and download a clean PDF with them removed. |
| 🔗 **PDF Merger** | `merger.html` | Combine multiple PDFs, reorder pages by drag & drop, and pick exactly which pages to keep. |
| 🖼️ **Images → PDF** | `img.html` | Turn JPG/PNG images into a single PDF — reorder, choose page size (A4 / Letter / Legal / fit-to-image) and orientation, tune compression. |

The landing page (`index.html`) links to all three.

## How it works

Everything is **100% client-side** — plain HTML, CSS and JavaScript with no build step. PDF work is done in the browser using:

- [pdf.js](https://mozilla.github.io/pdf.js/) — render page thumbnails
- [pdf-lib](https://pdf-lib.js.org/) — create/modify PDFs
- [SortableJS](https://sortablejs.github.io/Sortable/) — drag & drop reordering

These are loaded from CDN, so no installation is required.

## Run locally

Just open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy (Cloudflare Pages)

These are static files, so deployment needs no build:

1. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
2. Select this repository.
3. Build settings: **Framework preset = None**, **Build command = (empty)**, **Build output directory = `/`**.
4. Deploy. Every push to `main` auto-redeploys.

## Author

**Abhin Krishna**

- Website: [abhinkrishna.com](https://abhinkrishna.com)
- GitHub: [@dearabhin](https://github.com/dearabhin)
- LinkedIn: [abhin-krishna](https://linkedin.com/in/abhin-krishna)
