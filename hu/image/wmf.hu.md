{
  "date" : "2019-10-11",
  "keywords" :[ "wmf fájl", "wmf fájl formátum", "mi az a wmf fájl", "fájl", "wmf példa", "wmf fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Microsoft Windows metafájl formátum",
  "description":"További információ a WMF fájlformátumról és az API-król, amelyek WMF fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a WMF fájl?

A WMF kiterjesztésű fájlok a Microsoft Windows Metafile-t (WMF) képviselik a vektoros és bittérképes képadatok tárolására. Hogy pontosabbak legyünk, a WMF a grafikus fájlformátumok vektoros fájlformátum kategóriájába tartozik, amely eszközfüggetlen. A Windows Graphical Device Interface (GDI) a WMF-fájlban tárolt funkciókat használja a kép képernyőn való megjelenítéséhez. Később megjelent a WMF továbbfejlesztett változata, az Enhanced Meta Files (EMF), amely a formátumot funkciókban gazdagabbá teszi. Gyakorlatilag a WMF hasonló az SVG-hez.

## A WMF fájlformátum specifikációi ##

Egy WMF-fájl 16 bites fájlformátumra hivatkozott a Windows 3.0 rendszerrel való elindításakor. A fájlformátum változó hosszúságú rekordok sorozatából áll, amelyek grafikus rajzparancsokat, objektumdefiníciókat és tulajdonságokat tartalmaznak. Mivel a WMF fájlok a GDI számára megjelenített parancsokon alapulnak a kép megrajzolásához, a kép digitális rögzítésének is nevezik, amelyet vissza lehet játszani a kép reprodukálásához. A WMF teljes fájlformátum-specifikációja elérhető az interneten, és a WMF-fájlokkal működő alkalmazások fejlesztésekor hivatkozni kell rájuk. A WMF-fájlok a következők szerint vannak rendezve:

* WMF fejléc rekord
* WMF rekord(ok)
* WMF-fájlvégi rekord

### WMF fejléc rekord ###

A **META_HEADER rekord** olyan információkat tartalmaz, amelyek meghatározzák a metafájl jellemzőit, többek között:

* A metafájl típusa
* A metafájl verziója
* A metafájl mérete
* A metafájlban meghatározott objektumok száma
* A legnagyobb egyedi rekord mérete a metafájlban

### WMF elhelyezhető fejléc rekord ###

A **META_PLACEABLE Record** kiterjesztett információkat tartalmaz a képről, többek között:

* Határoló téglalap
* Logikai egység mérete, méretezéshez
* Ellenőrző összeg az érvényesítéshez

### WMF rekord ###

A WMF rekordok általános formátummal rendelkeznek, amelyet a specifikációs dokumentum határoz meg. Minden WMF rekord a következő információkat tartalmazza:

* A rekord mérete
* A rögzítési funkció
* A rögzítési funkció paraméterei, ha vannak

## Referenciák ##

* [[MS-WMF]: Windows Metafile Format](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Windows MetaFile – Wikipédia](https://en.wikipedia.org/wiki/Windows_Metafile)

