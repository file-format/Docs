{
  "date" : "2021-07-30",
  "keywords" :[ "dlg fájl", "dlg fájlformátum", "mi az a dlg fájl", "fájl", "dlg példa", "dlg fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - Shapefile Shape Index Format",
  "description":"Tudjon meg többet a DLG fájlformátumról és az API-król, amelyekkel DLG fájlokat hozhat létre és nyithat meg.",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## Mi az a DLG fájl?
Egy .dlg kiterjesztésű fájl tartalmazza a Digital Line Graph-ot, amely egy térképészeti térképelem, amely digitális vektoros formában jelenik meg, és amelyet az US Geological Survey (USGS) kezel. A DLG fájlok két különböző formátumban érhetők el:
1. **Opcionális formátum**: Egyszerűen használható formátum, amely magában foglal egy 80 bájtos logikai rekordhosszt, az UTM földi koordináta-rendszert, valamint a vonal-, csomópont- és területelemekben található topológiai kapcsolatokat.
2. **Spatial Data Transfer Standard (SDTS) formátum**: olyan formátum, amely megkönnyíti a téradatok átvitelét a különböző számítógépes rendszerek között.

## DLG fájlformátum
A DLG fájlformátumot az USGS térképekhez tervezték, és nagy, közepes és kis léptékben továbbítják, akár kilenc különböző kategóriájú jellemzőkkel. A DLG fájlok opcionális és Spatial Data Transfer Standard (SDTS) formátumban kaphatók, topológiailag felépítettek a térképészeti és GIS alkalmazásokhoz.
### A DLG fájlformátum specifikációi
A DLG-fájlokat három különböző skálán terjesztik:

1. **Nagy léptékű** - általában megfelel:
- Az USGS 7,5-7,5 perc
- 1:24 000 és 1:25 000 méretarányú topográfiai négyszög térképsorozat
- 1:63 360 méretarány Alaszkában
- 1:30 000 méretarányú Puerto Rico
 

2. **Középső skála** – az USGS-ből származik:

- 30x60 perc

- 1:100 000 méretarányú térképsorozat
3. **Kis léptékű** – az Egyesült Államok Nemzeti Atlaszának USGS 1:2 000 000 méretarányú metszeti térképeiből származik
### Adatkategóriák
Kilenc különböző kategóriájú réteg vagy szolgáltatás érhető el a DLG-fájlokban:
1. Közterület-felmérési rendszer (PLSS)
2. Határok (BD)
3. Közlekedés (TR)
4. Vízrajz (HY)
5. Hipográfia (HP)
6. Nem vegetatív jellemzők (NV)
7. Felmérés ellenőrzése és markerek (SM)

8. Ember alkotta jellemzők (MS)

9. Vegetatív felszínborítás (SC)

A nagyméretű DLG fájlok mind a kilenc réteget kínálják, míg a közepes méretű fájlok a PLSS, BD, TR, HY és HP öt rétegét kínálják. A kisméretű DLG-k öt réteget kínálnak: PLSS, BD, TR, HY és MS.

## Hivatkozások

* [Digitális vonaldiagram – a Wikipédia által)](https://en.wikipedia.org/wiki/Digital_line_graph)


