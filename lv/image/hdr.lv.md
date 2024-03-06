{
  "date": "2022-07-21",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDR faila formāts — kas ir HDR attēla fails?",
  "description": "Uzziniet par HDR failu formātu un API, kas var izveidot un atvērt HDR failus.",
  "linktitle": "HDR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-hd-lvr"
}
},
  "lastmod": "2022-07-21"
}

## Kas ir HDR fails?

HDR fails ir augsta dinamiskā diapazona (HDR) rastra attēla faila formāts digitālo kameru fotoattēlu glabāšanai. Tas ļauj fotoattēlu redaktoriem uzlabot to digitālo attēlu krāsu un spilgtumu, kuriem ir ierobežots dinamiskais diapazons. Šī modifikācija var uzlabot spilgtumu ap stūriem, kā rezultātā attēls ir tuvu dabiskajam. HDR faili parasti tiek saglabāti kā 32 bitu rastra attēli. Adobe Photoshop var izveidot un atvērt HDR failus.

HDR faili ir pazīstami arī kā HDRI.

## HDR faila formāts — vairāk informācijas

HDR faila formāts ir balstīts uz sākotnējo Radiance Picture (.pic) faila formātu. HDR faila pikseļu dati parasti tiek glabāti nesaspiesti, bet dažos gadījumos tie tiek saspiesti, izmantojot vienkāršu darbības garuma kodēšanas sistēmu.

### HDR faila struktūra

HDR attēla fails sastāv no šādām trim sadaļām:

 * **Galvene:** HDR fails tiek identificēts pēc pirmajiem attēla faila baitiem, piemēram, #?RADIANCE.
 * **Izšķirtspējas virkne:** galvenei seko viena izšķirtspējas rinda, kas sastāv no 4 vērtībām; X un Y etiķete, kam seko vesela skaitliska vērtība. X un Y secība norāda uz rotāciju. X un Y kombinācija ar pozitīvām un negatīvām vērtībām aptver visu iespējamo attēla orientāciju un rotācijas.
 * **Pikseļu dati:** HDR faila pikseļu dati ir nesaspiesti vai saspiesti, izmantojot standarta darbības garuma kodējumu.

## Atvērtā koda HDR/HDRI API

 * **[imageinfo](https://github.com/xiaozhuai/imageinfo)** — starpplatformu īpaši ātra vienas galvenes [C++](/programming/cpp/) bibliotēka, lai iegūtu attēla izmēru un formātu bez ielādes/dekodēšanas.
 * **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** — rūsas bibliotēka, lai iegūtu attēla izmēru un formātu bez ielādes/dekodēšanas. Atbalsta [.avif](/image/avif/), [.bmp](/image/bmp/), [.cur](/image/cur/), [.dds](/image/dds/), [ .gif](/image/gif/), hdr (pic), [heic (heif)](/image/heic/), [.icns](/image/icns/), [.ico](/image/ico/), [.jp2](/image/jp2/), [jpeg (jpg)](/image/jpeg/), [jpx](/image/jpx/), ktx, [png](/image/png/), [psd](/image/psd/), qoi, tga, tiff (tif) un webp.
 * **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** — HdrHistogrammas Java ieviešana.

## Atsauces

 * [Radiance HDR](http://paulbourke.net/dataformats/pic/)
 * [imageinfo](https://github.com/xiaozhuai/imageinfo)

