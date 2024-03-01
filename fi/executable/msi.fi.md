{
  "date": "2021-06-30",
  "keywords": [
"msi-tiedosto",
"MSI-tiedostomuoto",
"mikä on msi-tiedosto",
"tiedosto",
"msi esimerkki",
"msi tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi MSI-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MSI-tiedostoja.",
  "title": "MSI - Windows Installer -pakettitiedosto",
  "linktitle": "MSI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ms-fii"
}
},
  "lastmod": "2021-06-30"
}

## Mikä on MSI-tiedosto?
MSI-tiedosto, jota käytetään Windows-ohjelmien asentamiseen ja käynnistämiseen; täydellinen Microsoft Windows -paketti, joka sisältää asennustiedot tyypilliselle ohjelmistolle, mukaan lukien tärkeät asennettavat tiedostot ja tiedot asennuspaikasta. MSI-tiedostot voivat sisältää myös ohjelmistopäivityspaketin. MSI-tiedostot ovat samankaltaisia kuin [EXE](/executable/exe/), mutta joskus EXE ei välttämättä sisällä asennustietoja ja ohjelmisto saattaa toimia suoraan, kun EXE-tiedosto suoritetaan.

## MSI-tiedostomuoto
Windows Installer on itse asiassa Microsoft Windowsin API (Application Programming Interface) ja ohjelmistokomponentti, jota käytetään ohjelmistojen asennukseen, poistamiseen ja ylläpitoon. Asennustiedot ja valinnaiset tiedostot on pakattu asennuspaketteiksi ja löyhästi relaatiotietokantoiksi, jotka on strukturoitu COM Structured Storage -muodossa; tunnetaan hyvin nimellä **MSI-tiedostot**, joiden tiedostotunniste on .msi. Paketit, joiden tiedostotunniste on **.mst**, sisältävät Windows Installerin **Transformation Scripts**, tiedostot, joiden tiedostopääte on **.msm**, sisältävät **Merge Modules** ja tiedostotunnisteen **.pcp** käytetään **korjauksen luontiominaisuuksissa**. Windows Installerista tulee edistyneempi, kun siihen on tehty merkittäviä muutoksia aiemmista versioistaan Setup API. GUI-kehys ja asennuksen purkujakson automaattinen luominen ovat Windows Installerin uusia ominaisuuksia. Sitä on nyt pidetty vaihtoehtona itsenäisille suoritettaville asennuskehyksille.

### MSI-pakettien looginen rakenne
Paketti tarkoittaa yhden tai useamman täyden tuotteen asennusta, ja se tunnistetaan yleensä **GUID:llä**. Tuote koostuu yhdestä tai useista komponenteista ja ryhmitellään erilaisiin ominaisuuksiin. Windows Installer ei käsittele eri tuotteiden välisiä riippuvuuksia samanaikaisesti. Pakettien looginen rakenne koostuu seuraavista elementeistä:

- **Tuotteet**: Yksi asennettu, toimiva ohjelma tai useiden ohjelmien sarja yhdistettynä on tuote. Tuotteen tunnistaa yksilöllinen GUID.
- **Ominaisuudet**: Saattaa sisältää minkä tahansa määrän komponentteja ja muita aliominaisuuksia. Pienemmät paketit voivat koostua yhdestä ominaisuudesta.
- **Komponentit**: Windows Installer käsittelee komponenttia yhtenä kokonaisuutena. voi sisältää ohjelmatiedostoja, kansioita, rekisteriavaimia, COM-komponentteja ja pikakuvakkeita.
- **Key Paths**: A key path is a specific file, ODBC data source, or registry key that the package author specifies as critical for a given component.

## Viitteet 

* [Windows Installer - Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)



