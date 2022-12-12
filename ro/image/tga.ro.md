{
  "date" : "2019-10-11",
  "keywords" :[ "fișier tga", "format fișier tga", "ce este un fișier tga", "fișier", "exemplu tga", "extensie fișier tga", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fișier TGA - Un fișier de imagine grafică TARGA",
  "description":"Aflați despre formatul de fișier TGA și despre API-urile care pot crea și deschide fișiere TGA.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier TGA?

Un fișier cu extensia .tga este un format grafic raster și a fost creat de Truevision Inc. A fost proiectat pentru plăcile TARGA (Truevision Advanced Raster Adapter) și a oferit suport pentru afișaj Highcolor/truecolor pentru computerele compatibile IBM. Suportă 8, 16, 24 și 32 de biți per pixel și canal alfa de 8 biți. De asemenea, acceptă compresia RLE fără pierderi care poate fi aplicată pentru a reduce dimensiunea imaginii. Fotografiile și texturile digitale folosesc formatul de imagine TGA.

## Scurt istoric

Formarea formatului de fișier TGA a luat ființă în 1984 de către AT&T EPICenter (extras ulterior și format ca o entitate independentă cunoscută sub numele de Truevision) care lucra la comercializarea noilor tehnologii dezvoltate de AT&T pentru bufferele de cadre color. EPICenter lucra deja la primele două carduri, VDA (Video Display Adapter) și ICB (placă de captare a imaginii) pentru care lucrarea pe două tipuri de fișiere, .vda și .icb, era deja în proces. Aceste formate de fișiere au fost codificate și a fost introdus un format de fișier specific mai puțin larg TGA. TGA a fost o extensie a ceea ce era deja în uz și a furnizat informații precum lățimea, înălțimea, adâncimea pixelilor, harta de culori asociată și originea imaginii.

Versiunea 2.0 a TGA, publicată în 1989, a încorporat mai multe caracteristici îmbunătățite, cum ar fi:

* Miniaturi
* Canal alfa
* Valoare Gamma
* Metadate textuale

Printre principalii contribuitori la versiunea 2.0 a TGA se numără Shawn Steiner, Kevin Fiedly și David Spoelstra de la Truevision.

## Specificații de format de fișier TGA TARGA

Un fișier TGA este format din 2 părți principale:

* Antet
* Informații despre pixeli de culoare

Toate valorile dintr-un fișier TGA sunt în littl-endian conform specificațiilor de format.

### Antet TGA

Antetul unui fișier TGA este format din următoarele 5 câmpuri.

|Nr. câmp|Lungime |Nume câmp |Descriere|
---|---|---|---|
|1| 1 octet |lungimea ID| Lungimea câmpului ID imagine (0-255)|
|2| 1 octet |Tip hartă color| Dacă o hartă de culori este inclusă (0 - indică faptul că nu sunt incluse date de hartă de culori cu această imagine. 1 - indică faptul că o hartă de culori este inclusă cu această imagine.)|
|3| 1 octet |Tipul imaginii| Tipuri de compresie și culoare (0- Nu sunt incluse date de imagine. 1- Necomprimat, Imagine colorată, 2- Necomprimată, Imagine color adevărată, 9- Lungime codificată, Imagine color mapată, 11- Cod lungime, Imagine alb-negru )|
|4| 5 octeți |Specificație hartă de culori| Descrie harta de culori|
|5| 10 octeți |Specificație imagine| Dimensiunile și formatul imaginii|

### Date despre hartă de imagine și culoare

|Câmp nr. |Lungime |Câmp |Descriere|
---|---|---|---|
|6 |Din câmpul lungime ID imagine| ID imagine| Câmp opțional care conține informații de identificare|
|7 |Din câmpul de specificare a hărții de culori| Date hartă color| Tabel de căutare care conține datele hărții de culori|
|8 |Din câmpul de specificare a imaginii| Date imagini| Stocat conform descriptorului de imagine|

### Zona pentru dezvoltatori (Opțional)

Versiunea TGA 2.0 oferă suport pentru îmbunătățiri/extra-uri suplimentare pe care mulți dezvoltatori doreau să stocheze mai multe informații. Informația este opțională, astfel încât dacă un decodor TGA nu este capabil să o interpreteze, va fi ignorată.

### Zona de extensie (Opțional)

|Câmp nr.| Lungime| Câmp |Descriere|
---|---|---|---|
|10| 2 octeți |Dimensiunea extensiei |Dimensiunea în octeți a zonei de extensie, întotdeauna 495|
|11| 41 de octeți| Numele autorului |Numele autorului. Dacă nu sunt utilizați, octeții trebuie setați la NULL (\0) sau spații|
|12| 324 de octeți| Comentariu autor| Un comentariu, organizat în patru rânduri, fiecare constând din 80 de caractere plus un NULL|
|13| 12 octeți| Marca dată/ora |Data și ora la care a fost creată imaginea|
|14| 41 de octeți| ID job||
|15| 6 octeți| Timpul de lucru| Ore, minute și secunde petrecute creând fișierul (pentru facturare etc.)|
|16| 41 de octeți| ID software |Aplicația care a creat fișierul.|
|17| 3 octeți| Versiune software ||
|18| 4 octeți| Culoarea cheii ||
|19| 4 octeți| Raport de aspect al pixelilor ||
|20| 4 octeți| Valoare gamma ||
|21| 4 octeți| Offset de corecție a culorii |Numărul de octeți de la începutul fișierului până la tabelul de corecție a culorilor, dacă este prezent|
|22| 4 octeți| timbru poștal | Numărul de octeți de la începutul fișierului până la imaginea timbrului poștal, dacă este prezent|
|23| 4 octeți| offset linie de scanare| Numărul de octeți de la începutul fișierului până la tabelul cu linii de scanare, dacă este prezent|
|24| 1 octet| Tip de atribute| Specifică canalul alfa|

### Subsol fișier (opțional)

Ultimii 26 de octeți ai fișierului reprezintă subsolul, ceea ce, dacă este prezent, înseamnă că este probabil un fișier TGA versiunea 2.

|Câmp Nr.| Lungime| Câmp| Descriere|
---|---|---|---|
|28| 4 octeți| Compensare extensie| Offset în octeți de la începutul fișierului|
|29| 4 octeți| Offset zona dezvoltatorului| Offset în octeți de la începutul fișierului|
|30| 16 octeți| Semnătura| Conține „TRUEVISION-XFILE”|
|31| 1 octet| | Conține „.”|
|32| 1 octet| | Conține NULL|


## Referințe

* [Specificații de format de fișier TGA 2.0](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [TGA de Wikipedia](https://en.wikipedia.org/wiki/Truevision_TGA)

