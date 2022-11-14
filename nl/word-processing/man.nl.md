{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Unix-handleiding",
  "description":"Meer informatie over FODT-bestandsindelingen en API's die MAN-bestanden kunnen maken en openen.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## Wat is een MAN-bestand?

Een bestand met de extensie .man staat voor man-pagina, een gebruikershandleiding voor Unix-programmering in de vorm van softwaredocumentatie. Het wordt gebruikt door het `Man`-hulpprogramma, opgenomen in Unix, dat wordt gebruikt om de documentatie te bekijken. De softwaredocumentatie bevat informatie in secties en pagina's die kunnen worden opgehaald met het Man-hulpprogramma vanaf de opdrachtterminal door opdrachten uit te voeren. Omdat het beschikbaar is op de computer als een zachte kopie van documentatie, is er geen gedrukte kopie of internetverbinding nodig om toegang te krijgen.

## Unix Manual Man-bestandsindeling - Meer informatie

Man-pagina's worden opgeslagen in platte tekst en kunnen in elke teksteditor worden gemaakt en geopend om ze te bekijken of te bewerken. In UNIX wordt informatie uit de Man-pagina's opgehaald door commando's uit de terminal te geven die verwijzingen naar sectie- en paginanummers uit de handleiding bevatten.

### Secties en pagina's

Unix man is de systeemhandleiding waarin elk paginaargument van de opdracht verwijst naar de naam van een programma, hulpprogramma of functie. de opdracht, indien voorzien van sectie-informatie, zal zoeken naar de pagina in die specifieke sectie. Het standaardgedrag is echter om de pagina in alle secties te zoeken en de eerste pagina weer te geven, ongeacht of deze in meerdere secties bestaat.

### Sectienummers

Hieronder vindt u informatie over de sectienummers van de handleiding, gevolgd door de soorten pagina's die ze bevatten.

|Sectienummer|Type pagina's|
---|---|
|1|Uitvoerbare programma's of shell-commando's|
|2|Systeemaanroepen (functies geleverd door de kernel)|
|3|Bibliotheekoproepen (functies binnen programmabibliotheken)|
|4|Speciale bestanden (meestal te vinden in /dev)|
|5|Bestandsformaten en conventies, bijv. /etc/passwd|
|6|Spellen|
|7|Diversen (inclusief macropakketten en conventies), bijv. man(7), groff(7)|
|8|Systeembeheeropdrachten (meestal alleen voor root)|
|9|Kernelroutines [Niet standaard]|

## Voorbeeld - Hoe lees ik MAN-pagina's?

Hier is een voorbeeld van het ophalen van informatino over de MkDir-opdracht met behulp van de Man-opdracht.

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

## Referenties

* [Technische specificaties van OpenDocument - door Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — Linux-handleiding](https://man7.org/linux/man-pages/man1/man.1.html)

