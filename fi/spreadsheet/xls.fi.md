{
  "date": "2019-12-16",
  "keywords": [
"XLS",
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
  "description": "Tiedostomuoto-opas tietää, mikä on XLS-tiedosto ja API:t, jotka voivat luoda ja avata niitä.",
  "title": "Mikä on XLS-tiedostomuoto? Opi tiedostomuoto-asiantuntijoilta!",
  "linktitle": "XLS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xl-fis"
}
},
  "lastmod": "2019-12-16"
}

## Mikä on XLS-tiedosto?

Files with XLS extension represent Excel Binary File Format. Such files can be created by Microsoft Excel as well as other similar spreadsheet programs such as OpenOffice Calc or Apple Numbers. File saved by Excel is known as Workbook where each workbook can have one or more worksheets. Data is stored and displayed to users in table format in worksheet and can span numeric values, text data, formulas, external data connections, images, and charts. Applications like Microsoft Excel lets you export workbook data to several different formats including [PDF](/pdf/), [CSV](/spreadsheet/csv/), [XLSX](/spreadsheet/xlsx/), [TXT](/word-processing/txt/), [HTML](/web/html/), [XPS](/page-description-language/xps/), and several others. The XLS file format was replaced with a more open and structured format, XLSX, with the release of Microsoft Excel 2007. The latest versions still provide support for creating and reading XLS files, though XLSX is the first choice of use now.

## Lyhyt historia

XLS was created by Microsoft for use with Microsoft Excel and is also known as Binary Interchange File Format (BIFF). This file type was introduced for the first time by making it part of Excel for Windows in 1987. XLS file format specifications were made public for the first in June 2008 as Revision 1. After that, the specifications were continuously updated and the latest revision available is as of August 2018 that is marked as Revision 8.0. A brief history of different versions of XLS file format is as follow:

* Version 7.0 (released with office 95):  This version of excel was the most robust and faster among all the versions and internal stream rewrites were updated to 32 bits.
* Versio 8 (julkaistu Office 97:n kanssa): VBA otettiin käyttöön vakiokielenä ja poistetut luonnollisen kielen tarrat sisällytettiin tähän versioon ensimmäistä kertaa. Se esitteli myös ensimmäistä kertaa paperiliittimen toimistoavustajan.

* Versio 9 (julkaistu Office 2000:n kanssa): Versiossa 9 tehtiin vain pieniä muutoksia, joissa paperiliitintoimisto-avustaja pystyi säilyttämään samanaikaisesti useita objekteja, jotka eivät olleet aiemmin mahdollisia.

* Versio 10 (julkaistu Office XP:n kanssa): Tämä versio ei sisältänyt havaittavia parannuksia.

* Version 11 (Released with office 2003): Major update in version 11, excel 2003 was the introduction of new tables.

## XLS-tiedostomuodon tekniset tiedot ##

Tiedot on järjestetty XLS-tiedostoon binäärivirroina yhdistelmätiedoston muodossa Microsoftin [MS-CFB]. Data is stored in the compound file by using storages, streams, and substreams that contain information about the content and structure of a workbook, including workbook data such as worksheet definitions. Each stream or substream contains a series of binary records. Each binary record contains zero or more structured fields that contain the workbook data. This section gives a brief overview of XLS File Structure, but for detailed file format specifications, one must consult the [XLS File Formation Specifications](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)-asiakirjassa kuvatulla tavalla.

#### Stream ja Substream ####

Työkirjaa edustaa työkirjavirta. Jokaista työkirjan laskentataulukkoa edustavat alivirrat. Lisäksi siinä on Chart Sheet Substream, Macro Sheet Substream tai Dialog Sheet Substream, joka seuraa globaalia alivirtaa. Jokainen työkirjan dataa sisältävä binäärivirta tai alivirta ON kirjoitettava sarjana binääritietueita.

#### Ennätys ####

Työkirjan ominaisuuksien tiedot tallennetaan tietueeksi, joka on muuttuvapituinen tavusarja. Binääritietue koostuu seuraavista kolmesta osasta:

**Tietueen tyyppi:** Tietuetyyppi on kaksitavuinen etumerkitön kokonaisluku, joka määrittää, minkä tyyppisiä tietoja tietue määrittää ja kuinka tälle tietueelle ominaisten tietuetietojen rakenne on järjestetty ja jäsennelty. Tietuetyypin arvojen TÄYTYY olla arvo tietueluettelosta (osio 2.3) tai tietueen PITÄÄ hyödyntää tulevaa tietuearkkitehtuuria (osio 2.1.6).

**Tietueen koko**: Tietueen koko on kaksitavuinen etumerkitön kokonaisluku, joka määrittää tavumäärän, joka määrittää tietuetietojen kokonaiskoon. Tietueen koon PITÄÄ olla suurempi tai yhtä suuri kuin 0 ja TÄYTYY olla pienempi tai yhtä suuri kuin 8224.

**Tietuetiedot:** Tietueen tietokomponentti sisältää kenttiä, jotka vastaavat tiettyä tietuetyyppiä ja muodostavat tietueen loppuosan. Tietyn tietuetyypin kenttien järjestys ja rakenne on määritetty tietuetyypin vastaavassa osiossa. Tietueen datakomponentin koon TÄYTYY olla yhtä suuri kuin tietueen koko. Tietueen tietokomponentin kentät voivat sisältää yksinkertaisia arvoja, arvotaulukoita, useiden kenttien rakenteita, kenttätaulukoita ja rakenneryhmiä.

