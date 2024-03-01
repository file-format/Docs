{
  "date": "2019-10-11",
  "keywords": [
"fodg-tiedosto",
"fodg-tiedostomuoto",
"mikä on fodg-tiedosto",
"tiedosto",
"fodg esimerkki",
"fodg tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FODG - OpenDocument-piirustustiedostomuoto",
  "description": "Opi FODG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata FODG-tiedostoja.",
  "linktitle": "FODG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-fod-fig"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on FODG-tiedosto?

Tiedosto, jonka pääte on .fodg, on Apache OpenOffice Drawing -tiedostomuoto piirustuselementtien tallentamiseen. Se perustuu Advancement of Structural Information Standardsin (OASIS) määrittelemiin tiedostomuotomäärittelyihin. Toinen samanlainen tiedostomuoto OpenOffice-grafiikkaan on {{HYPERLINKKI}}, joka tallentaa piirustuselementit vektorikuvana. FODG-tiedostoja voidaan avata sekä OpenOfficen että LibreOfficen avulla. Muita OpenOfficen tukemia tiedostomuotoja ovat esimerkiksi [ODT](/word-processing/odt/), ODF, [ODP](/presentation/odp/) ja [ODS](/spreadsheet/ods/).

## FODG tiedostomuoto

FODG is based on the OpenDocument's XML file format that conforms to OASIS OpenDocument Format ISO/IEC 26300. Siinä on Internet Media Type -sovellus/vnd.oasis.opendocument.graphics ja se on myös org.oasis-open.opendocument public.composite-content -sisällön mukainen. XML-rakenne on yhteinen kaikille asiakirjatyypeille, kuten laskentataulukoille, piirustustiedostoille ja tekstiasiakirjoille. OpenOffice-dokumentit hyödyntävät huolenaiheiden erottamista erottamalla sisällön, tyylit, metatiedot ja sovellusasetukset neljään erilliseen XML-tiedostoon.

`<office:document-content> ` - Asiakirjan sisältö ja sisällössä käytetyt automaattiset tyylit.
`<office:document-styles> ` - Asiakirjan sisällössä käytetyt tyylit ja itse tyyleissä käytetyt automaattiset tyylit.
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings> ` - Sovelluskohtaiset asetukset, kuten ikkunan koko tai tulostintiedot.

## Viitteet ##
 * [Future Specifications for v 1.3 Standardization ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
 * [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
 * [OpenDocument-muoto – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

