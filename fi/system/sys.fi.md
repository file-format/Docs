{
  "date": "2021-07-08",
  "keywords": [
"SYS",
"laajennus",
"tiedosto",
"muoto",
"järjestelmä",
"Kuljettaja",
"Järjestelmätiedosto",
"ohjelmia",
"tietokone",
"sovellus"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "SYS - Järjestelmätiedostomuoto",
  "description": "Opi SYS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SYS-tiedostoja.",
  "linktitle": "SYS",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-sy-fis"
}
},
  "lastmod": "2021-07-08"
}

## Mikä on SYS-tiedosto? ##

SYS-tiedostot ovat järjestelmätiedostoja, joita käytetään Windows-käyttöjärjestelmässä ja MS-DOS-sovelluksissa. Näitä tiedostoja ei voi avata suoraan, ja ne koostuvat laitteen ohjaimesta ja kokoonpanosta. SYS-tiedostot vastaavat käyttöjärjestelmän ydintoimintojen tiedostoista. Näitä pidetään laiteajurin kriittisinä tiedostoina, ja niitä voidaan käyttää myös silloin, kun jokin kilpa-kuljettajan ongelma on ratkaistava. Nämä ovat vastuussa tietokonejärjestelmän asianmukaisesta toiminnasta, ja .sys-tiedostojen on oltava oikeita ja täydellisiä.


## Tekniset tiedot ##

.sys-tiedostot ovat itse asiassa {{HYPERLINKKI}}-muodon osajoukko, koska se sallii vain tietyt yhdistelmät. Näiden tiedostojen tavallinen muoto on LOGOS.SYS, LOGOW.SYS ja LOGO.SYS. Muilla tiedostoilla ei ole tätä muotoa.

Näitä tiedostoja käytetään useimmiten Windowsin *C*-hakemistossa asennuksen aikana. Useimmat laiteajureihin liittyvät ongelmat ratkaistaan päivittämällä Windows-käyttöjärjestelmä. Näiden tiedostojen yksityiskohdat ja tiedot voidaan tarkastella käyttämällä Windows-käyttöjärjestelmän sisäänrakennettuja ohjelmia. Nämä sisältävät myös viittaukset käyttöjärjestelmän eri moduuleihin.
Joitakin esimerkkejä järjestelmätiedostoista ovat:

* IO.SYS (Nämä tallentavat levykäyttöjärjestelmän laiteohjaimet)

* MSDOS.SYS (Nämä sisältävät ytimen tai käyttöjärjestelmän ydinkoodin)

* CONFIG.SYS (Nämä sisältävät erilaisia konfigurointivaihtoehtoja)

* KEYBOARD.SYS (Nämä sisältävät näppäimistön asettelua koskevia tietoja) 

* COUNTRY.SYS (Nämä sisältävät maata ja koodisivua koskevia tietoja)


## SYS-tiedostomuoto ##

Microsoft kehitti tiedostot .sys-tunnisteilla. Muuttujat ja funktiot sisältyvät SYS-tiedostoihin. Näitä käyttävät enimmäkseen Microsoft-käyttöjärjestelmä. Nämä tiedostot sijaitsevat pääasiassa levyn juurihakemistossa:

* C:\Windows\system32\drivers

* C:\Windows\WinSxS


Jotkut yleiset varoitukset SYS-tiedostoista ovat seuraavat:

* Näiden tiedostojen nimiä ei pidä muuttaa, koska nämä tiedostot ovat vastuussa käyttöjärjestelmän ydintoiminnoista ja muuttujista
* Näitä tiedostoja ei pidä poistaa, koska niiden puuttuminen voi aiheuttaa virheitä
* .sys-tiedostoja ei saa ladata Internetistä ennen kuin olet varma lähteen laillisuudesta
* Näiden tiedostojen kanssa ei pidä sotkea, koska niiden muuttaminen tai niiden kanssa sotkeutuminen aiheuttaa vakavia järjestelmävirheitä
* Jos jokin virus tai haittaohjelma vahingoittaa näitä tiedostoja, ne tulee asentaa uudelleen

## SYS-esimerkki ##

Seuraavassa on esimerkki yksinkertaisesta SYS-järjestelmän kokoonpanotiedostosta:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
