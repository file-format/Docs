{
  "date": "2019-12-10",
  "keywords": [
"XLSX",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Excel",
"Laskentataulukko"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi mikä on XLSX-tiedosto ja API:t, jotka voivat luoda ja avata XLSX-tiedostoja.",
  "title": "XLSX-tiedostomuoto - Mikä on XLSX-tiedosto?",
  "linktitle": "XLSX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xls-fix"
}
},
  "lastmod": "2019-12-10"
}

## Mikä on XLSX-tiedosto?

**XLSX** is well-known format for Microsoft Excel documents that was introduced by Microsoft with the release of Microsoft Office 2007. Uusi muoto perustuu OOXML-standardin ECMA-376 kohdassa [Part 2](https://www.ecma-international.org/publications-and-standards/standards/ecma-376/) kuvattuun Open Packaging Conventions -käytäntöön järjestettyyn rakenteeseen. Uusi muoto on zip-paketti, joka sisältää useita XML-tiedostoja. Taustalla oleva rakenne ja tiedostot voidaan tutkia yksinkertaisesti purkamalla .xlsx-tiedosto.

## XLSX-tiedostomuodon lyhyt historia

XLSX file format was introduced in 2007 and uses the Open XML standard adapted by Microsoft back in 2000. Ennen XLSX:ää yleinen käytetty tiedostomuoto oli [XLS](/spreadsheet/xls/), joka oli puhdas binääritiedostomuoto. Uuden tiedostotyypin etuja ovat pienet tiedostokoot, pienemmät korruption muutokset ja hyvin muotoiltu kuvien esitys. Vuoden 2000 alussa Microsoft päätti tehdä muutoksen mukauttaakseen **Office Open XML -standardin**. Vuoteen 2007 mennessä tämä uusi tiedostomuoto tuli osaksi Office 2007:ää, ja sitä käytetään myös Microsoft Officen uusissa versioissa.

## XLSX-tiedostomuodon tekniset tiedot

Viralliset [XLSX file format specifications](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) ovat saatavilla verkossa Microsoftilta. Nähdäksesi, mitä XLSX-tiedoston sisällä on, nimeä se uudelleen [ZIP](/compression/zip/)-tiedostoksi muuttamalla sen päätettä ja pura se sitten nähdäksesi tämän Excel-työkirjan osatiedostot. Kun tyhjä työkirja puretaan sen tiedostoihin, se sisältää seuraavat tiedostot ja kansiot.

### [Content_Types].xml ###

Tämä on ainoa tiedosto, joka löytyy perustasolta, kun zip-tiedosto puretaan. Siinä luetellaan paketin osien sisältötyypit. Kaikki viittaukset paketin XML-tiedostoihin viitataan tässä XML-tiedostossa.

### \_rels (kansio) ###

Tämä on Relationships-kansio, joka sisältää yhden XML-tiedoston, joka tallentaa pakettitason suhteet. Linkit Xlsx-tiedostojen tärkeimpiin osiin sisältyvät tähän tiedostoon URI-tunnuksina. Nämä URI:t tunnistavat kunkin avainosan ja paketin suhteen tyypin. Tämä sisältää suhteen ensisijaiseen toimistoasiakirjaan, joka sijaitsee muodossa xl/workbook.xml, ja muita docPropsin osia ydin- ja laajennettuina ominaisuuksina.

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


## XLSX-muotoesimerkki ##


Jokaista työkirjan Excel-laskentataulukkoa kohden on yksi XML-tiedosto. Löydät nämä XML-tiedostot xl/worksheets-kansiosta. Kaikki laskentataulukon sisältämät tiedot on järjestetty XML-tiedoston eri osiin. Tarkastellaan esimerkkilaskentataulukkoa työkirjasta, joka näkyy seuraavassa kuvassa.

{{< figure src="../XLSX file format.png" alt="XLSX-tiedostomuoto" >}}

Kuten voidaan nähdä, tämä laskentataulukko sisältää solujen A1–B2 sisällön ja kuvan. Lisäksi solu G13 on tällä hetkellä aktiivinen solu laskentataulukossa. Tarkastellaan nyt xl/worksheets/sheet1.xml-tiedostoa nähdäksesi, kuinka nämä tiedot esitetään XML-tiedostossa. Tämän XML-tiedoston sisältö on kuvattu alla.

{{< figure src="../XLSX File Format Details.png" alt="XPS tiedostomuoto" >}}

1. Välilehdellä on teemaväri. Se mainitaan XML-tiedostossa tagilla<tabColor> teeman id:n mukaan.
1. VälilehdenSelected arvoksi on asetettu 1, mikä osoittaa, että tämä on valittu arkki
1. Kuten yllä olevasta ensimmäisestä kuvasta näkyy, laskentataulukon solu G13 on aktiivinen solu, joka mainitaan myös XML-tiedostossa.
1. SheetData-välilehti edustaa laskentataulukon sisältämiä tietoja. Voit kuitenkin nähdä, että laskentataulukon alkuperäinen sisältö ei ole missään tässä osiossa. Tämä johtuu siitä, että teksti viitataan epäsuorasti sharedStrings XML-arkilta. Tämä linkittäminen varmistaa, että jokainen teksti tallennetaan vain kerran ja että siihen voidaan viitata uudelleen tilan säästämiseksi.
1. Kuvaan, kuten voidaan nähdä, viitataan viitetunnuksella rId2

## Osallistu

Onko sinun jaettava jotain XLSX- tai Spreadsheet-tiedostomuodoista? Voit julkaista havaintosi [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet)-osiossa.

## Viitteet

* [[MS-XLSX] - XLSX-tiedostomuoto](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


