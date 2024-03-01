{
  "date": "2019-12-10",
  "keywords": [
"XLTX",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Excel Open XML",
"Laskentataulukko"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Tiedostomuoto-opas tietää, mikä on XLTX-tiedosto ja API:t, jotka voivat luoda ja avata niitä.",
  "title": "Mikä on XLTX-tiedosto?",
  "linktitle": "XLTX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xlt-fix"
}
},
  "lastmod": "2019-12-10"
}

## Mikä on XLTX-tiedosto?

Tiedostot, joiden tiedostotunniste on .xltx, edustavat Microsoft Excel -mallitiedostoja, jotka perustuvat Office OpenXML -tiedostomuotomäärityksiin. Sitä käytetään luomaan vakiomallitiedosto, jota voidaan käyttää [XLSX](/spreadsheet/xlsx/)-tiedostojen luomiseen, joilla on samat asetukset kuin XLTX-tiedostossa.

## Lyhyt historia

Vuoden 2000 alussa Microsoft päätti tehdä muutoksen mukauttaakseen **Office Open XML -standardin**. Tämän uuden standardin mukaiset erityyppiset asiakirjat tunnistettiin lisäämällä X niiden laajennuksiin, missä X tarkoittaa XML:ää. Vuoteen 2007 mennessä tämä uusi tiedostomuoto tuli osaksi Office 2007:ää, ja sitä käytetään myös Microsoft Officen uusissa versioissa. Uusi tiedostotyyppi on lisännyt etuja: pienet tiedostokoot, vähemmän muutoksia korruptiossa ja hyvin muotoiltujen kuvien esitys.

## XLTX-tiedostomuodon tekniset tiedot

XLTX-tiedostot perustuvat Office OpenXML -tiedostomuotoon ja käyttävät XML:ää ja [ZIP](/compression/zip/) pienentämään tiedostokokoa. Se luotiin Microsoft Office 2007:n julkaisun yhteydessä korvaamaan binääri XLT-tiedostomuoto. XLTX:n tapaan XLT-tiedostomuotoa voidaan käyttää [XLS](/spreadsheet/xls/)-tiedostojen luomiseen Microsoft Excel 2003:lla ja 2007:llä. Ne voidaan avata Microsoft Excelillä kaksoisnapsauttamalla tiedostoa. Tiedostojen järjestystä XLTX-tiedostomuodossa voi tarkkailla nimeämällä tiedosto uudelleen ZIP:ksi ja purkamalla sen sisältö levylle.

### [Content_Types].xml ###

Tämä on ainoa tiedosto, joka löytyy perustasolta, kun zip-tiedosto puretaan. Siinä luetellaan paketin osien sisältötyypit. Kaikki viittaukset paketissa oleviin XML-tiedostoihin viitataan tässä XML-tiedostossa.

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

* [[MS-XLSX] - .Xlsx-tiedostomuoto](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


