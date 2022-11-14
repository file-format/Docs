{
  "date" : "2019-10-11",
  "keywords" :[ "bmp-bestand", "bmp-bestandsformaat", "wat is een bmp-bestand", "bestand", "bmp-voorbeeld", "bmp-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Beeldbestandsindeling",
  "description":"Meer informatie over BMP-bestandsindeling en API's die BMP-bestanden kunnen maken en openen.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# Wat is een BMP-bestand? #

Bestanden met de extensie .BMP vertegenwoordigen Bitmap Image-bestanden die worden gebruikt om digitale bitmapafbeeldingen op te slaan. Deze afbeeldingen zijn onafhankelijk van de grafische adapter en worden ook wel apparaatonafhankelijke bitmap (DIB)-bestandsindeling genoemd. Deze onafhankelijkheid dient om het bestand op meerdere platforms te openen, zoals Microsoft Windows en Mac. Het BMP-bestandsformaat kan gegevens opslaan als tweedimensionale digitale afbeeldingen in zowel zwart-wit als kleurformaat met verschillende kleurdiepten.

## Specificaties BMP-bestandsindeling ##

Apparaatonafhankelijke bitmaps fungeren als hulpmiddel bij het uitwisselen van bitmaps tussen apparaten en applicaties. Vanwege de voortdurende evolutie van dit bestandsformaat, kan de informatie in de headers verschillen per versie van Bitmap. Een enkel bitmapbestand bestaat uit zowel vaste als variabele groottestructuren in een specifieke volgorde.

Structuren in een Bitmap-bestand zijn in de volgende volgorde gerangschikt:


|Structuur|Optioneel|Grootte|Doel
---|---|---|---|
|Bestandskop|Nee|14|Om algemene informatie over het bitmapafbeeldingsbestand op te slaan
|DIB Header|No|Fixed-Size|Om gedetailleerde informatie over de bitmapafbeelding op te slaan en het pixelformaat te definiëren
|Extra bitmaskers|Ja|12 of 16 bytes|Om het pixelformaat te definiëren
|Kleurenpalet|Semi-optioneel|Variabele grootte|Om kleuren te definiëren die worden gebruikt door de bitmapafbeeldingsgegevens
|Gap1|Ja|Variabele grootte|Structuuruitlijning
|Pixel Array|No|Variabele grootte|Pixelformaat wordt gedefinieerd door de DIB-header of Extra bitmaskers.
|Gap2|Ja|Variabele grootte|Structuuruitlijning
|ICC Kleurprofiel|Ja|Variabele grootte|Om het kleurprofiel voor kleurbeheer te definiëren

Wanneer een bitmapafbeelding in het geheugen wordt geladen, wordt het een DIB-structuur die door Windows wordt gebruikt via de GDI API. De bestandskop maakt geen deel uit van deze gegevensstructuur. De kleur kan ook bestaan uit 16-bits items die indexen vormen voor het palet waarnaar momenteel wordt verwezen in plaats van expliciete RGB-kleurdefinities. Laten we enkele hiervan in detail bekijken, vooral de koppen.

### Bitmapbestandskop ###

Een Bitmap File Header is vergelijkbaar met andere bestandsheaders die worden gebruikt om het bestand te identificeren. Aangezien er verschillende varianten van het BMP-bestandsformaat zijn, zijn de eerste 2 bytes van het BMP-bestandsformaat teken "B" en vervolgens teken "M" in ASCII-codering. Alle integer-waarden worden opgeslagen in little-endian-indeling.

|Offset hex|Offset dec|Grootte|Doel
---|---|---|---|
|00|0|2 bytes|Het headerveld dat wordt gebruikt om het BMP- en DIB-bestand te identificeren is 0x42 0x4D in hexadecimaal, hetzelfde als BM in ASCII. Het kan de volgende mogelijke waarden volgen.* **BM** – Windows 3.1x, 95, NT, ... etc. * **BA** – OS/2 struct bitmap-array * **CI** – OS/2 struct kleurpictogram * **CP** – OS/2 const-kleuraanwijzer * **IC** – OS/2-structpictogram * **PT** – OS/2-aanwijzer
|02|2|4 bytes|De grootte van het BMP-bestand in bytes
|06|6|2 bytes|Gereserveerd; werkelijke waarde hangt af van de toepassing die de afbeelding maakt
|08|8|2 bytes|Gereserveerd; werkelijke waarde hangt af van de toepassing die de afbeelding maakt
|0A|10|4 bytes|De offset, dwz het startadres, van de byte waar de bitmapafbeeldingsgegevens (pixelarray) te vinden zijn.

#### DIB header (bitmap informatie header) ####

De gedetailleerde informatie over de afbeelding wordt weergegeven door deze kop. Op basis van deze informatie wordt de toepassing bepaald die zal worden gebruikt om de afbeelding op het scherm weer te geven. Al dergelijke headers bevatten een DWORD-veld (32-bits), waarin hun grootte wordt gespecificeerd, zodat een toepassing gemakkelijk kan bepalen welke header in de afbeelding wordt gebruikt. Dit is voornamelijk te wijten aan het feit dat het DIB-formaat verschillende uitbreidingen heeft ondergaan. Hieronder volgt de DIB-header met de vermelde velden.

#### Kleurenpalet ####

Een BMP-kleurenpalet is een reeks structuren die de RGB-intensiteitswaarden van elke kleur in het kleurenpalet van een weergaveapparaat specificeren. Elke pixel in de bitmapgegevens slaat een enkele waarde op die als index in het kleurenpalet wordt gebruikt. De kleurinformatie die in het element bij die index is opgeslagen, specificeert de kleur van die pixel. De beschikbaarheid van kleur in een bitmapbestand varieert als volgt:

* Eén, 4 en 8-bit - zal naar verwachting altijd een kleurenpalet bevatten
* Zestien, 24 en 32-bits - bevatten nooit kleurenpaletten
* Zestien en 32-bits BMP-bestanden - bevatten maskerwaarden voor bitvelden in plaats van het kleurenpalet

#### Pixel-opslag ####

Bitmappixels worden opgeslagen als bits die zijn verpakt in rijen waarbij de grootte van elke rij wordt afgerond op een veelvoud van 4 bytes (een 32-bits DWORD) door opvulling. Het totale aantal bytes dat nodig is om de pixels van een afbeelding op te slaan, kan niet direct worden berekend door alleen de bits te tellen. Aangezien er sprake is van opvulling, is het effect van het afronden van de grootte van elke rij tot een veelvoud van 4 bytes vereist. Opvulbytes (niet noodzakelijk 0) moeten aan het einde van de rijen worden toegevoegd om de lengte van de rijen op een veelvoud van vier bytes te brengen. Wanneer de pixelarray in het geheugen wordt geladen, moet elke rij beginnen bij een geheugenadres dat een veelvoud van 4 is.

De afbeelding wordt eigenlijk beschreven door de 32-bits DWORDs-weergave van de pixelarray. Meestal worden pixels "bottom-up" opgeslagen, beginnend in de linkerbenedenhoek, van links naar rechts, en dan rij voor rij van onder naar boven in de afbeelding. Pixelformaten en hun implicaties zijn zoals hieronder vermeld:

* Het 1-bits per pixel (1bpp) formaat ondersteunt 2 verschillende kleuren (bijvoorbeeld: zwart en wit).
* Het 2-bits per pixel (2bpp) formaat ondersteunt 4 verschillende kleuren en slaat 4 pixels per 1 byte op, waarbij de meest linkse pixel zich in de twee meest significante bits bevindt. Elke pixelwaarde is een 2-bits index in een tabel van maximaal 4 kleuren.
* Het 4-bits per pixel (4bpp) formaat ondersteunt 16 verschillende kleuren en slaat 2 pixels per 1 byte op, waarbij de meest linkse pixel de meest significante nibble is. Elke pixelwaarde is een 4-bits index in een tabel van maximaal 16 kleuren.
* Het 8-bits per pixel (8bpp) formaat ondersteunt 256 verschillende kleuren en slaat 1 pixel per 1 byte op. Elke byte is een index in een tabel van maximaal 256 kleuren.
* Het 16-bits per pixel (16bpp) formaat ondersteunt 65536 verschillende kleuren en slaat 1 pixel op per 2-byte WOORD. Elk WOORD kan de alfa-, rode, groene en blauwe voorbeelden van de pixel definiëren.
* Het 24-bits pixelformaat (24bpp) ondersteunt 16.777.216 verschillende kleuren en slaat 1 pixelwaarde op per 3 bytes. Elke pixelwaarde definieert de rode, groene en blauwe voorbeelden van de pixel (8.8.8.0.0 in RGBAX-notatie). Specifiek, in de volgorde: blauw, groen en rood (8 bits per monster).
* Het 32-bits per pixel (32bpp) formaat ondersteunt 4.294.967.296 verschillende kleuren en slaat 1 pixel op per 4-byte DWORD. Elke DWORD kan de alfa-, rode, groene en blauwe voorbeelden van de pixel definiëren.

## Referenties ##

* [Windows MetaFile-indeling](http://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [BMP-bestandsindeling](https://en.wikipedia.org/wiki/BMP_file_format)

