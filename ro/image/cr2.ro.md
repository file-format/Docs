{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier CR2 - Fișier imagine Canon Raw 2",
  "description":"Aflați despre formatul de fișier CR2 și despre API-urile care pot crea și deschide fișiere CR2.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Ce este un fișier CR2?

Un fișier CR2 (Camera RAW 2) este un fișier imagine RAW creat de camerele digitale Canon. Stochează datele originale de imagine, fără pierderi, neprocesate, capturate de cameră. Formatul de fișier CR2 a fost dezvoltat de Canon pentru camerele sale digitale și poate înregistra imagini de înaltă calitate de până la 14 biți RGB. Acest lucru produce imagini de înaltă calitate, cu suficient spațiu de postprocesare. Formatul de imagine CR2 a fost folosit de Canon în modelele lor de camere 350D, 20D și 1D. Fișierele CR2 sunt fișiere RAW și conțin informații suplimentare despre metadate, cum ar fi informații despre cameră, informații despre obiectiv, informații despre bracketing, balansul de alb și alte setări.

## Format de fișier CR2

Fișierele CR2 sunt stocate pe cardul de memorie al camerei ca fișiere binare în format de fișier proprietar Canon. Formatul de fișier CR2 a înlocuit formatul de fișier CRW utilizat inițial și a fost înlocuit ulterior cu formatul de fișier Canon RAW 3. Formatul de fișier CR2 se bazează pe specificațiile [TIFF](/ro/image/tiff/), care are 4 directoare de fișiere de imagine (IFD).

|Offset |Conținut |Comentariu|
---|---|---|
|0x0000 |Header |contine ordonarea octetilor, versiunea si offset-ul fata de imaginea RAW|
|calculat |IFD#0 |această parte conține secțiunea Exif, care conține secțiunea Makernotes.
Informații despre imaginea#0|
|computat |imagine#0 |versiune mică a imaginii (un sfert din dimensiunea originalului), comprimată în Jpeg|
|calculat |IFD#1 |Informații despre imaginea#1.|
|computat |imagine#1 |versiune mică a imaginii, comprimată în Jpeg|
|calculat |IFD#2 |Informații despre imaginea#2.|
|calculat |imagine#2 |versiune mică a imaginii, necomprimată|
|în antet| IFD#3| Informații despre imaginea#3, imaginea RAW la dimensiune completă|
|calculat |imagine#3 |Date imagini RAW, comprimate fără pierderi în Jpeg (nu date RGB!)|

## Avantajul formatului de fișier CR2

Stocarea imaginilor în format RAW permite o mulțime de post-procesare a fotografiei, cum ar fi ajustarea balansului de alb. Acest lucru este mult mai dificil și cu o pierdere mare de calitate cu alte formate de fișiere imagine, cum ar fi [JPEG](/ro/image/jpeg/).

## CR2 este mai bun decât JPEG?

Fișierele CR2 sunt fișiere brute fără pierderi de date și, prin urmare, fără pierderi de calitate. Pe de altă parte, JPEG este format de fișier imagine cu pierderi, deoarece pierde unele date pentru a reduce fișierul. Astfel, fișierele CR2 sunt de înaltă calitate și mai potrivite pentru retușare și îmbunătățiri.

## Referințe

* [Format fișier CR2](http://lclevy.free.fr/cr2/)