#### Solutaulukko ####

Solut ovat työkirjan peruslohkoja, jotka tallentavat työkirjan sisällön, kuten tekstin, kaavat ja numeeriset tiedot. Solut säilyttävät tallennetun datan tietueen tietorakenteen kautta, jota kutsutaan solutaulukoksi. Itse solutaulukko tallennetaan tietuejonoon, joka on määritysasiakirjassa määritettyjen CELLTABLE-sääntöjen mukainen. Se koostuu sarjasta rivilohkoja, joissa rivit on järjestetty rivilohkoiksi. Jokainen rivilohko sisältää rivejä ensimmäisestä dataa sisältävästä rivistä viimeiseen dataa sisältävään riviin.

Tiedot tai rivin muotoilu tallennetaan jokaisen rivilohkon rivitietueeseen. Jokaista dataa tai yksittäistä solumuotoilua sisältävää solua edustaa tietue. Soluun liittyvä muotoilu voidaan johtaa yksittäisen solun muotoilusta, rivin muotoilusta, sarakkeen muotoilusta tai oletussolumuodosta. Muotoilun tärkeysjärjestys on yksittäisten solujen muotoilu korkeimmalla tärkeydellä, jota seuraa rivien muotoilu ja sitten sarakemuotoilu ja sitten oletussolumuoto. Soluja, jotka eivät sisällä dataa ja jotka eivät sisällä yksittäistä muotoilua, ei tallenneta.

#### Kaavat ####

Kaava on sarja arvoja, soluviittauksia, nimiä, funktioita tai operaattoreita solussa, jotka yhdessä tuottavat uuden arvon. Kaavat tallennetaan tokenisoituun esitykseen, joka tunnetaan nimellä jäsennetty lauseke. Jäsennetty lauseke muunnetaan tekstikaavaksi ajon aikana näyttöä ja käyttäjän muokkausta varten. Solukaavat määritellään Formula-tietueessa. Array-tietue määrittää taulukkokaavat. Jaetut kaavat määritetään ShrFmla-tietueessa.

#### Kaaviot ####

Kaaviotaulukko määrittää kaavion, grafiikan, joka näyttää dataa tai tietojoukkojen väliset suhteet visuaalisessa muodossa, ja kaavion tietovälimuistin, paikallinen kopio kaaviotiedoissa käytetyistä tiedoista puuttuu tai linkit ulkoisiin tietolähteet ovat rikki. Kaaviossa määritellään yksi tai kaksiakseliset ryhmät, akselijoukot, joita vastaan kaaviotiedot piirretään, sekä sarjat, trendiviivat ja virhepalkki, jotka on määritetty kaaviossa. Kukin akseliryhmä määrittää yhdestä neljään kaavioryhmää, jotka määrittävät datan näyttämiseen käytettävän visualisoinnin tyypin. Jokainen sarja, trendiviiva ja virhepalkki määrittää kaavioryhmän, johon se liittyy.

#### Metatiedot ####

Metadata on lisätietoa, joka liittyy tiettyyn soluun tai sen sisältöön. Metadata tallennetaan BIFF8:aan vain tulevaa laajennettavuutta varten.

#### Pivot-taulukot ####

Pivot-taulukko on mekanismi lähdetietojen yhteenvetoon saadakseen yleiskuvan kyseisten tietojen jakautumisesta. Pivot-taulukossa soveltuvista lähdetietojen sarakkeista tulee kenttiä, joita voidaan käyttää tietojen yhteenvetoon. Kun pivot-taulukon lähdetiedot ovat OLAP-lähdetietoja, OLAP-hierarkioista ja joistakin muista OLAP-olioista tulee pivot-taulukon kenttiä.
Pivot-taulukossa on kaksi pääosaa, PivotCache ja PivotTable-näkymä. PivotTable-näkymiä voi olla useita, jotka perustuvat yhteen ei-OLAP-pivot-välimuistiin.

#### Tyylit ####

Tämä yleiskatsaus kuvaa, kuinka arkin (1) solujen muotoilu- ja suojaustiedot määritetään. Solujen muotoilu koostuu useista ominaisuuksista:

* Fontin ominaisuudet (lihavoitu, kursivoitu, fontin väri, kirjasinkoko jne.)

* Täyttöominaisuudet (etualan väri, taustaväri, kuvio, kaltevuus jne.)

* Tasausominaisuudet (vasen, keski, oikea kohdistus jne...)

* Reunuksen ominaisuudet (vasen, oikea, ylä, alaosa, paksu tai ohut, väri jne.)

* Numeron muotoilun ominaisuudet (päivämäärä, aika, desimaalien määrä jne.)

* Suojausominaisuudet (lukittu, piilotettu jne...)


Nämä ominaisuudet kokonaisuutena kuvaavat, kuinka tietty solu näytetään ja tulostetaan.

## Viitteet ##

* [[MS-XLS] - Excelin binaaritiedostomuotorakenne](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)

* [[MS-CFB] - Yhdistetyn tiedoston binaaritiedostomuoto](https://msdn.microsoft.com/en-us/library/dd942138.aspx)


