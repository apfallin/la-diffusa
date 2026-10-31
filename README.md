# La Diffusa

**lo scaffale diffuso / das verteilte Bücherregal / the distributed bookshelf**

A distributed neighborhood bookshelf for Berlin: books in foreign languages, lent between neighbors, Kiez by Kiez.

👉 **Live site:** <https://apfallin.github.io/la-diffusa/>

## Why

Berlin's public libraries are excellent, but they carry very few international titles — especially children's books in their original languages. La Diffusa fills that gap: neighbors lend each other the books the libraries don't have, and meet each other in the process.

## How it works

1. **Offer or search** — open the site, tap *Offri un libro* / *Cerco un libro* and fill the short form (scan the ISBN barcode with your phone camera and most details fill themselves).
2. **Find a book** — browse the shelf by covers, filter by type (offers/wishes), age group, Kiez and language, or let the dice surprise you.
3. **Ask for a loan** — tap *Scrivi a chi lo offre*: a ready-made email goes to the project's address. The lender gets a simple request (PRESTO / NON ADESSO) and shares their contact only after accepting. Books on loan are marked on the shelf.
4. **Borrow & return** — mark your book before lending it (a label with your initials works), then return it when done. A book that travels is a book that makes friends.

## Principles

- **Kiez is an orientation, not a border** — books are shown by neighborhood, but anyone in the city can borrow anything.
- **No names on the site** — books are offered *by a neighbor of <Kiez>*; your contact details stay private and are only shared for a concrete loan, with your consent.
- **All ages, all languages** — from picture books to novels, with dedicated age brackets for children and teens.
- **Lightweight by design** — a single self-contained HTML file, no build step, no cookies, no tracking, hosted on GitHub Pages.

## Tech

- Single-file static site (HTML + CSS + JS, inline) published on GitHub Pages.
- New books arrive through a short Google Form; a small automated keeper reads the responses, verifies ISBNs and updates the catalog (a human curator reviews anything unusual).
- Loans are coordinated via the project's email alias: requests are matched to lenders, contacts shared only after the lender's go-ahead.
- Book covers come from the [Open Library](https://openlibrary.org) API by ISBN, with a graceful illustrated fallback when no cover exists.
- Trilingual interface: Italiano / Deutsch / English, with dark mode ("night shelf"), FAQ and an Impressum & Datenschutz section.

## Roadmap

- **Now (step 1):** curated catalog + mediated contact via email, with a loan status on the shelf.
- **Step 2:** accounts and a real loan registry — loan status, gentle automatic reminders (escalating, never pushy), one-tap returns, and a personal *"my books: X at home, Y lent out"* balance. The goal: no book ever gets lost, and lending stays effortless.
- **Beyond:** each city is its own island — the data model already carries *city + Kiez*, so new cities can be seeded one at a time.
