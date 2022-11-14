{
  "date" : "2019-10-11",
  "keywords" :[ "webp-bestand", "webp-bestandsindeling", "wat is een webp-bestand", "bestand", "webp-voorbeeld", "webp-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP - Google Raster Image Bestandsformaat",
  "description":"Meer informatie over WEBP-bestandsindeling en API's die WEBP-bestanden kunnen maken en openen.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een WEBP-bestand?

WebP, geïntroduceerd door Google, is een modern rasterwebafbeeldingsbestandsformaat dat is gebaseerd op lossless en lossy compressie. Het biedt dezelfde beeldkwaliteit terwijl het beeldformaat aanzienlijk wordt verkleind. Aangezien de meeste webpagina's afbeeldingen gebruiken als effectieve weergave van gegevens, resulteert het gebruik van WebP-afbeeldingen in webpagina's in sneller laden van webpagina's. Volgens Google zijn WebP-afbeeldingen zonder verlies 26% kleiner in vergelijking met [PNG's](/nl/image/png/), terwijl WebP-afbeeldingen met verlies 25-34% kleiner zijn dan vergelijkbare [JPEG](/nl/image/jpeg/)-afbeeldingen. Afbeeldingen worden vergeleken op basis van de Structural Similarity (SSIM) -index tussen WebP en andere afbeeldingsbestandsindelingen. WebP is een zusterproject van het [WebM](https://en.wikipedia.org/wiki/WebM) multimediacontainerformaat.

## Overzicht van WebP-functies ##

WebP-afbeeldingen gebruiken het compressieproces op basis van de voorspelling van pixels uit hun omringende blokken, wat resulteert in pixels die meerdere keren in één bestand kunnen worden gebruikt. Het ondersteunt geanimeerde afbeeldingen en zal naar verwachting in de toekomst meer functies ondersteunen. Google heeft de broncode [online](https://developers.google.com/speed/webp/download) voor zijn encoder en decoder beschikbaar gesteld, zodat deze waar nodig kan worden gebruikt. De WebP-afbeelding biedt ondersteuning voor:

* **Compressie met verlies:** De compressie met verlies is gebaseerd op [VP8](http://en.wikipedia.org/wiki/VP8) keyframe-codering. VP8 is een videocompressieformaat gemaakt door On2 Technologies als opvolger van de VP6- en VP7-formaten.
* **Lossless-compressie:** Het lossless-compressieformaat is ontwikkeld door het WebP-team.
* **Transparantie:** 8-bits alfakanaal is handig voor grafische afbeeldingen. Het alfakanaal kan samen met lossy RGB worden gebruikt, een functie die momenteel niet beschikbaar is met een ander formaat.
* **Animatie:** Het ondersteunt geanimeerde afbeeldingen in ware kleuren.
* **Metadata:** Het kan EXIF- en XMP-metadata bevatten (bijvoorbeeld gebruikt door camera's).
* **Kleurprofiel:** Het kan een ingesloten ICC-profiel hebben.

Lossy WebP-compressie gebruikt voorspellende codering om een afbeelding te coderen, dezelfde methode die wordt gebruikt door de VP8-videocodec om keyframes in video's te comprimeren. Voorspellende codering gebruikt de waarden in aangrenzende pixelblokken om de waarden in een blok te voorspellen en codeert vervolgens alleen het verschil.

Lossless WebP-compressie maakt gebruik van reeds geziene beeldfragmenten om nieuwe pixels exact te reconstrueren. Het kan ook een lokaal palet gebruiken als er geen interessante overeenkomst wordt gevonden.

## Bestandsformaat ##

Het WebP-bestandsformaat is gebaseerd op het RIFF-documentformaat (resource interchange file format). De WebP-container biedt ondersteuning voor andere functies dan alleen een enkele afbeelding die is gecodeerd als een VP8-sleutelframe. Het basiselement van een RIFF-bestand is een chunk die bestaat uit:


|Veld|Beschrijving
---|---|
|Chunk FourCC: 32 bits|ASCII-code van vier tekens gebruikt voor chunk-identificatie
|Chunkgrootte: 32 bits (uint32)|De grootte van de chunk zonder dit veld, de chunk-ID of opvulling
|Chunk Payload: Chunk Size bytes|De data-payload. Als Chunk Size oneven is, wordt een enkele opvulbyte ~-~- die 0 ~-~- moet zijn toegevoegd
|ChunkHeader ('ABCD')|Wordt gebruikt om de FourCC- en Chunk Size-header van individuele chunks te beschrijven, waarbij 'ABCD' de FourCC is voor de chunk. De grootte van dit element is 8 bytes.

### WebP-koptekst ###

De header van een WebP-bestand is als volgt:

* RIFF Header - 32 bits die de ASCII-tekens 'R' 'I' 'F' 'F' vertegenwoordigen
* Bestandsgrootte - 32 bits (uint32) die de grootte van het bestand in bytes weergeven vanaf offset 8. De maximale waarde van dit veld is 2^32 minus 10 bytes en dus is de grootte van het hele bestand maximaal 4GiB minus 2 bytes .
* 'WEBP' - 32 bits die de ASCII-tekens 'W' 'E' 'B' 'P' vertegenwoordigen

### Bestandsindeling met verlies ###

WebP-afbeeldingen gebruiken de bestandsindeling met verlies als de afbeelding is gebaseerd op codering met verlies en geen geavanceerde/uitgebreide functies vereist, zoals transparantie, animatie, alfa, enz. Afbeeldingen met verlies zijn kleiner en worden ook door de oudere toepassingen ondersteund.

Het WebP-bestand bestaat in dit geval uit:

* 12 bytes WebP-bestandskop
* VP8 Chunk

De [VP8 Data Format and Decoding Guide](https://tools.ietf.org/html/rfc6386) illustreert de VP8 bitstream formaatspecificaties.

### Bestandsformaat zonder verlies ###

Deze lay-out wordt gebruikt wanneer de afbeelding is gebaseerd op lossless codering en er geen behoefte is aan de geavanceerde functies van het externe formaat. Oudere applicaties kunnen dergelijke bestanden mogelijk niet lezen.

Het WebP-bestand bestaat in dit geval uit:

* 12 bytes WebP-bestandskop
* VP8L Brok

## Referenties ##

* [WebP-ontwikkelaarsreferentie - door Google](https://developers.google.com/speed/webp/)
* [WebP-bestandsindeling - door Wikipedia](https://en.wikipedia.org/wiki/WebP)

