{
  "date" : "2019-10-11",
  "keywords" :[ "webp-fil", "webp-filformat", "vad är en webp-fil", "fil", "webp-exempel", "webp-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP - Google Raster Image File Format",
  "description":"Läs mer om WEBP-filformat och API:er som kan skapa och öppna WEBP-filer.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är WEBP fil?

WebP, introducerat av Google, är ett modernt rasterwebbbildsfilformat som är baserat på förlustfri och förlustfri komprimering. Den ger samma bildkvalitet samtidigt som den minskar bildstorleken avsevärt. Eftersom de flesta webbsidor använder bilder som effektiv representation av data, resulterar användningen av WebP-bilder på webbsidor i snabbare inläsning av webbsidor. Enligt Google är WebP-förlustfria bilder 26 % mindre i storlek jämfört med [PNGs](/sv/image/png/), medan WebP-förlustfria bilder är 25-34 % mindre än jämförbara [JPEG](/sv/image/jpeg/)-bilder. Bilder jämförs baserat på SSIM-indexet (Structural Similarity) mellan WebP och andra bildfilformat. WebP är ett systerprojekt i [WebM](https://en.wikipedia.org/wiki/WebM) multimediacontainerformat.

## WebP-funktionsöversikt ##

WebP-bilder använder komprimeringsprocessen baserat på förutsägelse av pixlar från deras omgivande block, vilket resulterar i att pixlar kan användas flera gånger i en enda fil. Den stöder animerade bilder och förväntas stödja fler funktioner i framtiden. Google har gjort källkoden tillgänglig [online](https://developers.google.com/speed/webp/download) för sin kodare och avkodare så att den kan användas vid behov. WebP-bilden ger stöd för:

* **Kompression med förlust:** Kompressionen med förlust är baserad på kodning för nyckelramen [VP8](https://en.wikipedia.org/wiki/VP8). VP8 är ett videokomprimeringsformat skapat av On2 Technologies som en efterföljare till VP6- och VP7-formaten.
* **Förlustfri komprimering:** Det förlustfria komprimeringsformatet är utvecklat av WebP-teamet.
* **Transparens:** 8-bitars alfakanal är användbar för grafiska bilder. Alfakanalen kan användas tillsammans med förlustfri RGB, en funktion som för närvarande inte är tillgänglig med något annat format.
* **Animation:** Det stöder animerade bilder i sanna färger.
* **Metadata:** Den kan ha EXIF- och XMP-metadata (används till exempel av kameror).
* **Färgprofil:** Den kan ha en inbäddad ICC-profil.

Lossy WebP-komprimering använder prediktiv kodning för att koda en bild, samma metod som används av VP8-videocodec för att komprimera nyckelbildrutor i videor. Prediktiv kodning använder värdena i angränsande pixelblock för att förutsäga värdena i ett block, och kodar sedan endast skillnaden.

Förlustfri WebP-komprimering använder redan sedda bildfragment för att exakt rekonstruera nya pixlar. Den kan också använda en lokal palett om ingen intressant matchning hittas.

## Filformat ##

WebP-filformatet är baserat på dokumentformatet RIFF (resource interchange file format). WebP-behållaren ger stöd för utöver funktioner än att bara innehålla en enda bild kodad som en VP8-nyckelram. Grundelementet i en RIFF-fil är en bit som består av:


|Fält|Beskrivning
---|---|
|Chunk FourCC: 32 bitar|ASCII fyrteckenkod som används för chunkidentifiering
|Chunk Size: 32 bits (uint32)|Storleken på chunken inklusive detta fält, chunk-identifieraren eller utfyllnad
|Chunk Payload: Chunk Size bytes|Datanyttolasten. Om Chunk Size är udda läggs en enda utfyllnadsbyte ~-~- som ska vara 0 ~-~- till
|ChunkHeader ('ABCD')|Används för att beskriva FourCC- och Chunk Size-huvudet för individuella chunks, där 'ABCD' är FourCC för chunken. Detta elements storlek är 8 byte.

### WebP Header ###

En WebP-filhuvud är följande:

* RIFF Header - 32 bitar som representerar ASCII-tecknen 'R' 'I' 'F' 'F'
* Filstorlek - 32 bitar (uint32) representerar storleken på filen i byte med start vid offset 8. Det maximala värdet för detta fält är 2^32 minus 10 byte och därmed är storleken på hela filen högst 4GiB minus 2 byte .
* 'WEBP' - 32 bitar som representerar ASCII-tecknen 'W' 'E' 'B' 'P'

### Lossy filformat ###

WebP-bilder använder filformatet med förlust om bilden är baserad på förlustkodning och inte kräver några avancerade/utökade funktioner som transparens, animera, alfa, etc. Förlustbilder är mindre och stöds även av de äldre programmen.

WebP-filen, i det här fallet, består av:

* 12 bytes WebP-filhuvud
* VP8 Chunk

[VP8 Data Format and Decoding Guide](https://tools.ietf.org/html/rfc6386) illustrerar specifikationerna för VP8-bitströmsformat.

### Förlustfritt filformat ###

Den här layouten används när bilden är baserad på förlustfri kodning och det inte finns något behov av de avancerade funktionerna i det externa formatet. Äldre program kanske inte kan läsa sådana filer dock.

WebP-filen, i det här fallet, består av:

* 12 bytes WebP-filhuvud
* VP8L Chunk

## Referenser ##

* [WebP Developer's Reference - By Google](https://developers.google.com/speed/webp/)
* [WebP-filformat - av Wikipedia](https://en.wikipedia.org/wiki/WebP)

