# PDF Text Editor

A personal website for editing text in PDFs. Open a PDF, click any text to change it or delete words, then download the edited PDF. It keeps the original look: same font when the PDF contains the letters you type, otherwise a font with matching letter widths (Calibri, Cambria, Arial/Helvetica, Times, Courier), plus the original size, colour and background.

It is a static website: plain HTML, JavaScript and font files. No server, no database, no build step. Any free static host can run it, and it keeps working for as long as that host account exists.

## Put it online with GitHub Pages (free, no expiry)

1. Create a free account at https://github.com (skip if you have one).
2. Click **+** (top right) → **New repository**. Name it, for example `pdf-editor`. Set it to **Public**. Click **Create repository**.
3. On the new repository page, click **uploading an existing file**.
4. Unzip `pdf-editor-site.zip` on your computer. Open the unzipped folder, select **everything inside it** (`index.html`, `fonts`, `lib`, `README.md`, `.nojekyll`) and drag it into the GitHub page. Wait until all files are listed, then click **Commit changes**.
   - On a Mac, press Cmd+Shift+. in Finder to see `.nojekyll`. If you skip it, the site still works.
5. Go to **Settings** → **Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, branch **main**, folder **/ (root)**. Click **Save**.
6. After 1 to 2 minutes, the page shows your address: `https://YOUR-USERNAME.github.io/pdf-editor/`. Bookmark it on your computer and phone.

Your PDFs are never uploaded to GitHub. Only the editor's code is public; your documents stay on your device.

### Optional: your own domain

Buy a domain from any registrar (Cloudflare, Namecheap, Porkbun, about $10 to $15 a year). In the repository go to **Settings → Pages → Custom domain**, enter it, and follow GitHub's DNS instructions. You own the domain through your registrar account.

## Where your work is saved

- Every PDF you open and every edit is saved automatically in the browser you use (IndexedDB). Refreshing, closing the tab or restarting the computer does not erase it. Saved files never expire.
- **My documents** lists saved PDFs. Open one to pick up where you left off.
- **Export backup** downloads one `.json` file with all your PDFs and edits. Keep it somewhere safe (Google Drive, OneDrive, email to yourself). **Restore backup** loads it back, in any browser on any device.
- Things that DO erase browser data: clearing site data or browsing history for this site, private/incognito windows, and uninstalling the browser. Export a backup now and then for this reason.
- Saved data belongs to one browser on one device. To move work from your computer to your phone, export a backup on one and restore it on the other.

## Making changes later

- All the app logic is in `index.html`. Edit it on GitHub (open the file → pencil icon → **Commit changes**). The site updates within a minute or two.
- You can also give `index.html` to any AI assistant or developer and ask for changes, then upload the new file the same way.
- `lib/` holds the open-source libraries (pdf.js 3.11.174 by Mozilla, pdf-lib 1.17.1, fontkit). `fonts/` holds the matching fonts (Liberation, Carlito, Caladea; SIL Open Font License, free to use and share).

## Good to know

- Edits cover the old text with the background colour and draw the new text on top. The page looks right and prints right, but the old words are still inside the file underneath. Do not use this to hide confidential information; use a proper redaction tool for that.
- Only horizontal text is editable. Scanned PDFs (images of text) have no editable text.
- Password-protected PDFs can't be opened.
