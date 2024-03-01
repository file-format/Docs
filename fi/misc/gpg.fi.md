{
  "date": "2022-02-17",
  "keywords": [
"gpg-tiedosto",
"gpg-tiedostomuoto",
"mikä on gpg-tiedosto",
"tiedosto",
"gpg esimerkki",
"gpg tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GPG-tiedosto - GNU Privacy Guardin julkinen avaimenperätiedosto",
  "description": "Opi GPG-tiedostoista ja sovellusliittymistä, jotka voivat luoda ja avata GPG-tiedostoja.",
  "linktitle": "GPG",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-gp-fig"
}
},
  "lastmod": "2022-02-17"
}

## Mikä on GPG-tiedosto?

GPG-tiedosto on salaus-/salauksenpurkuavaintiedosto, jota GNU Privacy Guard (GnuPG) -salausohjelma käyttää. Itse GnuPC-ohjelma perustuu OpenPGP-standardiin, sellaisena kuin se on määritelty RFC4880:na ja tunnetaan myös nimellä PGP. Avain GPG:n menestyksekkääseen käyttöön nykyaikaisessa käyttöjärjestelmässä on sen monipuolinen avaintenhallintajärjestelmä. GPG:n komentorivityökalu mahdollistaa sen helpon integroinnin muihin sovelluksiin.

## GPG tiedostomuoto

GPG-tiedostot tallennetaan salattuina binääritiedostoina, eivätkä tietenkään ole ihmisen luettavissa. Jos haluat purkaa salatun GPG-tiedoston, sinun on käytettävä samaa suojattua avainta. Ja siksi näiden tiedostojen sisäistä tiedostomuotoa ei tunneta.

## Salaa ja pura tiedostot GPG:llä Linuxissa

GPG-komentorivi-apuohjelmaa voidaan käyttää tiedostojen salaamiseen ja salauksen purkamiseen Linuxissa.

### Tiedoston salaus

Tiedosto voidaan salata gpg-komennolla ja -c (create) -vaihtoehdolla alla olevan kuvan mukaisesti.

```
gpg -c file1.txt
```
Tämän komennon suorittaminen pyytää avainlausetta, jolla alkuperäisen tiedoston file1.txt sisältö salataan. Tämä johtaa salatun tiedoston tiedosto1.txt.gpg luomiseen.

### Tiedoston salauksen purkaminen ja purkaminen

Salatun tiedoston salauksen purkamiseksi ja purkamiseksi voidaan käyttää seuraavaa komentoa.

```
gpg cfile.txt.gpg
```

## Viitteet

* [GNUPG](https://gnupg.org/)

* [HDF – Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)


