{
  "date": "2021-07-25",
  "keywords": [
"vyras",
"failą",
"pratęsimas",
"tipo",
"formatu",
"Unix vadovas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MAN - Unix vadovas",
  "description": "Sužinokite apie FODT failo formatą ir API, kurios gali kurti ir atidaryti MAN failus.",
  "linktitle": "MAN",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-ma-ltn"
}
},
  "lastmod": "2021-07-25"
}

## Kas yra MAN failas?

Failas su plėtiniu .man reiškia man puslapį, kuris yra Unix programavimo vartotojo vadovas programinės įrangos dokumentacijos formoje. Jį naudoja Man programa, įtraukta į Unix ir kuri naudojama dokumentams peržiūrėti. Programinės įrangos dokumentacijoje yra informacijos skyriuose ir puslapiuose, kuriuos galima gauti naudojant Man įrankį iš komandų terminalo, išduodant komandas. Kompiuteryje galima naudotis kaip minkšta dokumentų kopija, todėl norint ją pasiekti nereikia jokios spausdintos kopijos ar interneto ryšio.

## „Unix“ vadovo „Man“ failo formatas – daugiau informacijos

Man puslapiai saugomi paprasto teksto formatu, juos galima sukurti ir atidaryti bet kuriame teksto rengyklėje, kad būtų galima peržiūrėti ar redaguoti. UNIX sistemoje informacija iš Man puslapių gaunama iš terminalo išduodant komandas, kuriose yra nuoroda į vadovo skyrių ir puslapių numerius.

### Skyriai ir puslapiai

Unix man yra sistemos vadovas, kuriame kiekvienas komandos puslapio argumentas nurodo programos, programos ar funkcijos pavadinimą. komanda, jei pateikiama skyriaus informacija, ieškos puslapio toje konkrečioje skiltyje. Tačiau numatytasis elgesys yra ieškoti puslapio visose skiltyse ir rodyti pirmąjį puslapį, neatsižvelgiant į tai, ar jis yra keliose skiltyse.

### Sekcijų numeriai

Toliau pateikiama informacija apie vadovo skyrių numerius ir juose esančių puslapių tipus.

|Sekcijos numeris|Puslapių tipas|
---|---|
|1|Vykdomos programos arba apvalkalo komandos|
|2|Sistemos iškvietimai (branduolio teikiamos funkcijos)|
|3|Bibliotekos iškvietimai (funkcijos programų bibliotekose)|
|4|Specialūs failai (dažniausiai randami /dev)|
|5|Failų formatai ir sutartys, pvz., /etc/passwd|
|6|Žaidimai|
|7|Įvairūs (įskaitant makro paketus ir susitarimus), pvz., man(7), groff(7)|
|8|Sistemos administravimo komandos (dažniausiai tik root)|
|9|Branduolinės programos [Nestandartinė]|

## Pavyzdys – kaip skaityti MAN puslapius?

Štai pavyzdys, kaip gauti informaciją apie MkDir komandą naudojant komandą Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Nuorodos

* [OpenDocument techninės specifikacijos – Vikipedija](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)

* [man(1) – Linux vadovo puslapis](https://man7.org/linux/man-pages/man1/man.1.html)


