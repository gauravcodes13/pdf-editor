# PDF Editor

A private PDF editor and simple e-signing tool that runs entirely in the browser. Documents are never uploaded to a server; they are stored in the browser on the device you use.

## Deploying (GitHub Pages, free)

1. Unzip the package. All files sit in one folder, with no subfolders.
2. In your GitHub repository, click **Add file → Upload files**, drag in every file, and click **Commit changes**. Files with the same name are replaced; GitHub keeps the previous versions in the commit history.
3. Under **Settings → Pages**, make sure the source is the `main` branch, `/ (root)`.
4. Wait 1 to 2 minutes, then open `https://YOUR-USERNAME.github.io/REPO-NAME/` and press Ctrl+Shift+R.

No build step, server, API keys or paid services are needed. Any static host works the same way (Netlify, Cloudflare Pages, Vercel).

## What's in the folder

| Files | Purpose |
|---|---|
| `index.html` | The whole app, with its PDF libraries built in |
| `*.ttf`, `*.fontpack` | Fonts for matching and the font menu |
| `worker.min.js`, `tesseract-core-*.wasm.js`, `eng.traineddata.gz` | Text recognition (OCR) |

## Using it

**Edit mode**
- Double-click text to edit it. While editing, you can change font, weight, size, bold, italic, underline and colour.
- Tools: add text, highlight, underline, strikethrough, sticky notes, rectangles, circles, arrows, pen and redaction.
- Highlights, underlines, strikethroughs, shapes, arrows, pen drawings and sticky notes are saved as real PDF annotations, so they stay editable in Acrobat and other viewers.
- Text edits rewrite the PDF's text. Text inside embedded graphics or in unusual font types is drawn over the original instead; the download message says when this happens.
- On scanned pages, run OCR first. Recognized text becomes searchable, and edits are drawn over the scan, matching its background colour.
- Redaction turns the affected pages into images, so nothing underneath can be recovered. Links outside the redacted boxes are kept.
- In Select mode, drag to move, use the corner handles to resize, and press Delete to remove.
- Pages sidebar: drag pages to reorder them, or rotate, duplicate and delete them. **Insert PDF** and **Merge PDF** add pages from another file.
- Find and replace (Ctrl+F), OCR for scanned pages, undo and redo (Ctrl+Z / Ctrl+Y), and versions (Ctrl+S).

**Sign mode**
1. Choose a signer, or use **Add signer**.
2. Place fields: Signature, Initials, Date, Name and Text. Fields belong to the signer selected when you place them; select a field to reassign, move, resize or delete it.
3. Each signer clicks their own fields to fill them in. Signatures can be drawn, typed or uploaded, and saved on this device.
4. Each signer then clicks **Finish signing**, agrees to sign electronically, and their fields are locked.
5. **Download** produces the signed PDF with a signing summary page: signers, times, and a SHA-256 fingerprint of the original file.

These are simple electronic signatures. They do not verify identity and are not certificate-based digital signatures. In Ontario, the Electronic Commerce Act, 2000 generally allows electronic signatures, but some documents (for example wills and certain land transfers) are excluded or have extra requirements. Check before using it for anything legally important.

## Saving and backups

- Documents, edits, versions and signing history save automatically in the browser you use. Your original upload is never changed; **Versions → Original PDF** downloads it.
- Storage belongs to one browser on one device. It is lost if you clear this site's browser data, use a private window or uninstall the browser, so it is not a permanent backup. My documents shows how much space is used and warns when it's running low.
- Rename or delete documents from My documents, or click the file name at the top to rename an open document.
- **Export backup** (on My documents) saves everything to one file. **Restore backup** loads it in any browser on any device. This is how you move work between devices.
