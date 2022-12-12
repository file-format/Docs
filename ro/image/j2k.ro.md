{
  "date" : "2019-10-11",
  "keywords" :[ "fișier j2k", "format fișier j2k", "ce este un fișier j2k", "fișier", "exemplu j2k", "extensie fișier j2k", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2K",
  "description":"Aflați despre formatul de fișier J2K și despre API-urile care pot crea și deschide fișiere J2K.",
  "linktitle" : "J2K",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-03"
}

## Ce este un fișier J2K?

Un fișier **J2K** este o imagine care este comprimată folosind compresia wavelet în loc de compresia DCT. Acest format de fișier este utilizat de fișierele 2000 ale Joint Photographic Experts Group (JPEG). Fișierele J2K stochează informații despre metadate despre fișierul imagine în XML, spre deosebire de .jpeg sau .jpg care utilizează formatul EXIF în acest scop. Fișierele J2K acceptă culoare pe 15 biți, transparență alfa și compresie fără pierderi. Există mai multe API-uri comerciale pentru a decoda imagini JPEG 2000, cum ar fi J2K-Codec. Un fișier J2K poate fi deschis pe sistemul de operare Windows folosind vizualizatoarele de imagini standard.

## Format fișier J2K ##

Formatul de fișier J2K este același cu cel al JPEG 2000, care este adesea salvat ca .jp2 și .jpc. Acest lucru face ca fișierele J2K să urmeze aceeași abordare de codificare a metadatelor în format XML, în care Standardul 12234-1 este folosit ca referință între etichetele Exif și componentele XML. Este îmbunătățit și mai mult de extensia JPEG 2000 partea 2, care combină mecanismul de animație și configurațiile fluxului de cod într-o singură imagine. Astfel de fișiere în format de fișier extins sunt salvate ca .jpx.

### Aspectul unui fișier JPEG2000 ###

JPEG2000 acceptă o varietate de aplicații bazate pe conformitatea cu formatele de fișiere extensibile. Deși cel mai simplu tip poate conține o singură imagine, tipurile mai complexe pot include o serie de imagini, stivuite unele peste altele sau sunt secvențiate bazate pe timp.

#### Cutie JP2 ####
Este blocul de bază al formatului de fișier JP2 și conține câmpuri de tip și lungime în antet și o secțiune de date. Cel mai notabil tip de cutie este cutia codificată adiacentă. Această casetă stochează în secțiunea sa de date fluxul de cod JPEG2000.

#### JPEG2000 CodeStream ####

JPEG2000 CodeStream este o secvență de octeți care este necesar pentru a decoda imaginea comprimată JPEG2000. În cazul în care fișierul nu are altceva decât acest flux de cod, acesta se numește fișier de flux de cod brut. De obicei, un flux de cod JPEG este aplicarea algoritmului de compresie JPEG2000 pe o imagine, deși nu este singura modalitate.

#### Piese de gresie ####

O imagine codificată JPEG2000 este o colecție de unități de date numite pachete. Aceste pachete sunt menținute în fluxul de cod în interiorul unor grupuri de pachete numite tile-parts. Înainte de a codifica o imagine, codificatorul împarte imaginea într-o grilă dreptunghiulară de blocuri, numite plăci în care fiecare plăci este codificată separat, indiferent de alte plăci.

{{< figure src="../JPEG2000_Codestream.png" alt="Format de fișier JPEG2000" >}}

## Compresie J2K ##
JPEG 2000 folosește tehnologia de compresie wavelet, făcându-l rapid pe baza faptului că relativ puțini pixeli sunt afișați în orice fereastra sau fereastra în care vizualizatorul afișează imaginea. Acest lucru poate fi subliniat prin faptul că doar câțiva megaocteți de pixeli vor apărea pe ecran pentru imagini de dimensiuni foarte mari (în gigaocteți). Acest lucru ajută la preluarea și redarea rapidă numai a acelei părți a datelor de imagine care este necesară pentru popularea pixelilor de afișare. Acest lucru necesită, de asemenea, tehnologie de decompresie de mare viteză pentru a accelera mecanismul de preluare a imaginii pentru a crea imaginile necesare din mers.

J2K profită de decompresia rapidă și preia doar informațiile necesare pentru ca datele pixelilor să redă rapid o parte din imaginile vizibile pe ecrane. J2K este conceput în primul rând pentru vizualizarea datelor și nu pentru editarea acestora.

## Identificare J2K ##
Fișierele JPEG 2000 au octeți de semnătură 6A 50 20 20.

### Tipuri de mime ###
Tipurile Mime înregistrate pentru fișierele JPEG 2000 includ:
* imagine/jp2
* imagine/jpx
* imagine/jpm
* video/mj2

## Îmbunătățiri față de standardul JPEG ##
Îmbunătățirile față de standardul JPEG includ:
* Performanță superioară la compresie
* Reprezentare cu rezoluție multiplă
* Transmitere progresivă prin pixeli și precizie rezoluție
* Alegerea compresiei fără pierderi sau cu pierderi
* Reziliență la erori, format de fișier flexibil
* Suport pentru intervalul dinamic ridicat
* Informații spațiale ale canalului lateral

## Referințe ##
* [Taubman, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

