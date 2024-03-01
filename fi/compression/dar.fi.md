{
  "date": "2021-04-08",
  "keywords": [
"dar tiedosto",
"dar-tiedostomuoto",
"mikä on dar-tiedosto",
"tiedosto",
"vielä esimerkki",
"dar tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DAR - Levyn arkistointitiedostomuoto",
  "description": "Opi DAR-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DAR-tiedostoja.",
  "linktitle": "DAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-da-fir"
}
},
  "lastmod": "2021-04-09"
}

## Mikä on DAR-tiedosto?

Tiedosto, jonka pääte on .dar, on pakattu arkisto, joka on luotu DAR Disk -arkiston avulla. Se voi luoda varmuuskopion / arkiston koko levylle tai tiedostoryhmälle. Se luotiin korvaamaan [TAR](/compression/tar/)-tiedostomuoto UNIX-käyttöjärjestelmässä, ja se voidaan luoda jaetuiksi arkistotiedostoiksi suurelle määrälle tiedostoja. DAR-arkisto tukee mahdollisuutta poistaa järjestelmästä tiedostoja, jotka on linkitetty arkiston päätiedostoihin. Sen kyky tarjota differentiaali-, lisä- ja dekrementaalinen varmuuskopiointi tekee siitä TAR-tiedostoja parempia.

## DAR-tiedostomuoto

DAR-tiedostot ovat pakattuja arkistoja, jotka voivat käyttää mitä tahansa tiedostokohtaista pakkausta, kuten [gzip](/compression/gz/), [bzip2](/compression/bz2/), lzo, xz tai lzma. DAR-tiedoston tarkka tiedostomuoto riippuu siitä, minkä tyyppistä muotoilua arkiston sisällön pakkaamiseen käytetään. Se mahdollistaa myös valinnaisen Blowfish-, Twofish-, AES-, Serpent-, Camellia-salauksen sekä julkisen avaimen salauksen ja allekirjoituksen (OpenPGP).

### DAR-ominaisuudet

Jotkut DAR-tiedostomuodon ominaisuuksista ovat seuraavat.

 * Hoitaa kaiken tyyppiset inodit (hakemisto, tavalliset tiedostot, symlinkit, erikoislaitteet, nimetyt putket, pistorasiat, ovet, ...)
 * Huolehtii kiinteästi linkitetyistä inodeista (kovalinkitetyt tavalliset tiedostot, char-laitteet, lohkolaitteet, kiinteät symlinkit)
 * Hoitaa harvat tiedostot
 * Huolehtii Linux-tiedoston laajennetuista määritteistä,
 * Hoitaa Linux-tiedoston ACL:n
 * Hoitaa Mac OS X -tiedostohaarukat
 * Huolehtii joistakin tiedostojärjestelmäkohtaisista määritteistä, kuten HFS+-tiedostojärjestelmän syntymäpäivä ja ext2/3/4-tiedostojärjestelmän muuttumattomat, datajournaling-, suojattu-poisto-, ei-tail-merging-, undeletable-, noatime-attribuutit.
 * Tiedostokohtainen pakkaus gzip-, bzip2-, lzo-, xz- tai lzma-ohjelmilla (toisin kuin koko arkiston pakkaaminen). Henkilö voi halutessaan olla pakkaamatta jo pakattuja tiedostoja tiedostonimen jälkiliitteen perusteella.
 * Tiedostojen nopea purkaminen mistä tahansa arkistosta
 * Nopea arkiston sisällön luettelointi tallentamalla tiedostoluettelo arkistoon
 * Live-tiedostojärjestelmän varmuuskopio: havaitsee, kun tiedostoa on muokattu, kun sitä luettiin varmuuskopiointia varten, ja voi yrittää tallentaa sen uudelleen tiettyyn enimmäismäärään asti
 * Hash-tiedosto (MD5, SHA1 tai SHA-512), joka on luotu lennossa kullekin viipaleelle. Tuloksena oleva tiedosto on yhteensopiva md5sumin tai sha1sumin kanssa, jotta kunkin siivun eheys voidaan tarkistaa nopeasti.
 * Tiedostojärjestelmästä riippumaton: sitä voidaan käyttää palauttamaan järjestelmä erikokoiseen osioon ja/tai osioon, jossa on eri tiedostojärjestelmä[5]

## Viitteet

* [DAR](http://dar.linux.free.fr/)

* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))


