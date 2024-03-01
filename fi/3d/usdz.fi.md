{
  "date": "2021-02-01",
  "keywords": [
"usdz",
"usdz tiedosto",
"usdz tiedostomuoto",
"tiedosto muoto",
"3d",
"usdz-tiedoston lataus"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USDZ - Universal Scene Description ZIP-muoto",
  "description": "Opi USDZ-tiedostomuodosta ja API-liittymistä, jotka voivat avata ja luoda USDZ-tiedostoja.",
  "linktitle": "USDZ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-usd-fiz"
}
},
  "lastmod": "2021-02-01"
}

## Mikä on USDZ-tiedosto?

.usdz-tiedosto on pakkaamaton ja salaamaton ZIP-arkisto [USD](/3d/usd/) (Universal Scene Description) -tiedostomuodolle, joka sisältää ja välityspalvelimet arkistoon upotettuja tiedostoja (kuten pintakuvioita ja animaatioita) varten ja suorittaa ne. suoraan USD-ajon aikana ilman tarvetta purkamiseen. USDZ-tiedostot ovat paketteja, joiden suunnittelu perustuu paketin uuteen Ar-tason abstraktioon. Usdz rekisteröitiin IANA:ssa ja sillä on mallin mediatyypin nimi ja alatyypin nimi vnd.usd+zip ja sen tiedot löytyvät osoitteesta [IANA registration page](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## USDZ tiedostomuoto

USDZ files are based on the ZIP file format that archive individual files in its container. This enables the receiver end to just unzip the contents and use the normal USD scene description files to work with and inspect. Almost all operating systems provide builtin support for the ZIP file formats and choosing this archiving format over any custom method makes it easy for USDZ files to be useful as a simple transport protocol.

### ZIP-rajoitukset

USDZ-tiedostomuoto käyttää ZIP-tiedostomuotoa ilman pakkausta ja salausta. Suunnittelun tarkoituksena oli täyttää kaksi vaatimusta:

 * Paketille, joka on jo ladattu muistiin tai yhtenä tiedostona levylle, API on saatavilla Yhdysvaltain dollareina kuvan sisältämien tietojen käyttöä varten.
 * Tiedostoja ei pitäisi purkaa levylle tai varata lisää keon tallennustilaa

USDZ:n kanssa nämä molemmat vaatimukset täyttyvät, koska useimmat kuvamuodot itsessään sallivat sisäisen pakkausmallin, mikä johtaa kompaktiin tiedostokoon.

### Asetteluvaatimukset

USDZ-paketit edellyttävät tiedostojen asettelua paketissa siten, että kunkin tiedoston tietojen tulee alkaa 64 tavun kerrannaisella paketin alusta. Paketin pitäisi kuitenkin alkaa alkuperäisellä [USD](/3d/usd/)-tiedostolla, jos paketti kohdistetaan yksinkertaisella viitteellä. Tässä tapauksessa tätä ensimmäistä USD-tiedostoa kutsutaan oletustasoksi. Asiakkaat, jotka haluavat toimittaa suoratoistoa mahdollistavaa sisältöä, saattavat haluta harkita myös muita asettelua koskevia rajoituksia.

## USDZ-tiedoston lataus
Koska usdz-tiedostot ovat täynnä muita korkealaatuisia kuvia ja usd-tiedostoja, ne voivat viedä enemmän levytilaa. Täältä löydät yksinkertaisen ja pienemmän USDZ-esimerkkitiedoston ladattavaksi:

- {{HYPERLINKKI1}}

## Viitteet

* [USDZ-tiedostomuodon tekniset tiedot](https://openusd.org/release/spec_usdz.html)


