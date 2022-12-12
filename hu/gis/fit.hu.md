{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FIT fájlformátum - Garmin tevékenységfájl",
  "description":"További információ a FIT fájlformátumról és az API-król, amelyek FIT fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Mi az a FIT fájl?

A FIT fájl egy GIS fájl, amelyet a Garmin sport hordható eszközök hoztak létre. Arra használják, hogy rögzítsék a személy tevékenységeit, amikor ezeket az eszközöket viselve mozog. A tevékenységi adatok tartalmazzák a GPS-eszköz által rögzített helyet és időt. A FIT fájlokat a rögzített tevékenységi adatok webes API-k segítségével történő átvitelére is használják. Ez az oka annak, hogy a FIT fájlok a leggyakrabban használt fájlformátum a fitneszadatok más fitneszplatformokkal való megosztására. További gyakori fájlformátumok: [GPX](/hu/gis/gpx/), TCX és [KML](/hu/gis/kml/).

## FIT Fájlformátum - További információ

A FIT fájlok bináris fájlként kerülnek a lemezre a Garmin eszközök által a tevékenységhez rögzített információkkal. A FIT fájlban tárolt információk a következőket tartalmazzák:

* Dátum idő
* Sporttípusok
* Kör és osztott adatok
* GPS pálya
* Érzékelő adatok
* Események az aktív munkamenethez

A tevékenységadatok valós időben rögzíthetők a fájlban, vagy exportálhatók a tevékenységrögzítés befejezése után.

### FIT tevékenységüzenetek

A FIT tevékenységfájl tartalmazhat néhány kötelező üzenettípust. A tevékenységfájlhoz szükséges üzenetek a következők.

|Üzenet|Cél|
---|---|
|Fájlazonosító| A Fájlazonosító üzenet minden FIT fájltípushoz szükséges, és ez várhatóan az első üzenet a fájlban. Tevékenységfájlok esetén a Type tulajdonságot 4.|-re kell állítani
|Tevékenység| A FIT Activity fájlban egyetlen tevékenységi üzenet szükséges. A tevékenység üzenet tartalmazza a Helyi időbélyeg és a Munkamenetszám tulajdonságokat. A helyi időbélyeg határozza meg azt az időzóna-eltolást, amely a fájl összes időbélyegére alkalmazható. A legtöbb eszköz valós időben rögzíti a FIT fájlokat, és a munkamenetek száma ismeretlen lesz a rögzítés végéig. Emiatt a tevékenység üzenet gyakran az utolsó üzenet a fájlban.|
|Session| A tevékenységfájlok egy vagy több munkamenet-üzenetet tartalmaznak. A munkamenet üzenet egy összefoglaló üzenettípus. A kezdési idő, az összes eltelt idő, az időzítő teljes ideje és az időbélyegző mezők kötelezőek minden összefoglaló üzenethez.|
|Lap| A körüzenetek a munkameneten belüli köröket vagy intervallumokat jelölik. A körüzenet összefoglaló üzenettípus. A kezdési idő, az összes eltelt idő, az időzítő teljes ideje és az időbélyegző mezők kötelezőek minden összefoglaló üzenethez.|
|Rekord| A rögzítési üzenetek közé tartozik a GPS koordináta, sebesség, távolság, pulzusszám, teljesítmény stb.|

## FIT File Hasznos források

* [FIT tevékenységfájlok dekódolása](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [FIT tevékenységfájlok kódolása](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Referenciák ##

* [FIT tevékenységfájl](https://developer.garmin.com/fit/file-types/activity/)

