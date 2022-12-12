{
  "date" : "2021-08-11",
  "keywords" :[ "vox", "file", "extension", "format", "audio", "ADPCM", "Dialogic ADPCM", "Xentec VOX Studio", "vox extension", "vox files"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a VOX fájlformátumról és az API-król, amelyek VOX fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"VOX - Audio fájl formátum",
  "linktitle" : "VOX",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-11"
}

## Mi az a VOX fájl? ##

Alacsony mintavételezési gyakoriság mellett a VOX fájlok digitalizált hangadatok tárolására vannak megadva. Ezek olyan hangfájlok, amelyeket általában a telefonos kommunikációhoz meghatározott alkalmazásokban használnak. Ez a típusú fájlformátum veszteséges tömörítési algoritmust használ, amely optimalizálja a hangot.

A beszédalkalmazásokban általánosan használt VOX fájlok előre rögzített hangutasításokat tartalmaznak. Az ilyen típusú fájlformátumokat más népszerűbb formátumokká is konvertálják. Ezek használhatók Windows operációs rendszerben és macOS-ben.

Leginkább hangos felvételekhez és tömörítéshez használják. Ebben a formátumban a többszólamú adatok nem tárolhatók, mivel csak homofób adatokat támogatnak.



## Rövid története ##

A VOX fájlok a Dialogic DMV és JCT nevű médiatábláihoz kapcsolódnak. Ezek a VoxWare-hez és sok más szoftverhez tartoznak. Régen elavult formátumnak számított.

Elavult formátumként ezt követően nem használták. Más ADPCM formátumokhoz hasonlóan 4 bitre tömörítették. Ezen fájlok jellemzői elég közel állnak a [WAV](/hu/audio/wav) fájl specifikációihoz.


## Formátumspecifikációk ##

Ez a típusú fájlformátum kompatibilis a Windows operációs rendszer programjaival, mint például a Xentec Vox Studio. Sajátos jellemzői vannak, amelyeket az emberek beszédének stimulálására használnak. Az arcade játékok többnyire ezt a formátumot használják. A VOX fájlkiterjesztés 32 bájtos fejléccel, valamint 10 bájtos indexekkel és keretekkel rendelkezik. A tényleges hangadatokat a rendszer keretekben, szegmensek formájában, egyetlen fájlban menti. A kódolás típusától függően minden egyes keretben több bájt különböző formája van.

A hang tisztaságát alacsony mintavételezési frekvencián tartják fenn, ami a legtöbb hangformátumban ritka. Az ezekben alkalmazott algoritmus matematikai volt.

Ezt a fájlt az ADPCM kódolja. Rövidre zárja a 16 bites hangadatokat és a 4 bites tömörítést. Így előnye van, ha nagyobb méretű hanginformációkat menthet kompakt formában VOX fájlok segítségével.


## Referenciák ##

* [VOX – a Wikipedia által](https://en.wikipedia.org/wiki/Dialogic_ADPCM)

