{
  "date" : "2019-10-11",
  "keywords" :[ "fișier webp", "format fișier webp", "ce este un fișier webp", "fișier", "exemplu webp", "extensie fișier webp", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP – Google Raster Image File Format",
  "description":"Aflați despre formatul de fișier WEBP și despre API-urile care pot crea și deschide fișiere WEBP.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier WEBP?

WebP, introdus de Google, este un format de fișier imagine web raster modern care se bazează pe compresie fără pierderi și cu pierderi. Oferă aceeași calitate a imaginii în timp ce reduce considerabil dimensiunea imaginii. Deoarece majoritatea paginilor web folosesc imagini ca reprezentare eficientă a datelor, utilizarea imaginilor WebP în paginile web are ca rezultat încărcarea mai rapidă a paginilor web. Conform Google, imaginile WebP fără pierderi sunt cu 26% mai mici în comparație cu [PNG](/ro/image/png/), în timp ce imaginile WebP cu pierderi sunt cu 25-34% mai mici decât imaginile [JPEG](/ro/image/jpeg/) comparabile. Imaginile sunt comparate pe baza indexului de similaritate structurală (SSIM) între WebP și alte formate de fișiere imagine. WebP este un proiect partener al formatului de container multimedia [WebM](https://en.wikipedia.org/wiki/WebM).

## Prezentare generală a funcțiilor WebP ##

Imaginile WebP folosesc procesul de compresie bazat pe predicția pixelilor din blocurile din jur, rezultând pixeli care urmează să fie utilizați de mai multe ori într-un singur fișier. Acceptă imagini animate și este de așteptat să accepte mai multe funcții în viitor. Google a pus la dispoziție codul sursă [online](https://developers.google.com/speed/webp/download) pentru codificatorul și decodorul său, astfel încât să fie utilizat acolo unde este necesar. Imaginea WebP oferă suport pentru:

* **Compresie cu pierderi:** Compresia cu pierderi se bazează pe codificarea cadrului cheie [VP8](http://en.wikipedia.org/wiki/VP8). VP8 este un format de compresie video creat de On2 Technologies ca succesor al formatelor VP6 și VP7.
* **Compresie fără pierderi:** Formatul de compresie fără pierderi este dezvoltat de echipa WebP.
* **Transparență:** canalul alfa de 8 biți este util pentru imaginile grafice. Canalul Alpha poate fi folosit împreună cu RGB cu pierderi, o caracteristică care nu este disponibilă în prezent cu niciun alt format.
* **Animation:** acceptă imagini animate în culori reale.
* **Metadate:** poate avea metadate EXIF și XMP (utilizate de camere, de exemplu).
* **Profil de culoare:** Poate avea un profil ICC încorporat.

Compresia Lossy WebP folosește codarea predictivă pentru a codifica o imagine, aceeași metodă folosită de codecul video VP8 pentru a comprima cadrele cheie din videoclipuri. Codarea predictivă folosește valorile din blocurile vecine de pixeli pentru a prezice valorile dintr-un bloc și apoi codifică doar diferența.

Compresia WebP fără pierderi folosește fragmente de imagine deja văzute pentru a reconstrui exact noii pixeli. De asemenea, poate folosi o paletă locală dacă nu se găsește o potrivire interesantă.

## Tipul fisierului ##

Formatul de fișier WebP se bazează pe formatul de document RIFF (resource interchange file format). Containerul WebP oferă suport pentru funcții de mai sus decât de a conține doar o singură imagine codificată ca cadru cheie VP8. Elementul de bază al unui fișier RIFF este o bucată care constă din:


|Câmp|Descriere
---|---|
|Chink FourCC: 32 de biți|Cod ASCII din patru caractere utilizat pentru identificarea blocurilor
|Dimensiunea fragmentului: 32 de biți (uint32)|Dimensiunea fragmentului fără a include acest câmp, identificatorul fragmentului sau umplutura
|Încărcare utilă porțiune: octeți dimensiunea cantității|Sarcina utilă a datelor. Dacă Chunk Size este impară, se adaugă un singur octet de completare ~-~- care ar trebui să fie 0 ~-~-
|ChunkHeader ('ABCD')|Folosit pentru a descrie antetul FourCC și Chunk Size al fragmentelor individuale, unde 'ABCD' este FourCC pentru bucată. Dimensiunea acestui element este de 8 octeți.

### Antet WebP ###

Antetul unui fișier WebP este următorul:

* Antet RIFF - 32 de biți reprezentând caracterele ASCII „R” „I” „F” „F”
* Dimensiunea fișierului - 32 de biți (uint32) reprezentând dimensiunea fișierului în octeți începând cu offset-ul 8. Valoarea maximă a acestui câmp este 2^32 minus 10 octeți și astfel dimensiunea întregului fișier este de cel mult 4GiB minus 2 octeți .
* „WEBP” - 32 de biți reprezentând caracterele ASCII „W” „E” „B” „P”

### Format fișier cu pierdere ###

Imaginile WebP folosesc formatul de fișier cu pierderi dacă imaginea se bazează pe codificare cu pierderi și nu necesită caracteristici avansate/extinse, cum ar fi transparență, animație, alfa etc. Imaginile cu pierderi sunt mai mici și sunt acceptate și de aplicațiile mai vechi.

Fișierul WebP, în acest caz, constă din:

* Antet fișier WebP de 12 octeți
* VP8 Chunk

[VP8 Data Format and Decoding Guide](https://tools.ietf.org/html/rfc6386) ilustrează specificațiile formatului VP8 bitstream.

### Format de fișier fără pierderi ###

Acest aspect este utilizat atunci când imaginea se bazează pe codificare fără pierderi și nu este nevoie de caracteristicile avansate oferite de formatul extern. Este posibil ca aplicațiile mai vechi să nu poată citi astfel de fișiere.

Fișierul WebP, în acest caz, constă din:

* Antet fișier WebP de 12 octeți
* VP8L Chunk

## Referințe ##

* [Referință pentru dezvoltatori WebP - De la Google](https://developers.google.com/speed/webp/)
* [Format de fișier WebP - După Wikipedia](https://en.wikipedia.org/wiki/WebP)

