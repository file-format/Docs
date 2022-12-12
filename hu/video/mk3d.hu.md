{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MK3D fájlformátum",
  "keywords" :[ "mk3d", "matroska video", "mkv format", "stereoscopic 3d", "StereoMode", "video", "file", "format" ],
  "description":"Tudjon meg többet a Matroska által létrehozott sztereoszkópikus 3D videók MK3D fájlformátumáról és az MK3D fájlokat létrehozni és megnyitni képes API-król.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## Mi az MK3D fájl? ##

Az MK3D fájlok a Matroska videóformátumok családjába tartoznak. Ezek a fájlok valójában **sztereoszkópikus 3D** videók, amelyeket Matroska 3D formátumban készítettek. Az MKV-fájltároló egy StereoMode mező értékét használja a sztereoszkópikus 3D-s videóanyag típusának meghatározásához. A StereoMode érték is elérhető a régi sztereó 3D videók megjelenítéséhez a cián és a piros színek elválasztásával (AnaGlyph)

## Műszaki információk ##
A 3D videókat a következő két módon lehet tömöríteni:

- Külön pálya minden szem számára.
- Kombinálja az egyes szemkövetéseket egyetlen sávba.

Az MKV fájltároló mindkettőt támogatja.

Az egysávos videóknál, amelyek könnyebbek a bennük lévő 3D-s anyagokkal, be kell állítani a **StereoMode** mezőt, amely eldönti, hogy a síkok mono vagy bal jobb kombinált sávban legyenek összeállítva. A következő StereoMode mezőértékek egyikét használhatja:

|Érték | Leírás |
|---|---|
|0| mono|
|1| egymás mellett (bal szem az első)|
|2| felső-alsó (jobb szem az első)|
|3| fent-lent (bal szem az első)|
|4| tábla (jobb az első)|
|5| tábla (bal az első)|
|6| sor átlapolt (jobb az első)|
|7| sor átlapolt (bal az első)|
|8| oszlop átlapolt (jobb az első)|
|9| oszlop átlapolt (bal az első)|
|10| anaglifa (cián/piros)|
|11| egymás mellett (jobb szem az első)|
|12| anaglifa (zöld/bíbor)|
|13| mindkét szem befűzve egy blokkba (a bal szem az első) (mezőszekvenciális mód)|
|14| mindkét szem befűzve egy blokkba (jobb szem az első) (mezőszekvenciális mód)|

A több pálya esetén az MKV konténernek külön kell eldöntenie az egyes pályák funkcionalitását. A **TrackOperation** és a **TrackCombinePlanes** a munka elvégzésére szolgál.


## Hivatkozások ##

- [Matroska specifikációs megjegyzések](https://www.matroska.org/technical/notes.html)
- [MKV fájltároló támogatása sztereó 3D-s videókhoz és az MK3D-fájlokhoz](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d- fájlok/)

