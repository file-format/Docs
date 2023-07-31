{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR-filformat - Vad är en HDR-bildfil?",
  "description":"Läs mer om HDR-filformat och API:er som kan skapa och öppna HDR-filer.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## Vad är en HDR-fil?

En HDR-fil är ett rasterbildsformat (HDR) (High Dynamic Range) för lagring av digitalkamerafoton. Det tillåter fotoredigerare att förbättra färgen och ljusstyrkan på digitala bilder som har begränsat dynamiskt omfång. Denna modifiering kan förbättra ljusstyrkan runt hörnen, vilket resulterar i en naturlig bild. HDR-filer sparas vanligtvis som 32-bitars rasterbilder. Adobe Photoshop kan skapa och öppna HDR-filer.

HDR-filer är också kända som HDRI.

## HDR-filformat - Mer information

HDR-filformatet är baserat på det ursprungliga filformatet Radiance Picture (.pic). Pixeldata för en HDR-fil lagras vanligtvis okomprimerad, men i vissa fall komprimeras den med ett enkelt körlängdskodningssystem.

### HDR-filstruktur

En HDR-bildfil består av följande tre sektioner:

* **Rubrik:** En HDR-fil identifieras av de första byten i bildfilen, dvs. "#?RADIANCE".
* **Upplösningssträng:** Rubriken följs av en enda upplösningsrad som består av 4 värden; en X- och Y-etikett vardera följt av ett numeriskt heltalsvärde. Ordningen för X och Y indikerar rotation. Kombinationen av X och Y med positiva och negativa värden täcker alla möjliga bildorientering och rotationer.
* **Pixeldata:** Pixeldata för en HDR-fil är antingen okomprimerad eller komprimerad med en standardkörningslängdkodning.

## Open-Source HDR/HDRI API:er

* **[imageinfo](https://github.com/xiaozhuai/imageinfo )** - Supersnabbt bibliotek med enstaka rubriker över flera plattformar [C++](/sv/programming/cpp/) för att få bildstorlek och format utan att ladda/avkoda.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Rustbibliotek för att få bildstorlek och format utan att ladda/avkoda. Stöder [.avif](/sv/image/avif/), [.bmp](/sv/image/bmp/), [.cur](/sv/image/cur/), [.dds](/sv/image/dds/), [. gif](/sv/image/gif/), hdr (bild), [heic (heif)](/sv/image/heic/), [.icns](/sv/image/icns/), [.ico](/sv/image/ico /), [.jp2](/sv/image/jp2/), [jpeg (jpg)](/sv/image/jpeg/), [jpx](/sv/image/jpx/), ktx, [png](/sv/image/png /), [psd](/sv/image/psd/), qoi, tga, tiff (tif) och webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - Java-implementering av HdrHistogram.

## Referenser

* [Radiance HDR](http://paulbourke.net/dataformats/pic/)
* [bildinfo](https://github.com/xiaozhuai/imageinfo )

