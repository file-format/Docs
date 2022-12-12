{
  "date" : "2021-07-29",
  "keywords" :[ "gpkg fájl", "gpkg fájl formátum", "mi az a gpkg fájl", "fájl", "gpkg példa", "gpkg fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - GeoPackage Format Files",
  "description":"További információ a GPKG fájlformátumról és az API-król, amelyek GPKG-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Mi az a GPKG fájl?
A .gpkg kiterjesztésű fájl egy SQLite adatbázis-tárolóként megvalósított földrajzi információs rendszerből áll, amely adatokat és metaadattáblázatokat tartalmaz tipikus definíciókkal, formátumkorlátozásokkal, integritási állításokkal és tartalmi megszorításokkal. 2014-ben jelent meg; amelyet az OGC (Open Geospatial Consortium) határoz meg az amerikai hadsereg nevében. Különböző kormányok, kereskedelmi és nyílt forráskódú szervezetek széles körben támogatják a GeoPackage-et.

## GPKG fájlformátum
A GeoPackage kiterjesztett SQLite 3 adatbázisfájlként készül; egy szabvány szabályokat határoz meg (szükséges konvenciókat):
- Csempemátrix képkészletek tárolása
- Vektor funkciók
- Raszteres térképek különböző léptékben
- Metaadatok és séma

A GeoPackage kiterjeszthető a szabvány 2.3. pontjában meghatározott kiterjesztési szabályok használatával. A GeoPackage tervezésének célja az volt, hogy a lehető legnagyobb mértékben egy könnyű adatbázist készítsünk, és azt egy használatra kész fájlba foglaljuk. Ez ideálissá teszi a mobilalkalmazásokhoz off-line módban és gyors megosztáshoz felhőalapú tárolókon vagy USB-tárolóeszközökön stb.

### GPKG Tartalom
A GeoPackage-ek számos táblát tartalmaznak, akárcsak más relációs adatbázisok. Ezek a táblák lehetnek felhasználó által definiált vagy metaadattáblák. A GeoPackage két kötelező metaadat táblából áll:

#### gpkg_contents
Tartalomjegyzék egy GeoPackage számára. A táblázat kötelező oszlopai a következők:

- **tábla_neve**: a felhasználó által megadott adattábla tényleges neve;
- **adattípus**: az adattípus, pl. címek, jellemzők és attribútumok;
- **azonosító és leírás**: ember által olvasható szöveg ;
- **last_change**: az utolsó változtatás információs dátuma, ISO 8601 formátumban ;
- **min_x, min_y, max_x és max_y**: a tartalom térbeli kiterjedése. ;
- **srs_id**: térbeli referenciarendszer .

#### gpkg_spatial_ref_sys
Térbeli referenciatartalomhoz; beleértve, de nem kizárólagosan a csempéket és jellemzőket, a tartalom minden sorának egy koordináta-referenciarendszerre kell hivatkoznia; a **gpkg_spatial_ref_sys** táblában tárolva. A táblázat kötelező oszlopai a következők:

- **srs_name, description**: az SRS ember által olvasható neve és leírása;
- **srs_id**: az SRS egyedi azonosítója; a tábla elsődleges kulcsa is;
- **szervezet**: A meghatározó szervezet kis- és nagybetűk megkülönböztetése nélküli neve.
- **organization_coordsys_id**: A szervezet által hozzárendelt SRS numerikus azonosítója;
- **definíció**: Az SRS jól ismert szöveges meghatározása.


## Hivatkozások

* [GeoPackage – a Wikipedia által)](https://en.wikipedia.org/wiki/GeoPackage)
* [Getting Started With GeoPackage](http://www.geopackage.org/guidance/getting-started.html)

