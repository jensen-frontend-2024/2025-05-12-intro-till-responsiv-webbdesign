
# 2025-05-12-intro-till-responsiv-webbdesign

# 📱 Introduktion till responsiv layout

När vi bygger moderna webbplatser behöver vi se till att de fungerar på olika skärmstorlekar – från mobil till stora desktopskärmar. Det kallas för **responsiv design**.

## [Länk till presentation](https://docs.google.com/presentation/d/16w_t-XpipcYwPuVsUFXAcSmWxgdmj8_KrHPb-0RiYdE/edit?usp=sharing)

## 🔍 Viewport

`viewport` är det område som används för att visa webbplatsen i webbläsaren. Vi styr den med följande `meta`-tagg i `<head>`:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

## 📏 Enhetstyper i CSS

När vi jobbar med responsiv design behöver vi använda olika sorters måttenheter beroende på vad vi vill åstadkomma:

- `px` – **Pixlar** (absolut enhet, används ofta men kan bli stelbent i responsiva sammanhang)
- `%` – **Procent**, relativ till det elementets förälder – användbart för att skapa flexibla layouter
- `em` – Relativ till **fontstorleken** på det aktuella elementet
- `rem` – Relativ till **root-elementets** (html) fontstorlek
- `vw` / `vh` – Viewport Width / Height – procent av skärmens bredd eller höjd

Exempel:

```css
width: 50vw; /* 50% av skärmens bredd */
font-size: 1.2rem; /* 1.2 gånger grundstorleken */
```

## 🎯 Media Queries

**Media queries** används i CSS för att anpassa en webbsidas utseende beroende på t.ex. skärmens bredd, höjd, upplösning eller orientering. De är en central del av **responsiv design**.

### 📘 Exempel

```css
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

**Vad händer?**  
När skärmens bredd är 600 pixlar eller mindre (t.ex. på en mobil), får `body` en ljusblå bakgrund.

### 🔧 Vanliga användningsområden

- Göra text mindre/större på mobil
- Dölja eller visa element
- Ändra layout mellan kolumner och rader

### 📐 Tips

- Använd `max-width` för att styla när skärmen är **mindre än** ett visst värde.
- Använd `min-width` för att styla när skärmen är **större än** ett visst värde.
- Kombinera flera media queries för att skapa **breakpoints** – t.ex. en för mobil, en för surfplatta och en för desktop.

```css
/* Mobil (upp till 768px) */
@media (max-width: 768px) {
  .menu {
    display: none;
  }
}

/* Desktop (från 1024px och uppåt) */
@media (min-width: 1024px) {
  .container {
    max-width: 960px;
    margin: 0 auto;
  }
}
```

🧠 **Kom ihåg:** Media queries låter dig skapa flexibla, användarvänliga gränssnitt som fungerar på alla enheter!

---

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
