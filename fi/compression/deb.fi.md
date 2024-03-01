{
  "date": "2021-04-08",
  "keywords": [
"deb-tiedosto",
"deb-tiedostomuoto",
"mikä on deb-tiedosto",
"tiedosto",
"deb esimerkki",
"deb tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DEB - Bzip-pakattu terva-arkisto",
  "description": "Opi DEB-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DEB-tiedostoja.",
  "linktitle": "DEB",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-de-fib"
}
},
  "lastmod": "2021-04-09"
}

## Mikä on DEB-tiedosto?

Tiedosto, jonka laajennus on .deb, on Debianin binaaripakettitiedostomuoto, joka on saatavana ohjelmistopakettien jakeluun Linux-käyttöjärjestelmässä. Se koostuu kahdesta [TAR](/compression/tar/)-arkistotiedostosta. DPKG tarjoaa mekanismin DEB-pakettien lukemiseen ja asentamiseen. DEB-paketit voidaan asentaa APT-pakettien ohjelmistonhallintaliittymän avulla. DEB-tiedostojen Internet-mediatyyppi on application/vnd.debian.binary-package.

## DEB-tiedostomuoto

DEB-tiedosto koostuu kahdesta [TAR](/compression/tar/)-arkistotiedostosta. Yksi arkisto sisältää ohjaustiedot ja toinen asennettavat tiedot.

### Pakettiorganisaatio

DEB-tiedosto on **ar**-arkistotiedosto, jonka maaginen arvo on `!<arch> `. Debian 0.93:sta lähtien DEB-tiedostojen arkistointimekanismi sisältää kolme tiedostoa tietyssä järjestyksessä.

 1. `Debian Binary` - Sillä on rivi rivinvaihtoriveillä erotettuina. Tällä hetkellä vain yksi rivi, joka kuvaa versionumeroa. Nykyinen versionumero on 2.0.
 1. Ohjausarkisto - Se sisältää control.tar-arkiston, jossa on ylläpitäjän komentosarjoja ja metatietoja paketista, kuten paketin nimi, versio, riippuvuudet ja ylläpitäjä.
 1. `Data Archive` - Se on data.tar-niminen tar-arkisto, joka sisältää todelliset asennettavat mediatiedostot. Arkisto voidaan pakata komennoilla gz, bz2, lzma tai xz, ja tietoarkiston tiedostopääte muuttuu vastaavasti.

### Ohjausarkisto

Ohjausarkisto voi sisältää seuraavanlaista sisältöä.

 * `control` - It contains a brief description of the package as well as other information such as its dependencies.
 * md5sums - Se sisältää MD5-tarkistussummat kaikista paketissa olevista tiedostoista viallisten tai epätäydellisten tiedostojen havaitsemiseksi.
 * `conffiles` - Se luettelee paketin tiedostot, joita tulee käsitellä asetustiedostoina. Kokoonpanotiedostoja ei kirjoiteta päälle päivityksen aikana, ellei toisin mainita.
 * preinst, postinst, prerm ja postrm - Valinnaiset komentosarjat, jotka suoritetaan ennen paketin asentamista tai poistamista tai sen jälkeen
 * config on valinnainen komentosarja, joka tukee debconf-määritysmekanismia.
 * shlibs - Se on luettelo jaetuista kirjastojen riippuvuuksista.

## Viitteet

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))

* [Debianin binaaripakettimuoto](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)


