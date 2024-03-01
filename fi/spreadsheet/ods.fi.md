{
  "date": "2019-12-10",
  "keywords": [
"ODS",
"tiedosto",
"laajennus",
"tiedosto muoto",
"OpenDocument-laskentataulukko"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Tiedostomuoto-opas tietää, mikä on ODS-tiedosto ja API:t, jotka voivat luoda ja avata niitä.",
  "title": "Mikä on ODS-tiedosto? ",
  "linktitle": "ODS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-od-fis"
}
},
  "lastmod": "2019-12-10"
}

## Mikä on ODS-tiedosto?

Tiedostot, joiden laajennus on .ods, tarkoittavat OpenDocument Spreadsheet Document -muotoa, jota käyttäjä voi muokata. Tiedot tallennetaan ODF-tiedostoon riveihin ja sarakkeisiin. Se on XML-pohjainen muoto ja yksi useista Open Document Formats (ODF) -perheen alatyypeistä. Muoto on määritetty osana OASIS:n julkaisemia ja ylläpitämiä ODF 1.2 -määrityksiä. Useat Windows-sovellukset ja muut käyttöjärjestelmät voivat avata ODS-tiedostoja muokkausta ja käsittelyä varten, mukaan lukien Microsoft Excel, NeoOffice ja LibreOffice. ODS-tiedostoja voidaan myös muuntaa muihin laskentataulukkomuotoihin, kuten [XLS](/spreadsheet/xls/), [XLSX](/spreadsheet/xlsx/) ja muihin eri sovelluksilla.

## Lyhyt historia ##

ODS-tiedostomuotomääritykset perustuvat standardiin, joka on kehitetty ODF-spesifikaatioina. Nämä spesifikaatiot ovat kehittyneet menneisyydessä kolmena versiona, jotka OASIS on kehittänyt ja julkaissut seuraavasti:

2005 - Versio 1.0 julkaistiin toukokuussa 2005

`2007` - Versio 1.1 julkaistiin helmikuussa 2007

`2011` - Versio 1.2 julkaistiin syyskuussa 2011

ODF 1.0:sta 1.1:een siirtymisessä tehtiin melko pieniä muutoksia. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) on ODF-määritysten uusin versio, ja kehittäjien tulee kuulla sitä ODS-luku-/kirjoitussovellusten kehittämisessä.

## ODS-tiedostomuoto ##

OpenDocument-muoto tukee asiakirjan esittämistä yhtenä XML-asiakirjana sekä useiden aliasiakirjojen kokoelmaa paketissa [ZIP](/compression/zip/)-arkistona. Jokainen ZIP-arkiston tiedosto tallentaa osan koko asiakirjasta. Jokainen aliasiakirja tallentaa asiakirjan tietyn osan. Esimerkiksi yksi aliasiakirja sisältää tyylitiedot ja toinen aliasiakirja dokumentin sisällön. Tyypillisessä ODF-asiakirjassa on seuraavat osat:

* `content.xml` – Asiakirjan sisältö ja sisällössä käytetyt automaattiset tyylit.

* `styles.xml` – Asiakirjan sisällössä käytetyt tyylit ja itse tyyleissä käytetyt automaattiset tyylit.

* `meta.xml` – Asiakirjan metatiedot, kuten tekijä tai viimeisimmän tallennustoiminnon aika.

* `settings.xml` – Sovelluskohtaiset asetukset, kuten ikkunan koko tai tulostintiedot.


Näiden lisäksi paketissa voi olla monia muita aliasiakirjoja, kuten asiakirjan pikkukuva, kuvat jne.

Laskentataulukko-asiakirjatiedostot ovat ODF-tiedostojen osajoukko, johon sisältö (taulukot) on tallennettu content.xml-aliasiakirjaan.

## Viitteet ##

* [OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


