{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR2 fájlformátum - Canon Raw 2 képfájl",
  "description":"További információ a CR2 fájlformátumról és az API-król, amelyek CR2 fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Mi az a CR2 fájl?

A CR2 (Camera RAW 2) fájl egy Canon digitális fényképezőgépek által létrehozott RAW képfájl. Tárolja a fényképezőgép által rögzített eredeti, nem feldolgozott veszteségmentes képadatokat. A CR2 fájlformátumot a Canon fejlesztette ki digitális fényképezőgépeihez, és akár 14 bites RGB-s kiváló minőségű képeket is képes rögzíteni. Ez kiváló minőségű képeket készít elegendő utófeldolgozási hellyel. A CR2 képformátumot a Canon használta 350D, 20D és 1D fényképezőgép-modelljeiben. A CR2 fájlok RAW fájlok, és további metaadat-információkat tartalmaznak, például kamerainformációkat, objektívinformációkat, sorozatfelvételi információkat, fehéregyensúlyt és egyéb beállításokat.

## CR2 fájlformátum

A CR2 fájlok a fényképezőgép memóriakártyáján bináris fájlokként, Canon szabadalmaztatott fájlformátumban tárolódnak. A CR2 fájlformátum váltotta fel az eredetileg használt CRW fájlformátumot, majd magát a Canon RAW 3 fájlformátum váltotta fel később. A CR2 fájlformátum a [TIFF](/hu/image/tiff/) specifikációkon alapul, amely 4 képfájl-könyvtárat (IFD) tartalmaz.

|Eltolás |Tartalom |Megjegyzés|
---|---|---|
|0x0000 |A fejléc |tartalmazza a bájtsorrendet, a verziót és a RAW képhez képesti eltolást|
|számított |IFD#0 |ez a rész tartalmazza az Exif szakaszt, amely a Makernotes részt tartalmazza.
Információ a képről#0|
|számított |kép#0 |a kép kis változata (az eredeti méretének egynegyede), Jpeg-be tömörítve|
|számított |IFD#1 |Információ az 1. képről.|
|számított |kép#1 |a kép kis változata, Jpeg-be tömörítve|
|számított |IFD#2 |Információ a 2. képről.|
|számított |kép#2 |a kép kis változata, nem tömörítve|
|fejlécben| IFD#3| Információ a 3. képről, a teljes méretű RAW képről|
|számított |kép#3 |RAW képadatok, veszteségmentesen tömörítve Jpeg formátumban (nem RGB adatok!)|

## A CR2 fájlformátum előnyei

A képek RAW formátumban történő tárolása sok utófeldolgozást tesz lehetővé a fényképen, például a fehéregyensúly beállítását. Ez sokkal bonyolultabb és jelentős minőségromlást jelent más képfájlformátumokkal, például [JPEG](/hu/image/jpeg/).

## A CR2 jobb, mint a JPEG?

A CR2 fájlok nyers fájlok adatvesztés nélkül, és így minőségromlás nélkül. A JPEG másrészt veszteséges képfájlformátum, mivel elveszít néhány adatot a fájl méretének csökkentése érdekében. Így a CR2 fájlok kiváló minőségűek és alkalmasabbak retusálásra és javításra.

## Hivatkozások

* [CR2 fájlformátum] (http://lclevy.free.fr/cr2/)

