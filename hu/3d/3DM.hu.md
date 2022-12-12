{
  "date" : "2021-08-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3DM",
  "description":"Tudjon meg többet a 3DM fájlformátumról és az API-król, amelyek képesek megnyitni és létrehozni 3DM fájlokat.",
  "linktitle" : "3DM",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-08-13"
}

## Mi az a 3DM fájl?

A .3dm kiterjesztésű fájl egy nyílt forráskódú fájlformátum, amelyet 3D grafikus szoftverekhez használnak. 3D-s modelleket tartalmaz, valamint azok függő elemeit, például felület-, pont- és görbeinformációkat. A 3DM fájlformátumot az [openNURBS](https://github.com/mcneel/opennurbs) kezdeményezés fejlesztette ki a 3D geometria alkalmazások közötti pontos átvitelére. A 3DM fájlok megnyithatók és konvertálhatók olyan alkalmazásokkal, mint a Rhinoceros, az SAP VEViewer, a Moment of Inspiration és a Right Hemisphere Deep View.

## 3DM fájlformátum

Az [openNURBS](https://github.com/mcneel/opennurbs) egy nyílt forráskódú eszközkészlet, amely tartalmazza a 3DM fájlformátum specifikációit, dokumentációt, C++ forráskód-könyvtárakat és .NET 2.0 összeállításokat a fájlformátum olvasásához és írásához.

### 3DM példafájlok

Néhány példa 3DM-fájl letölthető az openNURBS [examples](https://github.com/mcneel/opennurbs/tree/7.x/example_files) szakaszból. Ezeket az openNURBS eszközkészlet segítségével lehet betölteni és megjeleníteni.

## Hogyan lehet 3DM fájlokat olvasni vagy írni?

Az [openNURBS](https://github.com/mcneel/opennurbs) könyvtárak lehetővé teszik, hogy bárki olvassa és írhassa a 3DM fájlformátumot Rhino nélkül. C++ forráskódot biztosít egy olyan könyvtárhoz, amely 3D modelleket olvas és ír az openNURBS fájlformátum használatával. Ez az eszközkészlet NURBS kiértékelő eszközöket és elemi geometriai és 3D nézet-manipulációs eszközöket, valamint forráskódot is tartalmaz számos példaprogramhoz. Az [Orrszarvú](https://discourse.mcneel.com/c/opennurbs/6) támogatási fóruma gazdag tartalom- és vitahely, ahol megoszthatják a 3DM-közösség problémáit, és megtalálhatják a megoldásokat.

## Referenciák ##

* [Orrszarvú](https://www.rhino3d.com/download/openNURBS)
* [Orrszarvú – Wikipédia](https://en.wikipedia.org/wiki/Rhinoceros_3D)
* [openNURBS a GitHubon](https://github.com/mcneel/opennurbs)

