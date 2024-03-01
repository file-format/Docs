{
  "date": "2019-10-11",
  "keywords": [
"gz tiedosto",
"gz tiedostomuoto",
"mikä on gz-tiedosto",
"tiedosto",
"gz esimerkki",
"gz tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GZ-tiedostomuoto - GNU-pakattu arkistotiedosto",
  "description": "Opi, mikä on GZ-tiedosto ja API:t, jotka voivat luoda ja avata GZ-tiedostoja.",
  "linktitle": "GZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-g-fiz"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on GZ-tiedosto?

GZ-tiedosto on pakattu arkisto, joka luodaan käyttämällä tavallista [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) -pakkausalgoritmia. Se voi sisältää useita pakattuja tiedostoja, hakemistoja ja tiedostokantoja. Tämä muoto kehitettiin alun perin korvaamaan pakkausmuodot UNIX-järjestelmissä. ja on edelleen yksi yleisimmistä arkistotyypeistä Linux-järjestelmissä. Sovellukset, kuten [WinZip](https://www.winzip.com/en/), voivat avata GZ-tiedostoja ja tarkastella niiden sisältöä sekä Windowsissa että MacOS:ssa.

## GZ-tiedostomuoto - lisätietoja

Gzip käyttää [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE)-algoritmia arkiston pakkaamiseen ja eroaa [ZIP](/compression/zip/)-arkistomuodosta siinä, että se käyttää pakkausalgoritmia täydelliseen arkistoihin yksittäisten tiedostojen sijaan. Internet Engineering Task Forcen (IETF) julkaisema GZIP-tiedostomuotomääritysten versio 4.3 sisältää yksityiskohtaisia tietoja tiedostomuodosta. Tiedostomuoto koostuu:

* Tiedoston otsikko

* Valinnaiset otsikot

* Pakatut tiedot

* Tiedoston alatunniste


## GZ-tiedoston otsikko ##

GZ-tiedoston otsikko koostuu 10 tavusta seuraavasti:

|Offset|Koko|Arvo|Kuvaus
---|---|---|---|
|0|2|0x1f 0x8b|Maaginen numero, joka tunnistaa tiedostotyypin
|2|1| |Compression Method * 0-7 (varattu) * 8 (tyhjennä)
|3|1| |Tiedostoliput
|4|4| |32-bittinen aikaleima
|8|1| |Pakkausliput
|9|1| |Käyttöjärjestelmän tunnus

### Tiedostoliput ###

|Arvo|Identifier|Description
---|---|---|
|0x01|FTEXT|Jos tämä on asetettu, pakkaamatonta dataa on käsiteltävä tekstinä binääritietojen sijaan. Tämä lippu viittaa rivin lopun muuntamiseen alustojen välisille tekstitiedostoille, mutta ei pakota sitä.
|0x02|FHCRC|Tiedosto sisältää otsikon tarkistussumman (CRC-16)
|0x04|FEXTRA|Tiedosto sisältää ylimääräisiä kenttiä
|0x08|FNAME|Tiedosto sisältää alkuperäisen tiedostonimimerkkijonon
|0x10|FCOMMENT|Tiedosto sisältää kommentin
|0x20| |Varattu
|0x40| |Varattu
|0x80| |Varattu

### Käyttöjärjestelmä ###

|Arvo|Kuvaus
---|---|
|0|FAT-tiedostojärjestelmä (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (tai OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari TOS
|6|HPFS-tiedostojärjestelmä (OS/2, NT)
|7|Macintosh
|8|Z-järjestelmä
|9|CP/M
|10|TOPS-20
|11|NTFS-tiedostojärjestelmä (NT)
|12|QDOS
|13|Acorn RISCOS
|255|tuntematon

## GZ valinnaiset otsikot ##

Valinnaiset ylimääräiset otsikot ovat ne, jotka on merkitty tiedostolipuilla, ja sisältävät tietoja, kuten alkuperäisen tiedostonimen, lisäkentät, kommentit ja otsikon tarkistussumman.

## Pakatut tiedot ##

Tämä osa sisältää pakatut tiedot DEFLATE-pakkausalgoritmilla.

## GZ-tiedoston alatunniste ##

Tiedoston alatunniste on kooltaan 8 tavua ja sisältää seuraavat tiedot.

|Offset|Koko|Kuvaus
---|---|---|
|0|4|Tarkistussumma (CRC-32)
|4|4|Pakkaamattoman tiedon koon arvo tavuina

## Viitteet ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

* [RFC1952: GZIP-tiedostomuodon määritys](https://datatracker.ietf.org/doc/html/rfc1952), IETF.


