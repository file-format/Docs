{
  "date": "2019-12-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Tiedostomuoto-opas tietää, mikä on _XLSX-tiedosto ja API:t, jotka voivat luoda ja avata _XLSX-tiedostoja.",
  "title": "Mikä on _XLSX-tiedosto?",
  "linktitle": "_XLSX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-_xls-fix"
}
},
  "lastmod": "2021-11-22"
}

## Mikä on _XLSX-tiedosto?

Tiedosto, jonka pääte on .\_xlsx, on itse asiassa [XLSX](/spreadsheet/xlsx/)-tiedosto, jonka jokin muu sovellus nimeää uudelleen. Tämä voi tapahtua tietyissä tapauksissa, kun tiedostonimi sisältää . tiedostonimen lopussa. \_XLSX-tiedostot voidaan avata Microsoft Excelissä samalla tavalla kuin XLSX-tiedostot nimeämällä ne uudelleen .xlsx-tunnisteeksi.

## _XLSX-tiedostomuoto - Lisätietoja

The _XLSX files are no different than the XLSX files and use the Open XML standard adopted by Microsoft back in 2000. Ennen XLSX:ää [XLS](/spreadsheet/xls/) oli ensisijainen tiedostomuoto, jota käytettiin Excel-laskentataulukoiden työskentelyssä asiakirjojen tallentamiseen binäärimuodossa. Tällä uudella XML-pohjaisella tiedostomuodolla oli etuja, kuten pieni tiedostokoko, tiedostojen korruption kestävyys ja hyvin muotoiltu kuvien esitys. Tämä uusi XML-pohjainen tiedostomuoto tuli osaksi Office 2007:ää, ja se toteutetaan myös Microsoftin uusissa versioissa.

## \_XLSX-tiedostomuodon tekniset tiedot

Koska \_XLSX-tiedosto on XLSX-tiedosto, joka on nimetty uudelleen, sillä on samat tekniset tiedot kuin alkuperäisellä tiedostolla. Se on vain arkistotiedosto, joka perustuu [ZIP](/compression/zip/)-arkistotiedostomuotoon. Jos haluat nähdä tämän arkiston sisällön, nimeä tiedosto uudelleen .zip-tunnisteeksi ja pura se nähdäksesi tämän Excel-työkirjan osatiedostot. Kun tyhjä työkirja puretaan sen tiedostoihin, se sisältää seuraavat tiedostot ja kansiot.

### [Content_Types].xml

Tämä on ainoa tiedosto, joka löytyy perustasolta, kun zip-tiedosto puretaan. Siinä luetellaan paketin osien sisältötyypit. Kaikki viittaukset paketin XML-tiedostoihin viitataan tässä XML-tiedostossa.

### \_rels (kansio)

Tämä on Relationships-kansio, joka sisältää yhden XML-tiedoston, joka tallentaa pakettitason suhteet. Linkit Xlsx-tiedostojen tärkeimpiin osiin sisältyvät tähän tiedostoon URI-tunnuksina. Nämä URI:t tunnistavat kunkin avainosan ja paketin suhteen tyypin. Tämä sisältää suhteen ensisijaiseen toimistoasiakirjaan, joka sijaitsee muodossa xl/workbook.xml, ja muita docPropsin osia ydin- ja laajennettuina ominaisuuksina.

### docProps

Tämä kansio sisältää asiakirjan yleiset ominaisuudet. Näitä ovat joukko ydinominaisuuksia, joukko laajennettuja tai sovelluskohtaisia ominaisuuksia ja asiakirjan esikatselu. Tyhjässä työkirjassa on kaksi tiedostoa tässä kansiossa, nimittäin app.xml ja core.xml. core.xml sisältää tietoja, kuten tekijä, luonti- ja tallennuspäivämäärä sekä muokkaus. App.xml sisältää tietoja tiedoston sisällöstä.

### xl (kansio)

Tämä on pääkansio, joka sisältää kaikki tiedot työkirjan sisällöstä. Oletuksena siinä on seuraavat kansiot:

* \_rels

* teema

* laskentataulukoita


ja seuraavat xml-tiedostot:

* styles.xml

* työkirja.xml


## Viitteet

* [MS-XLSX - .xlsx-tiedostomuoto](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


