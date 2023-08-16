{
  "date" : "2020-08-20",
  "keywords" :[ "fișier fnt", "format fișier fnt", "ce este un fișier fnt", "fișier", "exemplu fnt", "extensie fișier fnt", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Fișier cu font Windows",
  "description":"Aflați despre formatul de fișier FNT și despre API-urile care pot crea și deschide fișiere FNT.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Ce este un fișier FNT?

Un fișier cu extensia .fnt este un fișier de font care stochează informații generice despre font pe sistemele de operare Windows. Fișierele FNT au fost înlocuite în cea mai mare parte cu formatele de fișier TrueType (.TTF) și OpenType (.OTF) și este un format de fișier cu font învechit de acum. Aceste fișiere pot stoca un singur evaluator sau font vectorial. Toate driverele de dispozitiv acceptă fonturile Windows 2.x. Cu toate acestea, nu toate driverele de dispozitiv
acceptă versiunea Windows 3.0.

## Format de fișier FNT

Fișierele FNT sunt capabile să stocheze un singur font raster sau vectorial. Formatele vectoriale sunt utilizate mai frecvent de GDI în comparație cu rasterul în care gliful fiecărei charter este definit folosind un bitmap mic. Motivul evident pentru înlocuirea .fnt cu .ttf și .otf este formatul său raster.

### Antet fișier font
Pornirea ambelor fișiere cu font raster și vector este obișnuită, urmată de informații diferite pentru fiecare tip de fișier. Antetul font-file include pentru Windows 3.0 include șase câmpuri noi, după cum urmează, care sunt setate la zero pentru a asigura compatibilitatea cu versiunile viitoare de Windows.

* dFlags
* dfAspace
* dfBspace
* dfCspace
* dfColorPointer
* dfReserved1

Pentru informații detaliate despre anteturile pentru Windows 3.0 și 2.0, vizitați [Arhiva Microsoft KnowledgeBase](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Referințe
* [Format fișier font](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Cum se instalează sau se elimină un font în Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8-7613-c76f-88d043b334b8)

