{
  "date": "2019-10-11",
  "keywords": [
"odt tiedosto",
"odt tiedostomuoto",
"mikä on odt-tiedosto",
"tiedosto",
"outo esimerkki",
"odt tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODT - OpenDocument-tekstitiedosto",
  "description": "Opi ODT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ODT-tiedostoja.",
  "linktitle": "ODT",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-od-fit"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on ODT-tiedosto?

ODT-tiedostot ovat OpenDocument-tekstitiedostomuotoon perustuvilla tekstinkäsittelysovelluksilla luotuja asiakirjoja. Nämä luodaan tekstinkäsittelyohjelmilla, kuten ilmaisella OpenOffice Writerillä, ja ne voivat sisältää sisältöä, kuten tekstiä, kuvia, objekteja ja tyylejä. ODT-tiedosto on Writerin tekstinkäsittelyohjelmalle sama kuin {{HYPERLINKKI}} Microsoft Wordille. Useat sovellukset, kuten Google Docs ja Googlen verkkopohjainen tekstinkäsittelyohjelma, jotka sisältyvät Google Driveen, voivat avata ODT-tiedostoja muokkausta varten. Microsoft Word voi myös avata ODT-tiedostoja ja tallentaa ne muihin muotoihin, kuten [DOC](/word-processing/doc/) ja DOCX.

## Lyhyt historia ##

ODP-tiedostomuotomääritykset perustuvat standardiin, joka on kehitetty ODF-spesifikaatioina. Nämä spesifikaatiot ovat kehittyneet menneisyydessä kolmena versiona, jotka OASIS on kehittänyt ja julkaissut seuraavasti:

**2005** Versio 1.0 julkaistiin toukokuussa 2005

**2007:** Versio 1.1 julkaistiin helmikuussa 2007

**2011:** Versio 1.2 julkaistiin syyskuussa 2011

ODF 1.0:sta 1.1:een siirtymisessä tapahtui melko pieniä muutoksia. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) on ODF-määritysten uusin versio, ja kehittäjien tulee kuulla sitä ODS-luku-/kirjoitussovellusten kehittämisessä.

## Tiedostomuodon tiedot ##

OpenDocument-muoto tukee asiakirjan esittämistä yhtenä XML-asiakirjana sekä useiden aliasiakirjojen kokoelmaa paketissa [ZIP](/compression/zip/)-arkistona. Jokainen ZIP-arkiston tiedosto tallentaa osan koko asiakirjasta. Jokainen aliasiakirja tallentaa asiakirjan tietyn osan. Esimerkiksi yksi aliasiakirja sisältää tyylitiedot ja toinen aliasiakirja dokumentin sisällön. Tyypillisessä ODF-asiakirjassa on seuraavat osat:

* content.xml – Asiakirjan sisältö ja sisällössä käytetyt automaattiset tyylit.

* styles.xml – Asiakirjan sisällössä käytetyt tyylit ja itse tyyleissä käytetyt automaattiset tyylit.

* meta.xml – Asiakirjan metatiedot, kuten tekijä tai viimeisimmän tallennustoiminnon aika.

* settings.xml – Sovelluskohtaiset asetukset, kuten ikkunan koko tai tulostintiedot.


Näiden lisäksi paketissa voi olla monia muita aliasiakirjoja, kuten asiakirjan pikkukuvat, kuvat jne. Asiakirjatiedostot ovat ODF-tiedostojen osajoukko, johon sisältö (arkit) on tallennettu //content.xml//-aliasiakirjaan.

## Viitteet ##

* [OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


