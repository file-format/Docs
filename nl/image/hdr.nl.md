{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR-bestandsindeling - Wat is een HDR-beeldbestand?",
  "description":"Meer informatie over HDR-bestandsindelingen en API's die HDR-bestanden kunnen maken en openen.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## Wat is een HDR-bestand?

Een HDR-bestand is een High Dynamic Range (HDR) rasterafbeeldingsbestandsindeling voor het opslaan van foto's van digitale camera's. Hiermee kunnen foto-editors de kleur en helderheid van digitale afbeeldingen met een beperkt dynamisch bereik verbeteren. Deze aanpassing kan de helderheid rond de hoeken verbeteren, wat resulteert in een bijna natuurlijk beeld. HDR-bestanden worden meestal opgeslagen als 32-bits rasterafbeeldingen. Adobe Photoshop kan HDR-bestanden maken en openen.

HDR-bestanden worden ook wel HDRI genoemd.

## HDR-bestandsindeling - Meer informatie

Het HDR-bestandsformaat is gebaseerd op het originele Radiance Picture-bestandsformaat (.pic). De pixelgegevens van een HDR-bestand worden meestal ongecomprimeerd opgeslagen, maar in sommige gevallen worden ze gecomprimeerd met behulp van een eenvoudig coderingssysteem voor runlengte.

### HDR-bestandsstructuur

Een HDR-beeldbestand bestaat uit de volgende drie secties:

* **Header:** Een HDR-bestand wordt geïdentificeerd door de eerste bytes in het afbeeldingsbestand, dwz "#?RADIANCE".
* **Resolutiereeks:** De koptekst wordt gevolgd door een enkele resolutieregel die uit 4 waarden bestaat; een X- en Y-label, elk gevolgd door een numeriek geheel getal. De volgorde van de X en Y geeft rotatie aan. De combinatie van X en Y met positieve en negatieve waarden dekt alle mogelijke beeldoriëntatie en rotaties.
* **Pixelgegevens:** De pixelgegevens van een HDR-bestand zijn niet gecomprimeerd of gecomprimeerd met behulp van een standaard run-length-codering.

## Open-source HDR/HDRI-API's

* **[imageinfo](https://github.com/xiaozhuai/imageinfo)** - Cross-platform supersnelle single header [C++](/nl/programming/cpp/) bibliotheek om de afbeeldingsgrootte en het formaat te krijgen zonder te laden/decoderen.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Roest bibliotheek om de afbeeldingsgrootte en het formaat te krijgen zonder te laden/decoderen. Ondersteunt [.avif](/nl/image/avif/), [.bmp](/nl/image/bmp), [.cur](/nl/image/cur/), [.dds](/nl/image/dds/), [. gif](/nl/image/gif/), hdr (pic), [heic (heif)](/nl/image/heic/), [.icns](/nl/image/icns/), [.ico](/nl/image/ico /), [.jp2](/nl/image/jp2/), [jpeg (jpg)](/nl/image/jpeg/), [jpx](/nl/image/jpx/), ktx, [png](/nl/image/png /), [psd](/nl/image/psd/), qoi, tga, tiff (tif) en webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - Java-implementatie van HdrHistogram.

## Referenties

* [Straling HDR](http://paulbourke.net/dataformats/pic/)
* [afbeeldingsinfo](https://github.com/xiaozhuai/imageinfo)

