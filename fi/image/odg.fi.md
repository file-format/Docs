{
  "date": "2019-10-11",
  "keywords": [
"odg tiedosto",
"odg-tiedostomuoto",
"mikä on odg-tiedosto",
"tiedosto",
"outo esimerkki",
"odg tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODG tiedostomuoto",
  "description": "Opi ODG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ODG-tiedostoja.",
  "linktitle": "ODG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-od-fig"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on ODG-tiedosto?

Apache OpenOfficen Draw-sovellus käyttää ODG-tiedostomuotoa piirustuselementtien tallentamiseen vektorikuvana. Se noudattaa Advancement of Structural Information Standards (OASIS) -standardien XML-pohjaisia tiedostomuotomäärityksiä. ODG esittää piirustuksia vektorikuvina käyttämällä pisteitä, viivoja ja käyriä. OpenOfficen lisäksi LibreOffice ja muut sovellukset tukevat myös ODG-tiedostomuodon käyttöä. Muita OpenOfficen tukemia muotoja ovat esimerkiksi [ODT](/word-processing/odt/), ODF, [ODP](/presentation/odp/) ja [ODS](/spreadsheet/ods/).


## ODG-tiedostomuodon tekniset tiedot

ODG-tiedostomuoto perustuu OpenDocument-muotoon, joka on strukturoitu XML-dokumenttimuoto, jossa on hyvin määritelty kaava.
OpenDocument-muodon jokaista rakennekomponenttia edustaa elementti, jolla on siihen liittyviä attribuutteja. XML-pohjainen rakenne on yhteinen kaikille asiakirjatyypeille, kuten tekstiasiakirjalle, laskentataulukolle tai piirustustiedostolle. Asiakirja voi sisältää erilaisia tyylejä. OpenDocument-tiedostorakenne koostuu seuraavista elementeistä.
  * Asiakirjan juuri
  * Asiakirjan metatiedot
  * Runkoelementti ja asiakirjatyypit
  * Sovellusasetukset
  * Käsikirjoitukset
  * Fontin kasvojen ilmoitukset
  * Tyylit
  * Sivutyylit ja asettelut

##  Asiakirjan juuret ##

Asiakirjan juurielementti sisältää koko asiakirjan ja on OpenDocument-muodossa olevan tiedoston ensisijainen elementti. Samantyyppisiä asiakirjan juurielementtejä voidaan soveltaa kaikentyyppisiin asiakirjoihin, kuten tekstiin, asiakirjoihin, laskentataulukoihin ja piirustusasiakirjoihin.

### Juurielementit ###
Yksittäistä XML-dokumenttia edustaa sen oma juurielementti. Viisi erilaista tuettua juurielementtiä ovat seuraavat.

`<office:document> ` - Täydellinen Office-asiakirja yhdessä XML-asiakirjassa.
`<office:document-content> ` - Asiakirjan sisältö ja sisällössä käytetyt automaattiset tyylit.
`<office:document-styles> ` - Asiakirjan sisällössä käytetyt tyylit ja itse tyyleissä käytetyt automaattiset tyylit.
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings> ` - Sovelluskohtaiset asetukset, kuten ikkunan koko tai tulostintiedot.

### ODG-asiakirjan metatiedot ###
The OpenDocument contains all metadata elements in the \<office:meta> element. This general information about a document is contained at the start of the document and applications can update multiple instances of the same elements.

### Runkoelementit ja asiakirjatyypit ###
Asiakirjan runko ilmaisee asiakirjan sisältämän sisällön tyypin käyttämällä asiakirjatyyppielementtiä. Nämä asiakirjatyypit ovat:
  * tekstiasiakirjoja
  * asiakirjojen piirtäminen
  * esittelyasiakirjoja
  * laskentataulukkoasiakirjoja
  * kaaviodokumentit
  * kuvadokumentteja

### Sovellusasetukset ###
The settings for office applications represent different settings that are related to the document configuration or visual appearance of the document. Each category is represented by a `<config:config-item-set>`. Examples of such setting categories include:
  * Asiakirjan asetukset esim. oletustulostin
  * Näytä Asetukset esim. zoomaustaso

### Käsikirjoitukset ###
It is common for a document to contain several scripts. Each script in an OpenDocument file is represented by an `<office:script>` element. These script elements are contained in a single `<office:scripts>` element. Scripts do not update a document while the document is loading.
### Fontin kasvojen ilmoitukset ###

Fontin kasvojen ilmoitus sisältää tietoja dokumentin kirjoittajan käyttämistä fonteista. Nämä tiedot auttavat löytämään nämä kirjasimet muista järjestelmistä.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Tyylit ###
OpenDocument-muoto tukee seuraavia tyylejä.

Yleiset tyylit - Tällaisten tyylien XML-esityksiä kutsutaan tyyleiksi
Automaattiset tyylit - Sisältää muotoiluominaisuudet, jotka asiakirjan käyttöliittymänäkymässä on määritetty objektille, kuten kappaleelle.
Mater Styles - yleinen tyyli, joka sisältää muotoilutietoja ja lisäsisältöä, joka näytetään asiakirjan sisällön kanssa, kun tyyliä käytetään. Esimerkki mestarityylistä ovat sivupohjat.

## Viitteet ##
  * [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
  * [OpenDocument-muoto – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

