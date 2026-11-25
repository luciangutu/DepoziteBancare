# Depozite Bancare

Aplicație web simplă pentru evidența depozitelor bancare personale. Rulează integral în browser, fără server — datele se salvează în `localStorage`.

## Funcționalități

- Adăugare manuală de depozite (perioadă, valoare, valută, date, dobândă)
- Import din fișier CSV sau text lipit
- Export CSV pentru backup
- Calcul automat dobândă netă (brut − 10% impozit) și total la scadență
- Sumar pe valute (total depus, dobândă, scadență)
- Sortare pe orice coloană
- Indicator luni rămase / expirat (depozitele expirate nu intră în „Total depus”)

## Format CSV

Header (opțional):

```
Perioada luni,Valoare,Valuta,Data deschidere,Data finalizarii,Dobanda %
```

Exemplu:

```csv
Perioada luni,Valoare,Valuta,Data deschidere,Data finalizarii,Dobanda %
12,10000,RON,01.01.2025,01.01.2026,6.5
6,5000,EUR,15.03.2025,15.09.2025,4.2
3,"53029,57",RON,10.06.2025,10.12.2025,"4,7"
```

- Separatori acceptați: virgulă, punct-și-virgulă, tab
- Formate de dată: `dd.mm.yyyy`, `dd/mm/yyyy`, `yyyy-mm-dd`
- Valorile cu virgulă ca separator zecimal se pun între ghilimele: `"53029,57"`

## Demo

Aplicația este publicată la: **https://depozitebancare.netlify.app/**
sau la: **https://depozitebancare.climb.ro/**

## Deployment

Fișier static unic (`index.html`). Se poate publica pe orice hosting static (Netlify, GitHub Pages, etc.) — nu necesită build sau dependențe.

## Versionare

Versiunea curentă este afișată discret în subsolul paginii și se modifică manual în `index.html`:

```html
<footer class="app-version">v1.1.0</footer>
```

Actualizează versiunea din `index.html` la fiecare release.
