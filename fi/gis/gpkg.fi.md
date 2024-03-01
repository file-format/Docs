{
  "date": "2021-07-29",
  "keywords": [
"gpkg tiedosto",
"gpkg tiedostomuoto",
"mikä on gpkg-tiedosto",
"tiedosto",
"gpkg esimerkki",
"gpkg tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "GPKG - GeoPackage-muotoiset tiedostot",
  "description": "Opi GPKG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata GPKG-tiedostoja.",
  "linktitle": "GPKG",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gpkg"
}
},
  "lastmod": "2021-07-29"
}

## Mikä on GPKG-tiedosto?
Tiedosto, jonka laajennus on .gpkg, koostuu maantieteellisestä tietojärjestelmästä, joka on toteutettu SQLite-tietokantasäiliönä, joka sisältää data- ja metatietotaulukot tyypillisine määritelmin, muotorajoituksin, eheysvahvistuksineen ja sisältörajoitteineen. Se julkaistiin vuonna 2014; määritellyt OGC (Open Geospatial Consortium) Yhdysvaltain armeijan puolesta. Useat hallitukset, kaupalliset ja avoimen lähdekoodin organisaatiot tukevat laajasti GeoPackagea.

## GPKG-tiedostomuoto
GeoPackage koostuu laajennetusta SQLite 3 -tietokantatiedostosta; standardi määrittelee joukon sääntöjä (pakollisia käytäntöjä):
- Kuvien tallentaminen laattamatriisijoukkoon
- Vector ominaisuuksia
- Rasterikartat eri mittakaavassa
- Metadata ja skeema

Voit laajentaa GeoPackagea käyttämällä standardin kohdassa 2.3 määriteltyjä laajennussääntöjä. GeoPackagen suunnittelun tarkoituksena oli tehdä mahdollisimman kevyt tietokanta ja sisällyttää se käyttövalmiin yksittäiseen tiedostoon. Tämä tekee siitä ihanteellisen mobiilisovelluksiin off-line-tilassa ja nopeaan jakamiseen pilvitallennus- tai USB-tallennuslaitteissa jne.

### GPKG Sisältö
GeoPackages sisältää useita taulukoita, kuten muutkin relaatiotietokannat. Nämä taulukot voivat olla joko käyttäjän määrittämiä tai metatietotaulukoita. GeoPackages koostuu kahdesta pakollisesta metatietotaulukosta:

#### gpkg_contents
Geopaketin sisällysluettelo. Tämän taulukon pakolliset sarakkeet ovat:

- **taulukon_nimi**: käyttäjän määrittämän tietotaulukon todellinen nimi;
- **data_type**: the data type, e.g. titles, features and attributes;
- **identifier and description**: human-readable text ;
- **last_change**: the informational date of last change, in ISO 8601 format ;
- **min_x, min_y, max_x ja max_y**: sisällön spatiaaliset laajuudet. ;
- **srs_id**: paikkaviittausjärjestelmä .

#### gpkg_spatial_ref_sys
Tilaviitesisällölle; mukaan lukien mutta ei rajoittuen ruudut ja ominaisuudet, jokaisen sisällön rivin on viitattava koordinaattiviittausjärjestelmään; tallennettu **gpkg_spatial_ref_sys**-taulukkoon. Tämän taulukon pakolliset sarakkeet ovat:

- **srs_name, description**: a human readable name and description for the SRS;
- **srs_id**: a unique identifier for the SRS; also the primary key for the tabl-fie;
- **organisaatio**: määrittävän organisaation nimi, jossa kirjainkoolla ei ole merkitystä.
- **organisation_coordsys_id**: organisaation määrittämä SRS:n numerotunnus;
- **määritelmä**: SRS:n tunnettu tekstimääritelmä.


## Viitteet

* [GeoPackage - Wikipedia](https://en.wikipedia.org/wiki/GeoPackage)

* [Getting Started With GeoPackage](http://www.geopackage.org/guidance/getting-started.html)


