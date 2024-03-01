{
  "date": "2021-04-21",
  "keywords": [
"hernetiedosto",
"herne tiedostomuoto",
"mikä on hernetiedosto",
"tiedosto",
"herne esimerkki",
"pea tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PEA - PeaZip-arkiston tiedostomuoto",
  "description": "Opi PEA-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PEA-tiedostoja.",
  "linktitle": "PEA",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-pe-fia"
}
},
  "lastmod": "2021-04-21"
}

## Mikä on PEA-tiedosto?

Tiedosto, jonka pääte on .pea, lyhenne sanoista Pack, Encrypt ja Authenticate, on [zip](/compression/zip/)-arkisto, joka on luotu [PeaZip](https://peazip.github.io/)-arkistointiohjelmistolla. Siinä on pakkaus ja useita tilavuuksia, ja se tarjoaa joustavan suojausmallin Authenticated Encryption ja kryptografian avulla. Tämä tarjoaa sekä yksityisyyden että tietojen todennuksen. PeaZip-apuohjelma on saatavana avoimen lähdekoodin moottorina, joka voidaan kääntää eri käyttöjärjestelmille vaatimusten mukaan.

## PEA-tiedostomuoto

[PEA file format specifications](https://peazip.github.io/pea_help.pdf) ovat julkisesti saatavilla kehittäjille. PEA-arkistot ovat binääritiedostoja, joissa on joustava suojausmalli ja redundanttiset eheystarkistukset, jotka vaihtelevat tarkistussummista kryptografisesti vahvoihin tiivisteisiin. Tämä määrittelee kolme erilaista hallittavan viestinnän tasoa:

 * Virrat - todellinen ulostulodatavirta, joka muodostuu useista tulotiedostoista ja voidaan kirjoittaa useisiin lähtötaltioihin
 * Objektit - syöttötiedostot ja kansiot, jotka lähetetään .pea-arkistoon
 * Volumes - tulostusarkistotiedosto, joka voidaan laajentaa käyttäjän määrittelemään kokoon

Jokainen näistä on valinnainen ja voidaan sisällyttää käyttäjän vaatimusten mukaan. PEA-tiedostomuoto voi tallentaa yhden virran, joka sisältää rajattomasti objekteja. Jokainen virta on kooltaan enintään 2^64 tavua.

PEA-tiedostot tarjoavat valinnaisen eheyden tarkistuksen ja todennettua salausta käyttämällä AES-salausta EAX- tai HMAC-tilassa, vaihtoehtoisesti Twofish ja Serpent EAX-tilassa.

### PEA-arkiston otsikko

Arkiston otsikko on 10 tavua pitkä ja rakenteeltaan seuraava.

|Bytes|Kuvaus|
---|---|
|1 | Maaginen tavukenttä tiedostomuodon yksiselitteistämiseen: $EA|
|1 | Versionumero|
|1 | Versionumero|
|1 | Äänenvoimakkuuden säätöjärjestelmä|
|1 | Ilmoitetaan käyttöjärjestelmä, jossa stream rakennettiin|
|1 | Käyttöjärjestelmän päivämäärän ja kellonajan koodauksen ilmoittaminen|
|1 | Ilmoitetaan objektien nimi merkkien koodaus|
|1 | Prosessorin tyypin (7-bittisesti koodattu) ja endiannessin (msb:ssä) ilmoittaminen|
|1 | Varattu tulevaa käyttöä varten|

## Viitteet

* [PEA-tiedostomuodon tekniset tiedot](https://peazip.github.io/pea_help.pdf)

* [PEA-tiedostomuoto](https://peazip.github.io/pea-file-format.html#.pea_specifications)


