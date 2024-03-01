{
  "date": "2021-07-25",
  "keywords": [
"mies",
"tiedosto",
"laajennus",
"tyyppi",
"muoto",
"Unix käsikirja"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MAN - Unix-käsikirja",
  "description": "Opi FODT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MAN-tiedostoja.",
  "linktitle": "MAN",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-ma-fin"
}
},
  "lastmod": "2021-07-25"
}

## Mikä on MAN-tiedosto?

Tiedosto, jonka pääte on .man, tarkoittaa man-sivua, joka on Unix-ohjelmoinnin käyttöohje ohjelmiston dokumentaatiomuodossa. Sitä käyttää Unixissa oleva Man-apuohjelma, jota käytetään dokumentaation katseluun. Ohjelmistodokumentaatio sisältää tietoja osioissa ja sivuissa, jotka voidaan hakea Man-apuohjelmalla komentopäätteestä antamalla komentoja. Koska se on saatavilla tietokoneessa asiakirjan pehmeänä kopiona, se ei vaadi painettua kopiota tai Internet-yhteyttä käyttääkseen sitä.

## Unix Manual Man -tiedostomuoto - lisätietoja

Man-sivut tallennetaan vain tekstimuodossa, ja ne voidaan luoda ja avata missä tahansa tekstieditorissa katselua tai muokkausta varten. UNIXissa tiedot Man-sivuilta haetaan antamalla terminaalista komentoja, jotka sisältävät viittauksen oppaan osiin ja sivunumeroihin.

### Osat ja sivut

Unix man on järjestelmän käsikirja, jossa jokainen komennon sivuargumentti viittaa ohjelman, apuohjelman tai funktion nimeen. komento, jos se sisältää osion tiedot, etsii sivua kyseisestä osiosta. Oletustoiminto on kuitenkin etsiä sivua kaikista osioista ja näyttää ensimmäinen sivu riippumatta siitä, onko se useissa osioissa.

### Osion numerot

Seuraavassa on tietoja käsikirjan osien numeroista ja niiden sisältämien sivujen tyypeistä.

|Osion numero|Sivutyyppi|
---|---|
|1|Suoritettavat ohjelmat tai komentotulkkikomennot|
|2|Järjestelmäkutsut (ytimen tarjoamat toiminnot)|
|3|Kirjastokutsut (toiminnot ohjelmakirjastoissa)|
|4|Erikoistiedostot (yleensä /dev)|
|5|Tiedostomuodot ja käytännöt, esim. /etc/passwd|
|6|Pelit|
|7|Sekalaista (mukaan lukien makropaketit ja käytännöt), esim. man(7), groff(7)|
|8|Järjestelmänhallinnan komennot (yleensä vain pääkäyttäjälle)|
|9|Ytimen rutiinit [Ei vakio]|

## Esimerkki - Kuinka lukea MAN-sivuja?

Tässä on esimerkki MkDir-komennon tietojen hakemisesta Man-komennolla.

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

## Viitteet

* [OpenDocumentin tekniset tiedot – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)

* [man(1) – Linux-käyttöopassivu](https://man7.org/linux/man-pages/man1/man.1.html)


