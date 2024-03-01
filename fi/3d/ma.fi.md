{
  "date": "2019-10-11",
  "keywords": [
"ma",
"ma tiedosto",
"ma tiedostomuoto",
"tiedosto muoto",
"3d",
"ma-tiedoston lataus",
".ma-tiedosto",
".ma"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi MA-tiedostomuodosta ja sovellusliittymistä, jotka voivat avata ja luoda MA-tiedostoja.",
  "title": "MA tiedostomuoto",
  "linktitle": "MA",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-m-fia"
}
},
  "lastmod": "2021-06-04"
}

## Mikä on MA-tiedosto?

Tiedosto, jonka pääte on .ma, on Autodesk Maya -sovelluksella luotu 3D-projektitiedosto. Se sisältää suuren luettelon tekstikomentoista tiedoston tietojen määrittämiseksi. **.ma-tiedosto** voidaan avata ja muokata missä tahansa tekstieditorissa komentoihin liittyvien ongelmien korjaamiseksi, jos tiedosto vioittuu. Nämä tiedostot sisältävät tietoja 3D-näkymän määrittämiseen, kuten geometria, valaistus, animaatio ja renderöinti.

## MA tiedostomuoto

MA-tiedostot tallennetaan levylle ASCII-tekstimuodossa toisin kuin MB-tiedostot, jotka tallennetaan binääritiedostomuodossa levylle. Yksityiskohtainen viite MA-tiedostomuodolle on saatavilla osoitteessa [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001), ja siihen voi viitata kehittäjän viitteenä.

### MA-tiedoston otsikko

MA-tiedoston otsikko alkaa kommenttiosalla, joka antaa tiedoston luontitiedot ja muokkauspäivämäärän. Maya-tiedostonlukijat jättävät tämän lohkon huomiotta, koska sitä käytetään vain tiedoksi. Otsikon on kuitenkin alettava kuudella ensimmäisellä merkillä muodossa //Maya.

ASCII-tiedoston otsikko näyttää seuraavalta.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Tiedostoviitteet

.ma-tiedoston tiedostoviittaukset-osio sisältää tiedot kaikista muista Maya-tiedostoista, joihin tässä tiedostossa viitataan. Jokainen viitattu tiedosto voidaan lukea käyttämällä yhtä tiedostokomentoa, joka sisältyy samaan tiedostoon. Tiedostokomennon syntaksi, kun sitä käytetään viittaamiseen, on:

```
file -r -rpr prefixString fileName;
```
tai

```
file -r -ns nameSpace fileName
```
Tässä on esimerkkimerkkijono.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Tämä esimerkki osoittaa, että tiedoston aurinko sisältämä aurinkoobjekti olisi käytettävissä tässä tiedostossa nimellä aurinko_aurinko.

### Vaatimukset

.ma-tiedoston Vaatimukset-osio koostuu sarjasta vaadittuja komentoja ja kertoo toukokuun tiedot, kuten versio- ja laajennustiedot, joita tarvitaan tiedostojen lukemiseen. Esimerkki vaatimuksista on seuraava.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Seuraavassa osiossa määritellään vaatimukset. Tämä koostuu sarjasta vaadittavia komentoja. Tämä tiedoston osa kertoo Mayalle, mitä ohjelmistoja tarvitaan tiedoston lataamiseen oikein. Tarkemmin sanottuna mikä Maya-versio ja mitkä laajennukset.

## MA-tiedoston lataus
3D-mallin MA-tiedoston löytäminen ja lataaminen on hieman vaikeaa. Siksi voit ladata mallin MA-tiedoston täältä:

- {{HYPERLINKKI1}}


## Viitteet

* [Maya ASCII -tiedostojen organisaatio – Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)


