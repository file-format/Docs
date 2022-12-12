{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier PET - fișierul pachet de instalare Puppy Linux",
  "description":"Aflați despre formatul fișierului PET și despre API-urile care pot crea și deschide fișiere PET.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Ce este un fișier Linux PET?

Un fișier PET este un fișier de pachet de instalare a aplicației creat și utilizat cu varianta PuppyLinux a sistemului de operare Linux. Este creat ca un fișier comprimat [TGZ](/ro/compression/tgz/) care reduce dimensiunea fișierului arhivei comprimate. Integritatea formatului de fișier PET este asigurată de suma de control md5sum care este atașată la sfârșitul fișierului pentru verificare la capătul de la distanță. Fișierele PET pot fi extrase folosind extractorul de fișiere TGZ standard și WinRAR. Fișierele PET au înlocuit vechile fișiere de instalare a pachetului [PUP](/ro/compression/pup/).

## Format de fișier PET

Fișierele PET sunt salvate pe disc ca arhive comprimate în format de fișier binar. Cu toate acestea, detaliile interne ale formatului fișierului PET nu sunt cunoscute. Similar cu fișierele de instalare a pachetelor [.exe](/ro/executable/exe/) și [.msi](/ro/executable/msi/), fișierele PET încep o instalare atunci când sunt executate.

## Referințe

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [Indexul pachetelor PET PuppyLinux](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

