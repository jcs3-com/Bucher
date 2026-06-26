# Bücher

A small, private reading tracker. One HTML file. Your books live in your browser — no account, no server, no build step.

Browse your shelves, rate what you've read, drop books on themed carousels, and import an existing list in seconds. Coverless books render as designed typographic covers; add an ISBN and the real cover appears on its own.

---

## Use this template

Click **Use this template → Create a new repository** at the top of this page. You get your own copy with clean history — yours to host and change.

(Prefer the CLI: `gh repo create my-books --template <owner>/<this-repo> --public`.)

## Put it online

1. In your new repo: **Settings → Pages**.
2. Under **Build and deployment**, set **Source: Deploy from a branch**, **Branch: `main`**, folder **`/ (root)`**, and **Save**.
3. Wait a minute. Your tracker is live at `https://<your-username>.github.io/<your-repo>/`.

That's it. `index.html` is the whole app.

## Make it yours

Open `index.html` and find `var SEED = [ … ]` near the start of the script.

- **Want your own empty tracker?** Set it to `var SEED = [];`. The app then opens straight to an empty personal shelf — no sample, no demo banner — and remembers everything you add.
- **Want to keep a curated public list?** Leave a `SEED` in place (or replace it with your books). The hosted page opens in **sample mode**: visitors can play with it, their changes stay in *their* browser only, and a **Reset** button restores your list. A **Start my own** button lets a visitor switch to their own empty copy.
- **Want real covers on your seeded books?** Add an `isbn` to any seed entry, or a `cover_override` image URL.

Everything in `SEED` follows the same 13-field shape: `id, title, author, isbn, status, rating, started, finished, notes, cover_override, year_pub, genre, carousel`. Keep the `id` values unique (`b000`, `b001`, …).

## Add books

- **One at a time** — the **Add book** button.
- **In bulk** — the **Import** button takes a **CSV**, a **TSV**, a **Markdown table**, or just one book per line (`Title — Author`). It recognizes common spreadsheet and Goodreads column names and skips duplicates automatically. See [`reading-list.md`](./reading-list.md) for the format and a starter list.

Status is forgiving on import: *Finished/Done/Complete* → **Read**, *Currently reading/In progress* → **Reading**, *Want to read/Wishlist/blank* → **To read**, *Abandoned/DNF* → **DNF**. Shelves are comma-separated, so a book can live on several carousels at once.

## Your data, and backing it up

Everything is stored locally in your browser (IndexedDB). Nothing is uploaded anywhere. The practical consequence: **your library is per-browser and per-device.** A different browser, or cleared site data, starts fresh.

So the safety valve is export. **Export CSV** or **Export JSON** any time to keep a copy, move to another device, or commit a snapshot to this repo. Import reads both back.

> Opening the file straight off disk (`file://`) works, but some browsers block remote cover images and local storage there. Hosting it (GitHub Pages, or any static host) is the smoother path; treat a downloaded copy as your offline/backup version.

## What it deliberately doesn't do

No accounts. No backend or database. No real-time sync. No tracking. It's a personal shelf, kept simple on purpose. If you outgrow a few thousand books, that's the moment to graduate to a real datastore — not before.

## License

MIT — see [`LICENSE`](./LICENSE). Use it, fork it, give it away.
