{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CPIO-tiedosto - Unix CPIO-arkistotiedostomuoto",
  "description":"Opi tuntemaan, mikä on CPIO-tiedosto ja API:t, jotka voivat luoda ja avata CPIO-tiedostoja.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio-fi",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Mikä on CPIO-tiedosto?

CPIO-tiedosto on arkistotiedosto, joka on luotu Unixin Copy In Copy Out (CPIO) -muodossa. Se on samanlainen kuin TAR-tiedostomuoto, paitsi että se on pakkaamaton. CPIO-tiedostot voivat tallentaa laitetiedostoja, symbolisia linkkejä ja laajennettuja tiedostomääritteitä.

## CPIO-tiedostomuoto

CPIO-arkisto luodaan binääritiedostona, joka ei ole ihmisen luettavissa. Se tallentaa tiedostojen ja hakemistojen kokoelman. CPIO-arkiston sisältö tunnistetaan metatietotiedoilla, kuten tiedostonimillä, käyttöoikeuksilla, omistajuudella ja aikaleimoilla. Nämä metatietotiedot tallennetaan myös arkistotiedostoon järjestelmän sivuttaiskäyttöä varten.

## CPIO-arkiston muoto

CPIO-tiedosto koostuu yhdestä tai useammasta ketjutetusta jäsentiedostosta. Jokainen arkiston tiedosto koostuu otsikosta, jota mahdollisesti seuraa otsikossa mainittu tiedoston sisältö. Arkisto sisältää toisen otsikon lopussa, jota kuvaa tyhjä tiedosto nimeltä TRAILER!!.

### CPIO-arkistojen tyypit

CPIO-arkistoja on kahdenlaisia. Nämä eroavat vain otsikon tyylistä.

* ASCII-arkistot – Näissä CPIO-arkistoissa on tulostettava otsikko, josta tulee osa CPIO-arkistoa, jos itse arkisto koostuu ASCII-tiedostoista

* Binaariarkistot - Näillä CPIO-arkistoilla on binääriotsikot.


## Työskentely CPIO-arkiston kanssa

### Miten luodaan CPIO-arkistoja?

Voit luoda CPIO:n Unix-tyyppisissä järjestelmissä käyttämällä **cpio**-komentoa. Seuraava komento löytää kaikki tiedostot ja hakemistot nykyisestä hakemistosta ja sen alihakemistoista. Tämä tulos johdetaan sitten cpio-komentoon, joka luo uuden CPIO-arkiston nimeltä archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Kuinka purkaa tiedostoja CPIO-arkistoista?

Seuraava komento purkaa tiedostot olemassa olevasta arkistosta.

```
cpio -id < archive_cpio.cpio
```
Se lukee archive.cpio-tiedoston vakiosyötteestä ja purkaa tiedostot nykyiseen hakemistoon.


## Viitteet

* [CPIO - Wikipedia](https://en.wikipedia.org/wiki/Cpio)

* [CPIO File Format](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

