
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML fájl – Microsoft Assistance Markup Language File",
  "description":"További információ az AML-fájlokról és az API-król, amelyek AML-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML – Microsoft Assistance Markup Language File

## Mi az AML fájl?

Az AML (Assistance Markup Language) fájl a Microsoft Assistance Markup Language (MAML) segítségével generált XML-fájl. A Microsoft fejlesztette ki, hogy online segítséget nyújtson a Microsoft Windows operációs rendszerhez. Ezt megelőzően a Windows súgója a lefordított HTML [CHM](/hu/web/chm/) fájlformátumban volt elérhető. Az AML-fájlok strukturált dokumentumot biztosítanak, amely lehetővé teszi az alkalmazások számára, hogy forráskódot és támogató súgóoldalakat hozzanak létre. Ez lehetővé teszi a dokumentumok és alkotóelemeik kontextusuk szerinti meghatározását. Az AML súgófájljait online teszik közzé, és beállíthatók úgy, hogy az online elérhető csomagfrissítésekből frissüljenek.

## MAML fájlstruktúra

A MAML segítségével generált AML-fájlokat [XML](/hu/web/xml/) fájlként menti a rendszer, amely az aktív fogalmak széles körének kifejezésére használható. Vezetett súgót (aktív tartalom varázsló) is nyújthat, amely a súgófájlt interaktívvá teszi a felhasználó számára a lépésről lépésre varázsló segítségével.

A MAML segítségével létrehozott AML-fájl a szerzői struktúráját követi, amely szegmensekre osztható, például:

* Fogalmi
* GYIK
* Szójegyzék
* Eljárás
* Hivatkozás
* Újrafelhasználható tartalom
* Feladat
* Hibaelhárítás és
* Bemutató

## Hogyan készítsünk MAML fájlokat?

MAML fájlok a következő módszerek egyikével hozhatók létre:

* A Sandcastle használata – Sémák és program végrehajtható fájlok csomagját használja a súgófájl létrehozásához. Ez az eszköz azonban megszűnt.
* DocProject használata – A Microsoft Visual Studio beépülő modulja, amely a Microsoft Visual Studióból futtatható a súgótartalom létrehozásához.

MAML fájlok hozhatók létre a Sandcastle segítségével, amely .XSL sémák és programok futtatható fájljai. Létrehozhatók a DocProject, a Microsoft Visual Studio súgószerkesztő eszközének bővítményével is.

## Hivatkozások

* [XML-alapú súgó létrehozása a PlatyPS segítségével
](https://learn.microsoft.com/en-us/powershell/scripting/dev-cross-plat/create-help-using-platyps?view=powershell-7.2)
* [Microsoft Assistance Markup Language](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML – Arc Macro Language File

## Mi az ARC Macro AML fájl?

Az AML (ARC Macro Language) fájl az ArcInfo Workstation GIS alkalmazással generált parancsfájl. Az ARC Macro Language nyelven íródott, amely egy szabadalmaztatott, magas szintű algoritmikus nyelv GIS alkalmazások létrehozásához az ArcInfoban. Az AML-t az ESRI tervezte 1986-ban, és azt a célt szolgálta, hogy alkalmazásokat hozzanak létre parancssori ARCINFO GIS rendszerükből. Parancsfájlként az AML fájlok tartalmazhatnak parancsfájl-parancsokat számos feladat elvégzésére, például felhasználói felület összetevőinek létrehozására és a térképadatok manipulálására.

## AML fájlformátum – További információ

Az AML, mivel script fájlok, az információkat egyszerű szöveges fájlként menti a lemezre. Az AML szintaxist követi, amely a PRIMOS operációs rendszer CPL shell nyelvén alapult. Az AML nyelvet felváltotta az ESRI geofeldolgozó keretrendszere, amely az ArcGIS programcsomag része, és ArcObjects segítségével nyújt programozási támogatást VBA-n vagy Pythonon keresztül.

## Hivatkozások

* [ARC Macro Language](https://en.wikipedia.org/wiki/ARC_Macro_Language)
* [AML használata Script Tools-szal](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

