{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ZST-tiedosto - Zstandardi pakattu tiedostomuoto",
  "description":"Opi ZST-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ZST-tiedostoja.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-fi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Mikä on ZST-tiedosto?

ZST-tiedosto on pakattu tiedosto, joka luodaan Zstandardin (zstd) pakkausalgoritmilla. Se on pakattu tiedosto, joka on luotu algoritmin häviöttömällä pakkauksella. ZST-tiedostoja voidaan käyttää erityyppisten tiedostojen, kuten tietokantojen, tiedostojärjestelmien, verkkojen ja pelien, pakkaamiseen. Z-standardia hallitsee [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878), joka kuvaa yleisen pakkausmekanismin, mediatyypin ja sisällön koodauksen.

## ZST tiedostomuoto

ZST-tiedostot tallennetaan levylle pakatussa tiedostomuodossa. Pakkausmekanismi on RFC 8878:n kuvaama, joka vanhenee RFC 8478:n.

## ZST kehykset

ZST-tiedosto koostuu yhdestä tai useammasta kehyksestä. Jokainen kehys voi olla joko Zstandardikehys tai ohitettava kehys. Zstandardikehys sisältää pakattua dataa, kun taas ohitettava kehys sisältää mukautettuja käyttäjän metatietoja.

### Zstandardikehys

Zstandardikehyksellä on seuraava rakenne.

|Kenttä|Koko tavuina|
---|---|
|Magic_Number |4 tavua|
|Frame_Header |2-14 tavua|
|Data_Block |n tavua|
|[Lisää tietolohkoja] ||
|[Content_Checksum] |4 tavua|

### Ohitettava kehys

Ohitettava kehys mahdollistaa käyttäjän määrittämien metatietojen lisäämisen ketjutettujen kehysten virtaan. Ohitettavan kehyksen rakenne on seuraava.

|Magic_Number |Frame_Size |Käyttäjätiedot|
---|---|---|
|4 tavua |4 tavua |n tavua|

## Viitteet ##

* [RFC 8878 Zstandard Compression](https://www.rfc-editor.org/rfc/rfc8878)


