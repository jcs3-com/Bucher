# Reading list

A starter list for [Bücher](./). Two ways to use it:

1. **Import it.** Open Bücher, click **Import**, and paste the table below (or upload this file). Bücher reads Markdown tables directly and skips duplicates.
2. **Keep it as your list.** Edit the rows, commit the file, and it renders as a clean reading list right here on GitHub.

The example rows below are just to show the format — delete them and add your own.

| Title | Author | Status | Rating | Year | Genre | Shelves |
|-------|--------|--------|--------|------|-------|---------|
| Dune | Frank Herbert | Read | 5 | 1965 | Science Fiction | Favorites, Sci-Fi |
| The Left Hand of Darkness | Ursula K. Le Guin | Read | 4 | 1969 | Science Fiction | Sci-Fi |
| Pachinko | Min Jin Lee | Reading | | 2017 | Historical Fiction | Big Reads |
| The Overstory | Richard Powers | To read | | 2018 | Literary Fiction | Big Reads |
| Project Hail Mary | Andy Weir | Read | 5 | 2021 | Science Fiction | Sci-Fi, Favorites |
| Infinite Jest | David Foster Wallace | DNF | | 1996 | Literary Fiction | |

## Columns

Only **Title** is required. Everything else is optional — leave a cell blank and Bücher fills in a sensible default.

- **Title** — the book.
- **Author** — one name or several; whatever you'd write on a shelf.
- **Status** — `Reading`, `Read`, `To read`, or `DNF`. Bücher is forgiving: *Finished / Done / Complete* become **Read**, *Currently reading / In progress* become **Reading**, *Want to read / Wishlist / blank* become **To read**, *Abandoned / Did not finish* become **DNF**.
- **Rating** — a whole number 1–5, or blank.
- **Year** — year published.
- **Genre** — free text; it also tints the placeholder cover.
- **Shelves** — themed shelves, **comma-separated**. A book can sit on several at once (see *Sci-Fi, Favorites* above). These are the horizontal carousels in the app, and they're independent of status.

## Covers

Leave the cover alone and Bücher draws a typographic one from the title, author, and genre. Add an **ISBN** to a book (in the app, or as an `ISBN` column here) and it fetches the real cover automatically. You can also paste a direct image URL into a book's **Cover URL** field.

## Already have a list somewhere?

Export it as **CSV** (Goodreads, StoryGraph, a spreadsheet — all fine) and paste that into Import instead. You don't need to reshape it: Bücher recognizes common column names, including Goodreads' `ISBN13`, `My Rating`, `Exclusive Shelf`, and `Bookshelves`. Duplicates are skipped on the title + author match.
