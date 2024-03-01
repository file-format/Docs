{
  "date": "2019-12-10",
  "keywords": [
"XLTM",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Excel Open XML-makro",
"Laskentataulukko"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Tiedostomuoto-opas tietää, mikä on XLTM-tiedosto ja API:t, jotka voivat luoda ja avata niitä.",
  "title": "Mikä on XLTM-tiedosto?",
  "linktitle": "XLTM",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xlt-fim"
}
},
  "lastmod": "2019-12-10"
}

## Mikä on XLTM-tiedosto?

XLTM-tiedostotunniste edustaa tiedostoja, jotka on luotu Microsoft Excelillä makropohjaisina mallitiedostoina. XLTM-tiedostot ovat rakenteeltaan samankaltaisia kuin [XLTX](/spreadsheet/xltx/), paitsi että myöhempi ei tue mallitiedostojen luomista makrojen kanssa. Tällaisia mallitiedostoja käytetään asettelun, muotoilun ja muiden asetusten luomiseen ja asettamiseen yhdessä makrojen kanssa samanlaisten XLSX-tiedostojen luomisen helpottamiseksi.

## Lyhyt historia ##

Vuoden 2000 alussa Microsoft päätti tehdä muutoksen mukauttaakseen **Office Open XML -standardin**. Tämän uuden standardin mukaiset erityyppiset asiakirjat tunnistettiin lisäämällä X niiden laajennuksiin, missä X tarkoittaa XML:ää. Vuoteen 2007 mennessä tämä uusi tiedostomuoto tuli osaksi Office 2007:ää, ja sitä käytetään myös Microsoft Officen uusissa versioissa. Uusi tiedostotyyppi on lisännyt etuja: pienet tiedostokoot, vähemmän muutoksia korruptiossa ja hyvin muotoiltujen kuvien esitys.

## XLTM-tiedostomuodon tekniset tiedot ##

XLTM-tiedostot perustuvat Office OpenXML -tiedostomuotoon ja käyttävät XML:ää ja [ZIP](/compression/zip/) pienentämään tiedostokokoa. Ne voidaan avata Microsoft Excelillä kaksoisnapsauttamalla tiedostoa. Tiedostojen järjestystä XLTM-tiedostomuodossa voi tarkkailla nimeämällä tiedosto uudelleen ZIP:ksi ja purkamalla sen sisältö levylle.

### [Content_Types].xml ###

Tämä on ainoa tiedosto, joka löytyy perustasolta, kun zip-tiedosto puretaan. Siinä luetellaan paketin osien sisältötyypit. Kaikki viittaukset paketin XML-tiedostoihin viitataan tässä XML-tiedostossa.

### \_rels (kansio) ###

Tämä on Relationships-kansio, joka sisältää yhden XML-tiedoston, joka tallentaa pakettitason suhteet. Linkit Xltx-tiedostojen tärkeimpiin osiin sisältyvät tähän tiedostoon URI-tunnuksina. Nämä URI:t tunnistavat kunkin avainosan ja paketin suhteen tyypin. Tämä sisältää suhteen ensisijaiseen toimistoasiakirjaan, joka sijaitsee muodossa xl/workbook.xml, ja muita docPropsin osia ydin- ja laajennettuina ominaisuuksina.

### docProps ###

Tämä kansio sisältää asiakirjan yleiset ominaisuudet. Näitä ovat joukko ydinominaisuuksia, joukko laajennettuja tai sovelluskohtaisia ominaisuuksia ja asiakirjan esikatselu. Tyhjässä työkirjassa on kaksi tiedostoa tässä kansiossa, nimittäin app.xml ja core.xml. core.xml sisältää tietoja, kuten tekijä, luonti- ja tallennuspäivämäärä sekä muokkaus. App.xml sisältää tietoja tiedoston sisällöstä.

### xl (kansio) ###

Tämä on pääkansio, joka sisältää kaikki tiedot työkirjan sisällöstä. Oletuksena siinä on seuraavat kansiot:

* \_rels

* teema

* laskentataulukoita


ja seuraavat xml-tiedostot:

* styles.xml

* työkirja.xml


## Viitteet ##

* [MS-XLSX-tiedostomuoto](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


