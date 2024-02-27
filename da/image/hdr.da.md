{
  "date": "2022-07-21",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDR-filformat - Hvad er en HDR-billedfil?",
  "description": "Lær om HDR-filformat og API'er, der kan oprette og åbne HDR-filer.",
  "linktitle": "HDR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-hd-dar"
}
},
  "lastmod": "2022-07-21"
}

## Hvad er en HDR fil?

En HDR-fil er et HDR-rasterbilledfilformat (High Dynamic Range) til lagring af digitale kamerafotos. Det giver fotoredigerere mulighed for at forbedre farven og lysstyrken på digitale billeder, der har begrænset dynamisk rækkevidde. Denne ændring kan forbedre lysstyrken rundt om hjørnerne, hvilket resulterer i et tæt på naturligt billede. HDR-filer gemmes normalt som 32-bit rasterbilleder. Adobe Photoshop kan oprette og åbne HDR-filer.

HDR-filer er også kendt som HDRI.

## HDR-filformat - flere oplysninger

HDR-filformatet er baseret på det originale Radiance Picture (.pic) filformat. En HDR-fils pixeldata gemmes normalt ukomprimeret, men i nogle tilfælde komprimeres de ved hjælp af et ligetil kørselslængdekodningssystem.

### HDR-filstruktur

En HDR-billedfil består af følgende tre sektioner:

 * **Overskrift:** En HDR-fil identificeres af de første bytes i billedfilen, dvs. #?RADIANCE.
 * **Opløsningsstreng:** Overskriften efterfølges af en enkelt opløsningslinje, der består af 4 værdier; en X- og Y-mærke hver efterfulgt af en numerisk heltalsværdi. Rækkefølgen af X og Y angiver rotation. Kombinationen af X og Y med positive og negative værdier dækker alle mulige billedretninger og rotationer.
 * **Pixeldata:** Pixeldataene for en HDR-fil er enten ukomprimeret eller komprimeret ved hjælp af en standard kørselslængdekodning.

## Open Source HDR/HDRI API'er

 * **[imageinfo](https://github.com/xiaozhuai/imageinfo)** - Superhurtigt enkelt header-bibliotek på tværs af platforme [C++](/programming/cpp/) for at få billedstørrelse og -format uden indlæsning/afkodning.
 * **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Rustbibliotek for at få billedstørrelse og -format uden indlæsning/afkodning. Understøtter [.avif](/image/avif/), [.bmp](/image/bmp/), [.cur](/image/cur/), [.dds](/image/dds/), [ .gif](/image/gif/), hdr (pic), [heic (heif)](/image/heic/), [.icns](/image/icns/), [.ico](/image/ ico/), [.jp2](/image/jp2/), [jpeg (jpg)](/image/jpeg/), [jpx](/image/jpx/), ktx, [png](/image/ png/), [psd](/image/psd/), qoi, tga, tiff (tif) og webp.
 * **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - Java-implementering af HdrHistogram.

## Referencer

 * [Radiance HDR](http://paulbourke.net/dataformats/pic/)
 * [imageinfo](https://github.com/xiaozhuai/imageinfo)

