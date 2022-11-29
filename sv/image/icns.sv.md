{
  "date" : "2021-06-29",
  "keywords" :[ "ICNS", "tillägg", "fil", "format", "bild", "Apple Icon Image", "macOS", "Apple", "Icon" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - Apple Icon Image",
  "description":"Läs mer om ICNS-filformat och API:er som kan skapa och öppna ICNS-filer.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Vad är en ICNS fil? ##

Ett ikonformat som används av macOS-program kallas en ICNS-fil. Den tillåter 1-bitars och 8-bitars alfaband och sparar en eller flera bilder, vanligtvis gjorda av [PNG](/sv/image/png)-dokument. Programikonen i macOS-webbläsaren och gränssnittet visas med ICNS-filer.

Baserat på platsen kan samma stilikon ha flera inställningar. ICNS-formatet har genomgått många förändringar och har utvecklats till den punkt där det nu kan användas som grund för olika kompatibla format. Här är några andra viktiga punkter du behöver veta:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource och Mac OS icons Resource är några av de andra namnen.
* För ikoninformation används en källa i resursgrenen.
* I de flesta fall innehåller en fil många bilder. 1612 pixlar i kvadrat och 1024, 512, 256, 128, 48, 32 och 16 pixlar i kvadrat stöds bildstorlekar.


## ICNS filformat ##

ICNS-dataformatet är en kapsel för en eller flera bilder, som stöder 1-bitars band och många bildtillstånd.
Operativsystemet kan ändra storlek på ikonbilder för att passa den önskade skärmstorleken. De större ikonbilderna sparas vanligtvis som [JPEG](/sv/image/jpeg/) 2000- eller [PNG](/sv/image/png)-filer. En typ av både komprimerade och okomprimerade ICNS-filer är möjlig.

En rubrik och binära ikondata utgör strukturen för en ICNS-fil. Rubriken innehåller 8 byte med data, varav fyra är den magiska bokstaven och fyra av dem är filens längd. Typen och storleken för varje ikonbild lagras i ikondatasektionen, som följs av binära bilddata. Bildstorleken bestämmer den binära sektionens storlek.

## Teknisk specifikation ##

### Rubrik ###

|Offset|Storlek|Mål
---|---|---|
|0|4|Magisk bokstavlig, måste vara "icns" (0x69, 0x63, 0x6e, 0x73)
|4|4|Filens längd, i byte, msb först


### Ikondata ###

|Offset|Storlek|Mål
---|---|---|
|0|4|Ikontyp
|4|4|Längd på data, i byte (inklusive typ och längd), msb först
|8|Variabel|Ikondata

### Kompression ###

Pixeldata komprimeras till viss del. 32-bitars ("is32", "il32", "ih32", "it32") och ARGB ("ic04", "ic05") pixlar komprimeras ofta (per kanal) på liknande sätt som PackBits.

|Lead Value|Svansbyte|Resultat (okomprimerat)
---|---|---|
|0 - 127|1 - 128|1 - 128 byte
|128 - 255|1 Byte|3 - 130 kopior

## Referens ##

* [ICNS - Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

