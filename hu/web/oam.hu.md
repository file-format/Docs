{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAM fájl – Adobe Edge Animate Widget fájlformátum",
  "description" :"További információ az OAM-fájlokról és az API-król, amelyek OAM-fájlt hozhatnak létre és nyithatnak meg.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## Mi az OAM fájl?

Az .oam fájl egy animált widget fájl, amelyet az Adobe Edge Animate Widgetből exportáltak. Az OAM widget fájlformátumban exportált animációk beilleszthetők más Adobe-alkalmazásokba, például az InDesign Documents ([INDD-fájl](/hu/page-description-language/indd/), a Dreamweaver és a Muse. Az OAM-fájlok olyan telepítési csomagok beilleszthetők más Adobe-projektekbe, hogy kihasználhassák őket. Az OAM-fájlok információkat tartalmaznak az animáció eszközeiről, viselkedéséről és akcióscript-kódjáról. OAM-fájlt hozhat létre egy Adobe Animate projekt [.AN-fájl] (/hu/web/an/) közzétételével. .
A felhasználók egy Edge Animate projektből (.AN fájl) való közzététellel hozhatnak létre OAM-fájlokat.

## OAM fájlformátum

Az OAM-fájl tömörített [ZIP](/hu/compression/zip/) archívumként kerül a lemezre mentésre. Ez azt jelenti, hogy átnevezheti a fájl kiterjesztését .zip-re, és kicsomagolhatja bármilyen tömörítő segédprogrammal, például WinZIP vagy WinRAR segítségével. A csökkentett fájlméret megkönnyíti az animáció átvitelét és megosztását más felhasználókkal az interneten keresztül.

### OAM fájlstruktúra

Az .oam fájlok belső fájlstruktúrája védett, és az Adobe nem dokumentálja nyilvánosan. Ismeretes azonban, hogy az .oam fájlok fájlok és erőforrások (például grafikák, hanganyagok és ActionScript-kódok) gyűjteményét tartalmazzák egyetlen fájlba csomagolva. Az .oam fájlok tartalma tartalmazhat [XML](/hu/web/xml/) fájlokat, SWF fájlokat és egyéb erőforrásfájlokat. Az .oam fájl pontos szerkezete a létrehozásához használt Adobe Animate konkrét verziójától, valamint a fájlban található animáció és elemek típusától függ.

Egy OAM-fájl a következő információkat tartalmazza.

`Eszközök:` Információk az animációban használt grafikai, hang- és videoelemekről.

`Viselkedések:` Az animációban előforduló műveletek és interakciók leírása.

`ActionScript kód:` Az animáció viselkedésének és interaktivitásának vezérlésére használt kód.

Közzétételi beállítások: Információk az animáció közzétételi platformjáról és formátumáról, például HTML5 vagy AIR.

`Metaadatok:` További információk, például az animáció szerzője, létrehozásának dátuma és verziószáma.

## Hogyan lehet megnyitni az OAM fájlt?

A következő alkalmazásokat használhatja az OAM fájlok megnyitásához.

* Adobe Edge Animate CC (megszűnt)
* Adobe Animate 2023
* Adobe InDesign 2023
* Adobe Dreamweaver 2021

## Hivatkozások

* [OAM Publishing](https://helpx.adobe.com/animate/using/OAM-publishing.html)

