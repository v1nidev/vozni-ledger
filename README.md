# Vozni ledger

Used-car listing tracker for Croatia. Published at
<https://v1nidev.github.io/vozni-ledger/>.

This repo holds only the rendered page. It is generated, not edited by hand —
changes belong upstream:

- **Curated fields** (model name, body, kW, notes, photos) live in the Notion
  ledger.
- **Scraped fields** (price, km, year, location, status, flags, ad URL) come
  from the `car-scraper` datastore.

`render_page.py` in `car-scraper` merges both into `index.html` and this repo is
the deploy target.

An ad leaving the site does not mean the car was bought — ads expire and get
withdrawn. `gone` records absence, nothing more.
