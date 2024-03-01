{
  "date": "2021-07-29",
  "keywords": [
"md5 tiedosto",
"md5 tiedostomuoto",
"mikä on md5-tiedosto",
"tiedosto",
"md5 esimerkki",
"md5 tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MD5 - MD5-tarkistussummatiedosto",
  "description": "Opi MD5-tiedostoista ja sovellusliittymistä, jotka voivat luoda ja avata MD5-tiedostoja.",
  "linktitle": "MD5",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-md-fi5"
}
},
  "lastmod": "2021-07-29"
}

## Mikä on MD5-tiedosto?

MD5-tiedosto on tarkistussummatiedosto, jota käytetään tiedoston eheyden tarkistamiseen. Se on samanlainen kuin liitetyn tiedoston sormenjälki, ja se luodaan yksilöllisesti käyttämällä algoritmia, joka käyttää tiedoston bittien määrää. Sitä käytetään tiedoston tarkistamiseen ohjelmistolla, kuten {{HYPERLINKKI}}. Yksi MD5-tiedostojen käytön etu on varmistaa, että ladatut tiedostot eivät ole vioittuneet.

## MD5-tiedostomuoto – lisätietoja

Yleensä MD5-tiedosto tallennetaan samalla nimellä kuin alkuperäinen tiedostonimi, mutta tunnisteella .md5. Jos esimerkiksi liitetty tiedostonimi on abc_987_123456.grb, vastaava MD5-tiedoston nimi on abc_987_123456.grb.md5. MD5-tiedostot auttavat tunnistamaan, että vastaanotettu tai ladattu tiedosto ei ole vioittunut tai haitallinen sisältö ei vaikuta siihen. Lyhyesti sanottuna MD5-tiedostot takaavat tiedoston täydellisyyden.


## Kuinka tarkistaa MD5-tarkistussumma?

Yksittäinen tiedosto voidaan tarkistaa/varmentaa MD5:lle käyttämällä [md5sum](https://en.wikipedia.org/wiki/Md5sum)-työkalua seuraavasti.

```
md5sum -c abc_987_123456.grb.md5
```

## Viitteet

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)


