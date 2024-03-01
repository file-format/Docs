{
  "date": "2022-01-23",
  "keywords": [
"xz tiedosto",
"tiedosto muoto",
"mikä on xz-tiedosto",
"tiedosto",
"xz esimerkki",
"xz tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XZ-tiedosto - XZ-pakattu arkisto",
  "description": "Opi XZ-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata XZ-tiedostoja.",
  "linktitle": "XZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-x-fiz"
}
},
  "lastmod": "2022-01-23"
}

## Mikä on XZ-tiedosto?

XZ on pakattu tiedostomuoto, joka käyttää LZMA2-pakkausalgoritmia. Se on suunniteltu korvaamaan suosittuja gzip- ja bzip2-muotoja, ja se tarjoaa useita etuja näihin vanhempiin standardeihin verrattuna. XZ-tiedostot ovat hyvin tuettuja monilla alustoilla, ja ne voidaan purkaa nopeasti ja helposti. Vaikka XZ-arkistot eivät ole yhtä yleisiä kuin [ZIP](/compression/zip/)- tai [RAR](/compression/rar/)-tiedostot, niitä voidaan käyttää suurten tietomäärien tallentamiseen pakkauslaadusta tinkimättä. Jos sinun on pakattava tai purettava suuria tiedostoja, XZ-tiedostotunniste kannattaa harkita.

## XZ tiedostomuoto

XZ-tiedostot luodaan ja tallennetaan binääritiedostoina levylle. Se käyttää LZMA-algoritmia tietojen pakkaamiseen ja voi saavuttaa jopa 50 %:n pakkaussuhteen. XZ-tiedostoja käytetään yleensä ohjelmistojakeluihin ja varmuuskopioarkistoihin. Ne voidaan purkaa XZ-apuohjelmalla, joka sisältyy useimpiin Linux-jakeluihin.

## Pura XZ-tiedostot Linuxissa/Unixissa

Jos haluat purkaa XZ-tiedostot, asenna paketti `xz-utils' ensin:
```
$ sudo apt-get install xz-utils
```

Käytä unxz-komentoa .xz-tiedostojen purkamiseen:
```
$ unxz compressed_xz_file.xz
```

tai käyttämällä XZ:n --decompress-vaihtoehtoa:
```
$ xz --decompress compressed_xz_file.xz
```

## Viitteet

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)


