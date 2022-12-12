{
  "date" : "2021-06-16",
  "keywords" :[ "LZH", "Comprimat", "Fișier", "Extensie", "Format fișier", "Lempel-Ziv", "Haruyasu", "LHA"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier LZH",
  "description":"Aflați despre formatul de fișier LZH și despre API-urile care pot crea și deschide fișiere LZH.",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Ce este un fișier LZH? ##

Un fișier cu extensia .lzh și .lha se referă de obicei la formatul de fișier de compresie a arhivei. Acest format de fișier este același cu alte formate de compresie de fișiere, cum ar fi [ZIP](/ro/compression/zip/), [RAR](/ro/compression/rar/), etc. Scopul principal al acestor formate de fișier este de a reduce dimensiunea fișierului. format pentru a trimite cu ușurință precum și pentru a le păstra împreună în formă comprimată. În comparație cu alte companii occidentale, fișierele LZH sunt foarte populare în Japonia și sunt utilizate de obicei pentru comprimarea datelor din jocurile video. Suplimentul LZH pentru Windows 7 este încorporat în versiunea japoneză a Windows 7. Microsoft a lansat pentru prima dată programul de completare Microsoft Compressed (LZH) Folder pentru versiunea japoneză a Windows XP. Acest format de fișier este implementat cu prevederi de compresie și caracteristici utilizate de algoritmul Lempel-Ziv și Haruyasu

## Specificație LZH ##

Metoda de compresie a unei arhive LZH este afișată ca șir de text de cinci octeți, cum ar fi -lz1-. Aceștia sunt al treilea până la al șaptelea octeți din fișierul comprimat.

|Specificație|Descriere|
---|---|
|Extensie | .lzh, .lha|
|Tipul media| aplicație/x-lzh-comprimat|
|Cod de tip| „LHA_” (LHA-SPAȚIU)|
|UTI| public.archive.lha|
|Dezvoltat de| Haruyasu Yoshizaki (Yoshi)|
|Tip| Compresie|
|Extins de la| LArc|

## Probleme la deschiderea unui fișier LZH ##

Următoarele sunt câteva probleme care pot cauza funcționarea proastă a formatului de fișier LZH:
  

* Fișierul poate fi corupt. Pentru a rezolva această problemă, descărcați din nou fișierul sau cereți expeditorului să retrimite fișierul din nou
* Al doilea motiv este fișierul infectat, în acest caz, scanați fișierul corect
* Legături necorespunzătoare către fișierul LZH
* Eliminarea descrierii LZH
* Nu sunt suficiente resurse hardware
* Șoferi de echipamente învechiți

## Referințe ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
