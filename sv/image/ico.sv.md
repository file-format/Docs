{
  "date" : "2019-10-11",
  "keywords" :[ "ico fil", "ico filformat", "vad är en ico fil", "fil", "ico exempel", "ico filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Bildfilformat",
  "description":"Läs mer om ICO-filformat och API:er som kan skapa och öppna ICO-filer.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en ICO fil?

Filer med ICO-tillägg är bildfiltyper som används som ikon för representation av ett program på [Microsoft Windows](https://www.microsoft.com/en-us/windows). Dessa kommer i olika storlekar, färgstöd och upplösning för att passa skärmens krav. Ett annat liknande bildfilformat på Microsoft Windows är [CUR](/sv/image/cur/) för markörrepresentation och definierar en hotspot i bildhuvudet. På MacOS tjänar ICNS-filformat samma syfte som ICO-filer. Flera webbsidor och applikationer tillhandahåller funktionen att skapa sådana filer och konvertera andra bildformat som [BMP](/sv/image/bmp/), [PNG](/sv/image/png/), etc. till ikonfilformat. Den officiella IANA-registrerade internetmedietypen för ICO-filer är image/vnd.microsoft.icon.

## Kortfattad bakgrund ##

Ikoner introducerades i och med lanseringen av Microsoft Windows 1.0. Dessa var 32x32 stora och var monokroma. Med ankomsten till win32 introducerades stöd för ikonbilder i sann färg med upp till 256x256 pixlar i dimension. Windows XP var först med att ge stöd för 32-bitars färgikonbilder, vilket gjorde att halvtransparenta områden som skuggor, kantutjämning och glasliknande effekter kunde läggas till ikonen. Microsoft rekommenderade endast ikonstorlekar upp till 48×48 pixlar för Windows XP. Windows Vista lade till en ikonvy på 256×256 pixlar i Utforskaren i Windows, samt stöd för det komprimerade formatet [PNG](/sv/image/png/). Med användare som använder högre upplösningar och höga DPI-lägen rekommenderas större ikonformat (som 256×256).

## ICO-filformat ##

En enda ICO-fil består av en eller flera små bilder av flera storlekar och färgdjup. Närvaron av bilder i flera storlekar är för lämplig skalning vid olika skärmupplösningar. Alla värden i ICO/CUR-filer representeras i [little-endian](https://en.wikipedia.org/wiki/Little-endian) byteordning.

ICO-filen består av en ikonhuvud, en ikonkatalog,

|Fält|Beskrivning
---|---|
|Icon Header|Lagar allmän information om ICO-filen.
|Directory[1..n]|Lagar allmän information om varje bild i filen.
|Ikon #1|De faktiska "data" för den första bilden i gammalt AND/XOR DIB-format eller nyare PNG
|...|
|Ikon #n|Data för den sista ikonbilden

### Rubrik ###

|Offset|Storlek (i byte)|Syfte
---|---|---|
|0|2|Reserverad. Måste alltid vara 0.
|2|2|Anger bildtyp: 1 för ikonbild (.ICO), 2 för markörbild (.CUR). Andra värden är ogiltiga.
|4|2|Anger antalet bilder i filen.

### Katalog ###

Katalogen som finns i en ICO-fil, representerad som ICONDIR-struktur, innehåller en ICONDIRECTORY-struktur för varje bild i filen. Detsamma följs av ett sammanhängande block av alla bildbitmappsdata. Detta är som visas nedan.

|Offset|Storlek|Beskrivning
---|---|---|
|0 (0)|1|Bredd, bör vara 0 om 256 pixlar
|1 (1)|1|Höjd, bör vara 0 om 256 pixlar
|2 (2)|1|Färgantal, bör vara 0 om fler än 256 färger
|3 (3)|1|Reserverad, bör vara 0
|4 (4)|2|Färgplan i .ICO-format ska vara 0 eller 1, eller X-hotspot i .CUR-format
|6 (6)|2|Bitar per pixel i .ICO-format, eller Y-hotspot i .CUR-format
|8 (8)|4|Storleken på bitmappsdata i byte.
|12 (C)|4|Offset i filen.

## Referenser ##

* [ICO - av Wikipedia](https://en.wikipedia.org/wiki/ICO_(filformat))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

