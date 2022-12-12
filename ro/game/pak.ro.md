{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "format fișier", "ce este un fișier pak", "fișier", "exemplu pak", "Fișier pachet de jocuri video", "extensie"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre fișierul .pak și API-urile care pot crea și deschide fișiere PAK.",
  "title" :"Format fișier PAK- Fișier pachet joc video",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Ce este un fișier PAK?

Un fișier PAK este un fișier pachet creat de diferite jocuri video pentru a arhiva datele jocului. În esență, este un format de fișier de joc. Aceasta poate include mai multe elemente de joc, cum ar fi grafică, texturi, sunete, obiecte, împreună cu alte date de joc. Arhiva este în mare parte salvată ca fișier .zip și poate fi extrasă cu software-ul de decompresie popular, cum ar fi WinZip și WinRAR. Exemple de jocuri video care utilizează fișiere PAK includ Quake, Hexen, Crysis și Half-Life.

## Format de fișier PAK - Mai multe informații

În cele mai multe cazuri, fișierele PAK sunt salvate în [format fișier ZIP](/ro/compression/zip/). Dar diferite aplicații pot utiliza format de fișier diferit pentru stocarea acestor fișiere.


## Cum se deschide fișierele PAK?

Puteți deschide fișiere PAK cu aplicații precum [PakExplorer](https://www.quaketerminus.com/tools.shtml) și [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- ------------------------**

## Format fișier PAK - Fișier obiect Simutrans

Un fișier cu extensie .pak este un format de fișier de joc de simulare de transport [Simutrans](https://www.simutrans.com/en/). Conține obiecte utilizate în simulare, cum ar fi grafice realizate de utilizator și conținut de date. Poate avea mai multe obiecte diferite, cum ar fi vehicule de joc, clădiri, teren, etc. Fișierele PAK sunt generate utilizând MakeObject, un utilitar care compilează fișiere .dat și imagini .png pentru crearea acestor obiecte de simulare. Simutrans le permite jucătorilor să conducă un sistem de transport de succes prin construirea și gestionarea sistemelor de transport terestru pentru pasageri, corespondență și mărfuri

## Cum se creează fișiere PAK?

Simutrans a enumerat exemple de exemple pentru crearea fișierelor PAK pe sistemul de operare Windows și Linux.

### Sistemul de operare Windows

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## Referințe

* https://simutrans-germany.com/wiki/wiki/en_doPak
* https://en.wikipedia.org/wiki/Simutrans

