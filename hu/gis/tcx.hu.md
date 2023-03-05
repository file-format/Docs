{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCX fájlformátum - Oktatóközpont XML fájl",
  "description":"További információ a TCX fájlformátumról és az API-król, amelyek TCX-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Mi az a TCX fájl?

A TCX (Training Center XML) fájl egy adatcsere-formátum, amelyet a fitneszeszközök közötti adatok megosztására használnak. 2008-ban mutatták be a Garmin Training Center termékével. Az edzésadatok, például a pulzusszám, a futási ütem, a kerékpáros ütem, a kalóriák és a köridő [XML](/hu/web/xml/) formátumban tárolódnak a TCX-fájlban. Ezenkívül a TCX fájl összefoglaló adatokat is tartalmaz az edzéspályáról. A TCX fájlok hasonlóak a Garmin sport hordható eszközökkel létrehozott [FIT](/hu/gis/fit/) fájlokhoz.

## TCX fájlformátum - További információ

A TCX-fájlokat a rendszer XML-fájlként menti a lemezre, minden rekord tevékenységként mentve. Egy tevékenység magában foglalja az edzés összes adatát, például időt, köridőt, azonosítót, pulzusszámot, intenzitást, ütemet és pályainformációkat, amelyek a pozíciópárokat és az adott hosszúságú pozícióhoz tartozó időbélyegzőt tartalmazzák, hasonlóan a [GPX]-hez. (/hu/gis/gpx/) fájlokat.

### TCX fájlformátum-verziók

Ennek a formátumnak két változata létezik saját XML-sémákkal, amelyeket a Garmin tárol. Íme néhány közülük:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX adatprotokoll

A TCX XML formátum gyors verziója [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol) néven érhető el a Githubon.

## Referenciák ##

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

