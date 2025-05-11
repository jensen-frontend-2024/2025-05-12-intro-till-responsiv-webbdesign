# 2025-05-12-intro-till-responsiv-webbdesign

# 📱 Introduktion till responsiv layout

När vi bygger moderna webbplatser behöver vi se till att de fungerar på olika skärmstorlekar – från mobil till stora desktopskärmar. Det kallas för **responsiv design**.

## 🔍 Viewport

`viewport` är det område som används för att visa webbplatsen i webbläsaren. Vi styr den med följande `meta`-tagg i `<head>`:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">

## 📏 Enhetstyper i CSS
- px – pixlar (absolut enhet)

- % – procent av ett element eller dess förälder (relativ)

- em / rem – relativt till fontstorlek

- vw / vh – viewport width / height, alltså procent av skärmen

## 🎯 Media Queries
Med media queries kan vi ändra stilen beroende på skärmens bredd:

'@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}'

Detta gör t.ex. bakgrunden ljusblå om skärmen är mindre än 600 pixlar bred – perfekt för mobilanpassning!

# 🧩 Övning: Klona en hemsida – fokus på layout och responsivitet

I den här övningen ska ni träna på att bygga upp en enkel webbsida genom att **klona en befintlig sajt**. Syftet är att öva på **layout**, **viewport-anpassning** och **media queries** – alltså hur en sida förändras beroende på skärmstorlek.

Ni har ännu inte lärt er Flexbox eller Grid, så ni får gärna använda enklare tekniker som:

- `inline-block`
- `position`
- `float`

Poängen är inte att det ska bli perfekt – utan att ni **testar, experimenterar och lär er** hur man börjar tänka responsivt.

## 📌 Förslag på sidor att klona

- [https://www.apple.com/se/](https://www.apple.com/se/)
- [https://tldr.tech/](https://tldr.tech/)
- En enkel produkt- eller portfoliowebbplats

## 💡 Tips

- Börja med att klona layouten för **desktop**.
- Lägg sedan till en eller två **media queries** för att anpassa sidan till mobil.
- Använd **Chrome DevTools** för att inspektera hur originalet är uppbyggt.
- Det viktigaste är att ni **försöker förstå strukturen** – inte att allt blir exakt som originalet.

