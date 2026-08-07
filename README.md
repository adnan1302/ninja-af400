# Ninja AF400 kuharica

Mobilno-prilagođena javna kuharica za Ninja AF400.

## Arhitektura

- Statički frontend: index.html, styles.css, app.js
- Sadržaj: javni Google Sheet, kartica Recepti
- Učitavanje: Google Visualization CSV endpoint
- Otpornost: ugrađeni seed podaci se prikazuju ako Sheet nije dostupan
- Lične postavke: favoriti se čuvaju samo u browseru kroz localStorage
- Hosting: Vercel static hosting bez servera ili tajni

Javni Sheet: https://docs.google.com/spreadsheets/d/1fDokMAGMrqvou6bKlyTDfBXcoeV32LXMykMvIxeMXOs/edit

Kolone koje aplikacija očekuje su: Naziv, Kategorija, Mod, Temperatura °C, Vrijeme, Okretanje / miješanje, Napomena, Status, Favorit, Datum testiranja.

Statusi su ✅ Provjereno, 🟡 Za testiranje i 🔴 Ne preporučujemo. Aplikacija automatski izostavlja redove čiji naziv sadrži riječ slanina.

## Nova funkcionalnost

- Klik na recept otvara detalje.
- Kolona `YouTube link` u kartici `Recepti` prikazuje YouTube player u detaljima.
- Forma `Dodaj recept` je ugrađena u aplikaciju.
- Forma koristi javni append-only Google Apps Script endpoint kada je `WRITE_ENDPOINT` podešen u `app.js`.
