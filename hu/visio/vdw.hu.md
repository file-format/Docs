{
  "date" : "2019-10-11",
  "keywords" :[ "vdw", "vdw fájl", "vdw fájlformátum", "vdw fájl típusa", "fájl", "típus", "mi az a vdw fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW – Visio Graphics Service File Format",
  "description":"További információ a VDW fájlformátumról és az API-król, amelyek VDW fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## Mi az a VDW fájl?

A VDW a Visio Graphics Service fájlformátuma, amely meghatározza a webes rajzok megjelenítéséhez szükséges adatfolyamokat és tárolókat. A webes rajz rajzoldalak, alakzatok, betűtípusok, képek, adatkapcsolatok és diagramfrissítési információk gyűjteménye, amelyek vektoros vagy raszteres rajzként jeleníthetők meg. A VDW fájlok a Microsoft Visio programban is megnyithatók, de elsősorban webes használatra mentik őket. A Microsoft Visio lehetőséget kínál a Visio-fájlok számos különböző fájlformátumra konvertálására, beleértve a [PNG](/hu/image/png/), [BMP](/hu/image/bmp/), [PDF](/hu/pdf/) és más formátumokat.

## **VDW** fájlformátum

A VDW-fájlformátum műszaki specifikációi a [Microsoft]-tól elérhetők online (https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx), és a fejlesztők hivatkozhatnak rájuk a létrehozáshoz. alkalmazások. A műszaki dokumentum a tárolókat és adatfolyamokat tartalmazó összetett fájlban található adatokat írja le. A webes rajzok megjelenítése egy VisioServerData nevű adatfolyamon keresztül lehetséges egy ZIP archívumban. Az archívumban található ShapGraphic XML rész leírja a webes rajzban megjelenített grafikus elemeket, és XAML-ben (Extensible Application Markup Language) vannak kifejezve. A ZIP-archívum XML-részeinek gyűjteménye leírja a webes rajz adatkapcsolatát, az alakjával kapcsolatos információkat és a diagramfrissítési logikát. Ezek a részek XML-ben vannak kifejezve. A DataGraphic XML rész azokat az újraszámított tulajdonságokat írja le, amelyeket ki kell értékelni, miután a webes rajzban lévő adatok frissítésre kerültek az adatforrásból. A ZIP archívum további elemei információkat tartalmaznak a webes rajzban használt betűtípusokról és képekről.

|![Fájl lehetséges megvalósítása](/hu/web/vdw.png "Egy fájl lehetséges megvalósítása")

## Hivatkozások

* [[MS-VGSFF]: Visio Graphics Service (.vdw) fájlformátum](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

