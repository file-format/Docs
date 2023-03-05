{
  "date" : "2021-02-15",
  "keywords" :[ "asf fájl", "asf fájl formátum", "mi az asf fájl", "fájl", "asf példa", "asf fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - Advanced Systems File Format",
  "description":"További információ az ASF-fájlformátumról és az ASF-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Mi az ASF fájl?

Az .asf kiterjesztésű fájl egy multimédiás fájlformátum digitális médiafolyamok hálózaton keresztüli tárolására és lejátszására. Ez egy konténerfájlformátum, amely video- és audiotartalmat is tartalmazhat az online streaminghez. Ritkán találsz ASF-fájlokat, és nagyobb valószínűséggel találkozhatsz a Windows Media Audio ([WMA](/hu/audio/wma/)) és a Windows Media Video ([WMV](/hu/video/wmv/)) fájlokkal, amelyek egyaránt ASF-fájlokat adnak meg. megfelelő kodekekkel kódolt tartalommal. A Windows médiafájlok a Windows Media Format SDK segítségével hozhatók létre és olvashatók.

## ASF fájl formátum

Egy ASF-fájl több független vagy függő adatfolyamot is tartalmazhat. Ez magában foglalhat több hangfolyamot többcsatornás hanghoz vagy több bitsebességű videofolyamot. A többszörös bitráta alkalmassá teszi a streameket különböző sávszélességeken történő átvitelre. Ezenkívül az ASF-fájlban lévő adatfolyamok lehetnek tömörített vagy tömörítetlen formátumban. A legjobb tömörítés a Microsoft Windows Media Audio and Video 9 Series kodekekkel érhető el. Az ASF-fájlformátum teljes specifikációi a [Microsoft webhelyén](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc) érhetők el.

### ASF legfelső szintű fájlstruktúra

Az ASF-fájlok logikailag háromféle legfelső szintű objektumot tartalmaznak:

* "Header Object" - kötelező, és minden ASF-fájl elejére kell helyezni
* `Data Object` - kötelező, és követnie kell a fejléc objektumot
* "Index objektum(ok)" - opcionális, de hasznos időalapú véletlenszerű hozzáférést biztosítva az ASF-fájlokhoz

A következő képen az ASF-fájlok legfelső szintű fájlstruktúrája látható.

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF legfelső szintű fejlécobjektum

A Header objektum egy jól ismert bájtsorozatot biztosít az ASF-fájlok elején, és opcionálisan tartalmazhat metaadatokat, például bibliográfiai információkat. Minden olyan információt tartalmaz, amely az adatobjektumban található információ megfelelő értelmezéséhez szükséges. A fejlécobjektum több szabványos objektumot is tartalmazhat, beleértve, de nem kizárólagosan:

* File Properties Object – Globális fájlattribútumokat tartalmaz.
* Stream Properties Object – Meghatározza a digitális médiafolyamot és annak jellemzőit.
* Header Extension Object – Lehetővé teszi további funkciók hozzáadását egy ASF-fájlhoz, miközben megőrzi a visszamenőleges kompatibilitást.
* Tartalomleírás Objektum – Bibliográfiai információkat tartalmaz.
* Script Command Object – A lejátszási idővonalon végrehajtható parancsokat tartalmaz.
* Marker Object – Megnevezett ugrási pontokat biztosít egy fájlon belül.

A fejléc objektum a következő struktúrával van ábrázolva:

|Mező neve |Mező típusa |Méret (bit)|
---|---|---|
|Objektumazonosító| GUID| 128|
|Tárgy mérete| QWORD| 64|
|Fejlécobjektumok száma| DWORD| 32|
|Fenntartva1| BYTE| 8|
|Fenntartva2| BYTE| 8|

#### ASF legfelső szintű adatobjektum

Az ASF-fájlhoz tartozó összes digitális médiaadatot az adatobjektum tartalmazza, és ASF-adatcsomagok formájában tárolja. Minden adatcsomag rögzített hosszúságú, és egy vagy több digitális médiafolyam adatait tartalmazza.

#### ASF legfelső szintű indexobjektumok

Az ASF legfelső szintű indexobjektumainak két típusa van:

* `Simple Index Object` – Az ASF-fájlban lévő videoadatok időalapú indexét tartalmazza. Az indexbejegyzések közötti időintervallum állandó, és az egyszerű indexobjektumban tárolódik.
* `Indexobjektum` - Az indexobjektumra, a médiaobjektum-indexobjektumra és az időkód-indexobjektumra utal, amelyek formátuma hasonló. Az egyszerű indexobjektumhoz hasonlóan az indexobjektum is meghatározott időintervallumban indexel, de nem korlátozódik a videofolyamokra.

## Hivatkozások

* [ASF-fájlformátum – Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [QuickTime fájlformátum – Wikipédia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

