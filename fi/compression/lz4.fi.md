{
  "date": "2021-04-08",
  "keywords": [
"lz4 tiedosto",
"lz4 tiedostomuoto",
"mikä on lz4-tiedosto",
"tiedosto",
"lz4 esimerkki",
"lz4 tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZ4 - LZ4 pakattu tiedostomuoto",
  "description": "Opi LBR-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata LZ4-tiedostoja.",
  "linktitle": "LZ4",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lz-fi4"
}
},
  "lastmod": "2021-04-19"
}

## Mikä on LZ4-tiedosto?

Tiedosto, jonka pääte on .lz4, on pakattu arkistotiedosto, joka on luotu sovelluksilla/apuohjelmilla, jotka tukevat {{HYPERLINKKI}})-pakkausta. LZ4-algoritmi keskittyy nopeuden ja pakkaussuhteen väliseen kompromissiin. Pakatut LZ4-arkistot voidaan luoda käyttämällä LZ4-komentoriviohjelmaa, ja ne voidaan purkaa samalla.

## LZ4 tiedostomuoto

LZ4-tiedostomuoto, joka perustuu LZ4-pakkausalgoritmiin, on riippumaton suorittimen tyypistä, käyttöjärjestelmästä, tiedostojärjestelmästä ja merkistöstä. Se soveltuu tiedostojen pakkaamiseen ja suoratoistopakkaukseen LZ4-algoritmilla. Yann Collet toteutti LZ4-muodon ensimmäisen käyttöönoton [C](/programming/c/)-kielellä vuonna 2011, ja se on saatavilla kehittäjien viitteeksi osoitteessa [Github](https://github.com/lz4/lz4).

### LZ4-kehysmuoto

LZ4-tiedostomuodon yleinen rakenne on alla kuvattu.

|MagicNb|F. Kuvaaja| Lohko|(...)|Loppumerkki |C. Tarkistussumma|
---|---|---|---|---|---|
|4 tavua| 3-15 tavua||| 4 tavua| 0-4 tavua|

#### Maaginen numero

4 tavua, Little Endian -muoto. Arvo: 0x184D2204

#### Kehyksen kuvaus

Kehyskuvaaja koostuu 3 t0 15 tavusta ja on spesifikaatioiden tärkein osa. Yhdessä Magic_Number- ja Frame_Descriptor-kentistä käytetään nimitystä LZ4 Frame Header, ja sen koko vaihtelee 7-19 tavua. Se on alla olevan kuvan mukainen.

|FLG| BD| (Sisällön koko)| (Sanakirjan tunnus)| HC|
---|---|---|---|---|
|1 tavu| 1 tavu| 0 - 8 tavua| 0 - 4 tavua| 1 tavu|

#### Tietolohkot

Jokainen tietolohko noudattaa seuraavaa järjestystä.

|Lohkon koko| data| (Block Checksum)|
---|---|---|
|4 tavua| |0 - 4 tavua|

#### EndMark

Lohkojen kulku päättyy, kun viimeistä datalohkoa seuraa 32-bittinen arvo 0x00000000.

#### Sisällön tarkistussumma

Content_Checksum varmistaa oikein dekoodattavan sisällön oikeellisuuden ja suoritetaan käyttämällä xxHash-32-algoritmin tulosta. Se vahvistaa kaikkien lohkojen onnistuneen lähetyksen tulokset oikeassa järjestyksessä ja ilman virheitä.

## Viitteet

* [LZ4-kehysmuoto](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)

* [LZ4 Compression Algorithm - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))


