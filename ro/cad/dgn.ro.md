{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "Fișier", "Format", "Deschidere", "Citește", "API", "MicroStation", "Sistem de proiectare grafică interactivă Intergraph"],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - MicroStation CAD Design File Format",
  "description" :"Aflați despre formatul de fișier DGN și despre API-urile care pot crea și deschide fișiere DGN.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## Ce este un fișier DGN?

Un fișier cu o extensie .dgn (Design) este un fișier de desen creat și susținut de aplicații CAD, cum ar fi MicroStation și Intergraph Interactive Graphics Design System. Este utilizat pentru crearea și salvarea proiectelor de construcții, cum ar fi autostrăzi, poduri și clădiri. Formatul este similar cu formatul de fișier [DWG](/ro/cad/dwg/) al Autodesk și este considerat concurentul său. Fișierele DNG pot fi salvate fie ca format de fișier standard Intergraph, fie ca DGN V8. DGN poate fi convertit în mai multe alte formate, cum ar fi DWG, [BMP](/ro/image/bmp/), [JPEG](/ro/image/jpeg/), [PDF](/ro/pdf/), [GIF](/ro/image/ gif/) și altele. Poate fi deschis cu Autodesk AutoCAD, Bentley View și Bentley Systems MicroStation, pe lângă alte aplicații software, cum ar fi versiunile Corel PaintShop Photo Pro și IMSI TurboCAD Deluxe.

## Format de fișier DGN V8

Un fișier DGN MicroStation V8 este compus din unul sau mai multe modele. Un model este un container pentru elemente. V8 DGN elimină toate constrângerile bazate pe format de fișier care erau prezente în versiunile anterioare ale MicroStation. Mai jos este o listă de îmbunătățiri ale formatului de fișier DGN.

* Limita numărului de niveluri dintr-un fișier DGN a fost eliminată, iar fiecare nivel este denumit și stocat ca element.
* Dimensiunea fizică maximă a fișierului DGN nu are nicio limitare și este limitată doar de sistemul de operare (cum ar fi limita NT este de 4 GB)
* Dimensiunea maximă a unui singur element este de 128 KB.
* Nu există limită pentru dimensiunea maximă a unei celule.
* Numele celulelor sunt limitate la aproximativ 500 de caractere.
* Nu există limită pentru numărul de referințe care pot fi atașate la un fișier DGN.
* Un șir de linii, o formă sau o curbă de punct poate avea până la 5000 de vârfuri.
* Nu există limită pentru numărul de componente dintr-un lanț complex sau o formă complexă.
* Nu există limită pentru numărul de grupuri grafice dintr-un fișier DGN.
* Gardul este paralel cu vederea în care este amplasat.
* O singură linie de text poate conține 65.535 de caractere.
* Nu există limită pentru dimensiunea maximă a unui nod text.
* Nu există limită pentru numărul de noduri text dintr-un fișier DGN.
* Fiecare element are un identificator unic de 64 de biți care nu se modifică pe parcursul ciclului de viață al elementului.
* Fiecare element are un marcaj de timp care indică ora celei mai recente modificări.

## Referințe

* [DNG - După Wikipedia](https://en.wikipedia.org/wiki/DGN)
* [OpenDNG](http://www.bentley.com/opendgn)
* [Format de fișier DGN MicroStation V8](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

