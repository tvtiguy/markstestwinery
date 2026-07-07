# Marksplinter Vineyard — demo site

A **fictional** Willamette Valley winery site used for testing our tasting-room
scheduling and cellar-management software. Marksplinter Vineyard is not a real
winery — all names, wines, awards, and addresses are made up.

Static HTML/CSS, no build step. Deploy the folder as a static site (e.g. Vercel)
or open `index.html` locally.

## Pages
- `index.html` — Home
- `wines.html` — Our Wines
- `club.html` — Wine Club
- `about.html` — About
- `visit.html` — Reservations (hands off to an external scheduler)
- `embed.html` — hidden preview of an *embedded* booking widget (not linked from the nav)

## Scheduler hand-off
On the Reservations page, every **Reserve** button links out to an external
booking system, passing `?winery=marksplinter&venue=<id>`. To point them at the
real scheduler, change one line in `visit.html`:

```js
window.MARKSPLINTER_BOOKING_URL = "https://scheduling.example/book";
```

## Local preview
```
python3 -m http.server 3000
```
then open http://localhost:3000
