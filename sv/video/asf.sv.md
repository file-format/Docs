{
  "date" : "2021-02-15",
  "keywords" :[ "asf-fil", "asf-filformat", "vad är en asf-fil", "fil", "asf-exempel", "asf-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - Advanced Systems File Format",
  "description":"Läs mer om ASF-filformat och API:er som kan skapa och öppna ASF-filer.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Vad är en ASF fil?

En fil med filtillägget .asf är ett multimediafilformat för att lagra och spela upp digitala mediaströmmar över nätverket. Det är ett containerfilformat som kan ha både video- och ljudinnehåll för streaming online. Du kommer sällan att hitta ASF-filer, och fler kommer förmodligen att stöta på Windows Media Audio ([WMA](/sv/audio/wma/)) och Windows Media Video-filer ([WMV](/sv/video/wmv/)) som båda anger ASF-filer ha innehåll kodat med respektive codec. Windows mediafiler kan skapas och läsas med Windows Media Format SDK.

## ASF filformat

En ASF-fil kan bestå av flera oberoende eller beroende strömmar. Detta kan inkludera flera ljudströmmar för flerkanaligt ljud eller videoströmmar med flera bithastigheter. De multipla bithastigheterna gör strömmarna lämpliga för överföring över olika bandbredder. Dessutom kan strömmarna i en ASF-fil vara i komprimerat eller okomprimerat format. Den bästa komprimeringen uppnås med Microsoft Windows Media Audio and Video 9 Series codec. Fullständiga specifikationer för ASF-filformat finns tillgängliga på [Microsofts webbplats](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### ASF-filstruktur på toppnivå

ASF-filer innehåller logiskt sett tre typer av objekt på toppnivå:

* "Header Object" - obligatoriskt och måste placeras i början av varje ASF-fil
* `Dataobjekt` - obligatoriskt och måste följa rubrikobjektet
* "Indexobjekt(er)" - valfritt, men användbart för att ge tidsbaserad slumpmässig åtkomst till ASF-filer

Följande bild visar toppnivåfilstrukturen för ASF-filer.

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF Top-Level Header Object

Header-objektet tillhandahåller en välkänd bytesekvens i början av ASF-filerna och kan valfritt innehålla metadata såsom bibliografisk information. Den innehåller all information som krävs för att tolka informationen i dataobjektet korrekt. Header-objektet kan innehålla flera standardobjekt inklusive, men inte begränsat till:

* Filegenskaper Objekt - Innehåller globala filattribut.
* Stream Properties Object - Definierar en digital mediaström och dess egenskaper.
* Header Extension Object - Tillåter att ytterligare funktioner läggs till i en ASF-fil samtidigt som bakåtkompatibiliteten bibehålls.
* Innehållsbeskrivning Objekt - Innehåller bibliografisk information.
* Skriptkommandoobjekt - Innehåller kommandon som kan köras på uppspelningstidslinjen.
* Markörobjekt - Ger namngivna hopppunkter i en fil.

Rubrikobjektet representeras med följande struktur:

|Fältnamn |Fälttyp |Storlek (bitar)|
---|---|---|
|Objekt-ID| GUID| 128|
|Objektstorlek| QWORD| 64|
|Antal rubrikobjekt| DWORD| 32|
|Reserverad1| BYTE| 8|
|Reserverad2| BYTE| 8|

#### ASF-dataobjekt på toppnivå

Alla digitala mediadata för en ASF-fil finns i dataobjektet och lagras i form av ASF-datapaket. Varje datapaket har en fast längd och innehåller data för en eller flera digitala mediaströmmar.

#### ASF-indexobjekt på toppnivå

ASF-indexobjekt på toppnivå har följande två typer:

* `Simple Index Object` - Innehåller ett tidsbaserat index över videodata i en ASF-fil. Tidsintervallet mellan indexposter är konstant och lagras i det enkla indexobjektet.
* `Indexobjekt` - hänvisar till Indexobjektet, Media Object Index Object och Timecode Index Object, vars format är liknande. Precis som det enkla indexobjektet indexeras indexobjektet efter tid med ett fast tidsintervall men är inte begränsat till videoströmmar.

## Referenser

* [ASF-filformat - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [QuickTime File Format - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

