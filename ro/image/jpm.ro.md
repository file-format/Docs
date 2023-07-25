{
  "date" : "2019-11-25",
  "keywords" :[ "fișier jpm", "format fișier jpm", "ce este un fișier jpm", "fișier", "exemplu jpm", "extensie fișier jpm", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPM - Format de fișier compus JPEG 2000",
  "description":"Aflați despre formatul de fișier JPM și despre API-urile care pot crea și deschide fișiere JPM.",
  "linktitle" : "JPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-08"
}

## Ce este un fișier JPM?

JPM se referă la sistemul de codare a imaginii JPEG 2000 Partea 6, care este utilizat pentru imaginea documentelor. Se bazează pe standardul de conținut raster mixt (ISO/IEC 16485) și conține imagini statice stratificate care utilizează JPEG 2000 și alte codificări. În plus față de propriile specificații, formatul de fișier JPM moștenește caracteristici de la părintele său, adică formatul de fișier [jp2](/ro/image/jp2/).

## Format de fișier JPM

Formatul de fișier JPM este definit de [ISO/IEC 15444-6:2003](https://www.iso.org/standard/61124.html) -- imaginea JPEG 2000 sistem de codare -- Partea 6: Format de fișier imagine compus. O imagine compusă poate conține imagini scanate, imagini sintetice sau ambele, necesitând o combinație de tonuri continue și metode de compresie pe două niveluri. Formatul de fișier JPM definește un model de compoziție care descrie metoda de combinare a mai multor imagini pentru a genera o imagine compusă utilizând modelul de imagini cu mai multe straturi Mixed Raster Content (MRC), definit în ITU-T T.44 | ISO/IEC 16485.

### Specificații JPM
Standardul de format de fișier JPM specifică ca acesta să fie un container binar pentru a reprezenta o imagine compusă prin care mai multe imagini pot fi combinate într-o singură imagine. Acesta stabilește mecanismul pentru gruparea mai multor imagini într-o ierarhie de obiecte de aspect, pagini și colecții de pagini pentru a stoca JPEG 2000 și alte formate de date de imagine comprimate. Formatul include mecanismul de încorporare a metadatelor (denumite adesea metadate structurale în proiectele bibliotecii digitale).

## Referințe

* [UIT-T Rec. T.805](https://www.itu.int/rec/T-REC-T.805/en)
* [ISO/IEC 15444-6:2013](https://www.iso.org/standard/61124.html)
* [Wikipedia:JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000)

