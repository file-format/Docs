{
  "date": "2019-10-11",
  "keywords": [
"shp tiedosto",
"shp-tiedostomuoto",
"mikä on shp-tiedosto",
"tiedosto",
"shp esimerkki",
"shp tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SHP - ESRI Shapefile",
  "description": "Opi SHP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SHP-tiedostoja.",
  "linktitle": "SHP",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sh-fip"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on SHP-tiedosto?

SHP on tiedostopääte yhdelle ensisijaisesta tiedostotyypistä, jota käytetään ESRI Shapefilen esittämiseen. Se edustaa paikkatietoa vektoritiedon muodossa, jota käytetään Geographic Information Systems (GIS) -sovelluksissa. Formaatti on kehitetty avoimina spesifikaatioina ESRI:n ja muiden ohjelmistotuotteiden yhteentoimivuuden helpottamiseksi.

## Tietojen esitys

Kuten mainittiin, shapefile-muoto kuvaa tietojoukon geospatiaalista tietoa vektoriominaisuuksina. Näitä vektorin ominaisuuksia ovat:

* pisteet

* rivit

* polygonit


Nämä ominaisuudet yhdessä voivat edustaa melkein minkä tahansa tyyppisiä muotoja, kuten vesikaivoja, maiden rajoja, spatiaalisia pisteitä, jokien virtausta, järviä jne. Jokaisella vektoripiirteellä voi olla attribuutteja, jotka määrittelevät ominaisuuden tarkoituksen. Esimerkiksi Los Angelesin kaupunkeja sisältävässä shape-tiedostossa voi olla kaupungin nimi ja lämpötila attribuutteina, jotka antavat merkityksellisen esityksen paikkatiedoille.

## Liittyvät tiedostot

Ohjelmistosovellukset eivät voi käyttää itsenäistä shp-tiedostoa sen sisältämien tietojen merkityksen määrittämiseen. Sellaisen tiedoston sisältämien tietojen ymmärtämiseksi shape-tiedosto käyttää seuraavia pakollisia lisätiedostoja.

* shx-tiedosto - hakemistotiedosto

* dbf-tiedosto - dBASE-tiedosto, joka tallentaa kaikki päätiedoston muotojen attribuutit

* prj-tiedosto - tallentaa tiedoston projektitiedot


Voi olla myös muita valinnaisia tiedostoja, joilla on sama nimi kuin päätiedostolla.

## SHP-tiedostomuodon tekniset tiedot

Shapefile-tiedoston avoimet tekniset tiedot ovat saatavilla verkossa ESRI:ltä muodossa [Technical Description](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf), ja niissä käsitellään tiedoston yleistä rakennetta yksityiskohtaisesti. .shp-päätiedoston tiedot koostuvat otsikoista ja tietueista. Kiinteäpituista tiedoston otsikkoa seuraavat muuttuvapituiset tietueet, joissa jokainen tietue koostuu kiinteän pituisesta tietueotsikosta, jota seuraa muuttuvapituinen tietuesisältö.

### SHP-tiedoston pääotsikko

Tiedoston pääotsikko alkaa tiedoston alusta ja on 100 tavua pitkä. Tämän päätiedoston otsikon järjestely sekä tavujen sijainti, arvo, tyyppi ja tavujärjestys on seuraavan taulukon mukainen.


|Tavut|Kenttä|Arvo|Tyyppi|tavujärjestys
---|---|---|---|---|
|0-3|Tiedostokoodi|9994|Kokonaisluku|Big Endian
|4-23|Käyttämätön|0|Kokonaisluku|Big Endian
|24-27|Tiedoston pituus|Tiedoston pituus|Kokonaisluku|Big Endian
|28-31|Versio|1000|Kokonaisluku|Little Endian
|32-35|Muototyyppi|Muototyyppi|Kokonaisluku|Little Endian
|36-67|Rajauksen vähimmäissuorakulmio|Xmin, Ymin, Xmax ja Ymax|kaksois|Little Endian
|68-83|Rajauslaatikko|Zmin, Zmax|kaksois|Little Endian
|84-99|Rajausruutu|Mmin, Mmax|kaksois|

On huomattava, että tiedoston pituuden arvo on tiedoston kokonaispituus 16-bittisinä sanoina, joka sisältää myös otsikon muodostavat viisikymmentä 16-bittistä sanaa.

#### Muototyypit

Yllä olevan taulukon muototyyppikentän arvot ovat seuraavat:


|Arvo|Muototyyppi
---|---|
|0|Nollamuoto
|1|Piste
|3|Polyline
|5|Monikulmio
|8|Monipiste
|11|PisteZ
|13|PolyLineZ
|15|MonikulmioZ
|18|MultiPointZ
|21|PisteM
|23|PolyLineM
|25|MonikulmioM
|28|MultiPointM
|31|MultiPatch

### Tietotietueet ###

Päätiedoston otsikkoa seuraavat muuttuvapituiset tietueet, joissa jokainen tietue koostuu kiinteäpituisesta tietueotsikosta, jota seuraa muuttuvapituinen tietuesisältö.

#### Tietueen otsikko ####

Tietueen otsikko sisältää tiedot tietueen numerosta ja sisällön pituudesta kiinteänä 8 tavun pituisena. Tietueen otsikon järjestys on seuraava:


|Tavut|Kenttä|Arvo|Tyyppi|tavujärjestys
---|---|---|---|---|
|0-3|tietuenumero|tietuenumero|kokonaisluku|iso
|4-7|tietueen pituus|tietueen pituus|kokonaisluku|iso

#### Tallenteen sisältö ####

Shapefile-tietueen sisältö koostuu muototyypistä, jota seuraa kyseisen muodon geometriset tiedot. Muototyyppi 0 edustaa nollamuotoa, jolla ei ole muodon geometrisia tietoja. Tietueen sisällön pituus on muodon osien ja kärkien heijastus. Otetaan esimerkki Point Shape -tyypistä selvittääksesi, kuinka tietue sisältää tietoja tällaisesta muototyypistä.

Piste edustaa tiettyä maantieteellistä sijaintia järjestyksessä X,Y, jossa jokaista koordinaattia edustaa kaksinkertainen tarkkuusarvo. Seuraava taulukko näyttää pisteen muototyypin järjestelyn.


|Tavut|Muototyyppi|Arvo|Tyyppi|Numero|tavujärjestys
---|---|---|---|---|---|
|0-3|Muototyyppi|1|Kokonaisluku|1|Pieni
|4-11|X|X|kaksinkertainen|1|vähän
|12-19|Y|Y|tupla|1|vähän

Examples of other shape types can be found the ESRI technical description document.

## Viitteet ##

* [ESRI Shapefile Technical Description](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf), ESRI


