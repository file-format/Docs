{
  "date" : "2021-02-10",
  "keywords" :[ "jpx-fil", "jpx-filformat", "vad är en jpx-fil", "fil", "jpx-exempel", "jpx-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX - Bildfilformat",
  "description":"Läs mer om JPX-filformat och API:er som kan skapa och öppna JPX-filer.",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Vad är en JPX fil? ##

En fil med filtillägget .jpx är ett tillägg till filformatet JPEG 2000. Den använder primärt JPEG 2000-komprimering och ger även avancerade funktioner som flera lager för en bild, olika färgrymder, opacitet och fragmenterade kodströmmar. JPX tillåter även andra komprimeringar som JBIG, CCITT Group3, CCITT Group4, etc. förutom JPEG 2000-komprimeringen. JPX-filformatet godkändes som [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html) standard, men kunde inte ta emot ett varmt mottagande på grund av den omfattande användningen av [JPEG ](/sv/image/jpeg/) filformat. Program som kan öppna JPX-filer inkluderar Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 och CorelDraw Graphics Suite 2020.

## Kortfattad bakgrund

År 2000 designade Joint Photographic Experts Group-kommittén JP2 med målet att förbättra sin egen diskreta cosinustransformationsbaserade JPEG-standard med denna nya wavelet-baserade metod. JPEG-kommittén hade som mål att tillhandahålla sina baslinjemetoder fria från licensavgifter. När JP2-licensen fick konkurrens bland 20 företag vann de med morrhår. JPEG 2000 har deklarerats som en ISO-standard, även om de flesta webbläsare inte är redo att ge en hand till JPEG 2000 sedan 2017. 2004 accepterades ISO/IEC 15444-2-formatet offentligt som en tillägg till JP2-filformatet.

## JPX filformat

JPX-filformatet har formulerats för att möta kraven för applikationer som behövde datastrukturer utöver den funktionalitet som definieras av filformatet [JP2](/sv/image/jp2/). En JP2-fil med icke-kompatibla tillägg kan leda till förvirring på marknaden där vissa läsare kan tolka vissa JP2-filer men inte andra. JPX är svaret på att undvika sådana problem i applikationer.

### Filidentifiering

JPX-filer lagras som [JPF](/sv/image/jpf/) när de lagras i ett traditionellt datorfilsystem. Det är därför som JPX-termen är minst vanligt förekommande jämfört med JPF. En JPX-fil börjar med följande byte:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Filorganisation

I likhet med JP2 är en JPX-fil en samling lådor som har en binär struktur med rutorna arrangerade i en sammanhängande ordning. Den första rutan ger starten till filen med dess första byte och den sista byten i den sista rutan representerar den sista byten i filen.
Den binära strukturen för en ruta i en JPX-fil är identisk med den som definieras i filformatet [JP2](/sv/image/jp2/).

### Lagring av CodeStream i JPX

JPX-filformatet gör att bildkodströmmen kan delas upp i fragment. Detta gör det möjligt att modifiera en enda ruta i bilden och skriva den modifierade brickan till slutet av filen utan att skriva om hela filen. Det ursprungliga filformatet [JP2](/sv/image/jp2/) begränsar att hela kodströmmen lagras i en sammanhängande del av filen, vilket kan vara problematiskt för bildredigeringsapplikationer som kanske vill modifiera en enda ruta av bilden och uppnå ovanstående stödbarhet av JPX-filformat. Fragmenteringen av bildkodströmmen gör JPX-filformatet överlägset JP2-filformatet. Dessutom tillåter JPX-filformatet att flera kodströmmar kan kombineras och producera renderade resultat. Kodströmmar kan kombineras som sammansättning och animering.

## Referenser ##

* [Översikt över JPEG 2000](https://jpeg.org/jpeg2000)

