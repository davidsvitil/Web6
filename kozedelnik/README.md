# Kožedělník – koncept nového e-shopu

Statický frontend (HTML + CSS + vanilla JS, bez buildu) pro kozedelnik.cz. Stejný designový jazyk jako koncepty Montana Cans, Autolaky, Grafficon a další (tmavý rám, zaoblené plochy, plovoucí pill menu, obří „ghost“ nápisy, pozadí se přebarvuje podle barvy kůže vybraného produktu).

**Jde o neoficiální návrh** – stránka má trvalý pruh „KONCEPT“, vodoznak a `noindex`.

## Co umí
- **Kompletní katalog** – 369 produktů v 8 kategoriích (Pro muže, Pro ženy, zápisníky, kryty a pouzdra, doplňky, dárky a pro firmy, psí obojky, workshopy), 93 produktů s variantami (barva kůže, délka opasku).
- Carousel z výřezů produktů, stránka se přebarví podle barvy kůže (koňaková, zelená, bordó…), výběr barvy kůže jako vzorky.
- Košík s dopravou zdarma nad 3 000 Kč, osobní odběr v ateliéru.

## Spuštění lokálně
```bash
cd kozedelnik && python3 -m http.server 8000   # http://localhost:8000
```

## Nasazení
Settings → Pages → Source: **GitHub Actions**, pak Actions → Run workflow. Kořenový `index.html` přesměruje do `kozedelnik/`.

## Struktura
- `index.html`, `css/style.css`, `js/app.js` – sdílená šablona; `js/shop.js` – vše specifické pro obchod
- `data/catalog.json` – katalog; `assets/img/p/` – fotky (WebP), `assets/img/hero/` – výřezy pro carousel

## Co ještě chybí do ostrého provozu
- Platby, sklad a objednávky v reálném čase – ceny jsou snímek z 19. 11. 2026, objednávka zatím odchází e-mailem (mailto).
- Konfigurátory (kůže × nitě × přezka) jsou v náhledu zjednodušené na výběr barvy kůže.
