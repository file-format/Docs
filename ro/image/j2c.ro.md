{
  "date" : "2019-10-11",
  "keywords" :[ "fișier j2c", "format fișier j2c", "ce este un fișier j2c", "fișier", "exemplu j2c", "extensie fișier j2c", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"Aflați despre formatul de fișier J2C și despre API-urile care pot crea și deschide fișiere J2C.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## Ce este un fișier J2C?

Un fișier cu extensia .j2c este o variantă a formatului de fișier JPEG și este comprimat cu compresia wavelet. Are un sistem de markeri și segmente aproape identic cu formatul de fișier JPEG 2000. Formatul de fișier J2C este definit în partea 1 a suportului JPEG 2000, care acceptă atât compresia cu pierderi, cât și fără pierderi. Fluxul de cod JPEG 2000 a fost conceput pentru a fi încorporat în [JP2](/ro/image/jp2/) sau în alt format de fișier, deși poate apărea într-un fișier de la sine. Un fișier J2C poate fi deschis folosind Adobe Photoshop 2020, Adobe Illustrator 2020 și Corel Paintshop Pro.

## Format de fișier J2C

Formatul de fișier J2C este același cu cel al JPEG 2000, care este adesea salvat ca .jp2 și .jpc. Acest lucru face ca fișierele J2C să urmeze aceeași abordare de codificare a metadatelor în format XML, în care Standardul 12234-1 este folosit ca referință între etichetele Exif și componentele XML. Este îmbunătățit și mai mult de extensia JPEG 2000 partea 2, care combină mecanismul de animație și configurațiile fluxului de cod într-o singură imagine. Astfel de fișiere în format de fișier extins sunt salvate ca [.jpx](/ro/image/jpx/).

### Aspectul unui fișier JPEG2000

JPEG2000 acceptă o varietate de aplicații bazate pe conformitatea cu formatele de fișiere extensibile. Deși cel mai simplu tip poate conține o singură imagine, tipurile mai complexe pot include o serie de imagini, stivuite unele peste altele sau sunt secvențiate bazate pe timp.

#### Cutia JP2
Este blocul de construcție de nivel superior al formatului de fișier JP2 și conține un câmp de tip și lungime în antet și o secțiune de date. Cel mai notabil tip de cutie este cutia codificată adiacentă. Această casetă stochează în secțiunea sa de date fluxul de cod JPEG2000.

#### JPEG2000 CodeStream

JPEG2000 CodeStream este o secvență de octeți care este necesar pentru a decoda imaginea comprimată JPEG2000. În cazul în care fișierul nu are altceva decât acest flux de cod, acesta se numește fișier de flux de cod brut. De obicei, un flux de cod JPEG este aplicarea algoritmului de compresie JPEG2000 pe o imagine, deși nu este singura modalitate.

#### Piese de gresie ####

O imagine codificată JPEG2000 este o colecție de unități de date numite pachete. Aceste pachete sunt menținute în fluxul de cod în interiorul unor grupuri de pachete numite tile-parts. Înainte de a codifica o imagine, codificatorul împarte imaginea într-o grilă dreptunghiulară de blocuri, numite plăci în care fiecare plăci este codificată separat, indiferent de celelalte plăci.

{{< figure src="../JPEG2000_Codestream.png" alt="Format de fișier JPEG2000" >}}

## Compresie J2C
JPEG 2000 folosește tehnologia de compresie wavelet, făcându-l rapid pe baza faptului că relativ puțini pixeli sunt afișați în orice fereastră sau fereastră în care vizualizatorul afișează imaginea. Acest lucru poate fi subliniat prin faptul că doar câțiva megaocteți de pixeli vor apărea pe ecran pentru imagini de dimensiuni foarte mari (în gigaocteți). Acest lucru ajută la preluarea și redarea rapidă numai a acelei părți a datelor de imagine care este necesară pentru popularea pixelilor de afișare. Acest lucru necesită, de asemenea, tehnologie de decompresie de mare viteză pentru a accelera mecanismul de preluare a imaginii pentru a crea imaginile necesare din mers.

J2C profită de decompresia rapidă și preia doar informațiile necesare pentru ca datele pixelilor să redă rapid o parte din imaginile vizibile pe ecrane. J2C este conceput în primul rând pentru vizualizarea datelor și nu pentru editarea acestora.

## Identificare J2C
Fișierele JPEG 2000 au octeți de semnătură `FF 4F FF 51`.

### Tipuri Mime
Tipurile Mime înregistrate pentru fișierele JPEG 2000 includ:
* imagine/j2c
* imagine/jpx
* imagine/jpm
* video/mj2

## Îmbunătățiri față de standardul JPEG
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

