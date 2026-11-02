# PDF Editor

A private PDF editor that runs entirely in your browser. Your documents are never uploaded anywhere; they are stored only in the browser you use.

## Updating your GitHub site

1. Unzip the package. All files sit together in one folder, with no subfolders.
2. On your repository, click **Add file → Upload files**, drag in every file, and click **Commit changes**. Files with the same name are replaced.
3. Wait 1 to 2 minutes, then open your site and press Ctrl+Shift+R.

## What's in the folder

- `index.html`: the whole app
- `*.ttf`, `*.fontpack`: fonts
- `worker.min.js`, `tesseract-core-*.wasm.js`, `eng.traineddata.gz`: text recognition (OCR)

## Tools and shortcuts

| Action | How |
|---|---|
| Select, move, resize, delete annotations | V, drag, corner handles, Delete |
| Edit existing text | Double-click text, or T then click |
| Add new text | A, then click |
| Highlight / underline / strikethrough | H / U / K, drag across text |
| Sticky note | N, click |
| Rectangle / circle / arrow / pen | R / O / L / P |
| Redact | X, drag a box |
| Bold / italic / underline while editing | Ctrl+B / Ctrl+I / Ctrl+U |
| Undo / redo | Ctrl+Z / Ctrl+Y |
| Find and replace | Ctrl+F |
| Save a version | Ctrl+S |
| Zoom | Ctrl+= / Ctrl+- / Ctrl+0 |

Pages: use the left sidebar to drag pages into a new order, or hover a page to rotate, duplicate or delete it. **Insert PDF** adds another file after the current page; **Merge PDF** adds it at the end.

## How editing works

- **Text edits rewrite the PDF.** The original words are removed from the file and the new text is written in their place, using the PDF's own font when possible. Text inside complex graphics, or in unusual font types, is drawn over the original instead; the download message tells you when that happens.
- **Redaction** turns the affected pages into images, so nothing underneath can be recovered. Text on those pages is no longer selectable.
- **OCR** reads scanned pages so you can search them, and edit them by drawing over the scan.
- Your original upload is never changed. **Versions** lets you save snapshots, restore them, and download any version or the original.

## Your saved work

Everything saves automatically in this browser. Use **Export backup** (on the My documents screen) now and then, and **Restore backup** to move work to another device.
