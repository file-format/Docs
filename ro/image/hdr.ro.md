{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier HDR – Ce este un fișier imagine HDR?",
  "description":"Aflați despre formatul de fișier HDR și despre API-urile care pot crea și deschide fișiere HDR.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## Ce este un fișier HDR?

Un fișier HDR este un format de fișier imagine raster cu gamă dinamică înaltă (HDR) pentru stocarea fotografiilor camerei digitale. Permite editorilor foto să îmbunătățească culoarea și luminozitatea imaginilor digitale care au o gamă dinamică limitată. Această modificare poate îmbunătăți luminozitatea în jurul colțurilor, rezultând o imagine aproape naturală. Fișierele HDR sunt de obicei salvate ca imagini raster pe 32 de biți. Adobe Photoshop poate crea și deschide fișiere HDR.

Fișierele HDR sunt cunoscute și ca HDRI.

## Format de fișier HDR - Mai multe informații

Formatul de fișier HDR se bazează pe formatul original de fișier Radiance Picture (.pic). Datele de pixeli ale unui fișier HDR sunt de obicei stocate necomprimate, dar în unele cazuri sunt comprimate folosind un sistem simplu de codare a lungimii de rulare.

### Structura fișierului HDR

Un fișier de imagine HDR este format din următoarele trei secțiuni:

* **Header:** Un fișier HDR este identificat prin primii octeți din fișierul imagine, adică „#?RADIANCE”.
* **Șir de rezoluție:** Antetul este urmat de o singură linie de rezoluție care constă din 4 valori; o etichetă X și Y, fiecare urmată de o valoare întreagă numerică. Ordinea lui X și Y indică rotația. Combinația dintre X și Y cu valori pozitive și negative acoperă toate orientarea și rotațiile posibile ale imaginii.
* **Date pixeli:** Datele pixeli ale unui fișier HDR sunt fie necomprimate, fie comprimate utilizând o codificare standard a lungimii de rulare.

## API-uri HDR/HDRI open-source

* **[imageinfo](https://github.com/xiaozhuai/imageinfo)** - Bibliotecă cu antet unic super rapid [C++](/ro/programming/cpp/) pentru a obține dimensiunea și formatul imaginii fără încărcare/decodare.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Biblioteca Rust pentru a obține dimensiunea și formatul imaginii fără încărcare/decodare. Suportă [.avif](/ro/image/avif/), [.bmp](/ro/image/bmp), [.cur](/ro/image/cur/), [.dds](/ro/image/dds/), [. gif](/ro/image/gif/), hdr (pic), [heic (heif)](/ro/image/heic/), [.icns](/ro/image/icns/), [.ico](/ro/image/ico /), [.jp2](/ro/image/jp2/), [jpeg (jpg)](/ro/image/jpeg/), [jpx](/ro/image/jpx/), ktx, [png](/ro/image/png /), [psd](/ro/image/psd/), qoi, tga, tiff (tif) și webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - Implementarea Java a HdrHistogram.

## Referințe

* [Radiance HDR](http://paulbourke.net/dataformats/pic/)
* [imageinfo](https://github.com/xiaozhuai/imageinfo)

