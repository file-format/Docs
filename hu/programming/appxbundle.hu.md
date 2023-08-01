{
  "date" : "2021-04-22",
  "keywords": [ "appxbundle file", "extension", "format","how to open appxbundle file","appxbundle file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"appxbundle - Mi az APPXBundle fájl?",
  "description":"További információ az APPX fájlformátumról és az APPX-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "APPXBUNDLE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-19"
}

## Mi az APPXBUNDLE fájl?

Az APPXBUNDLE-fájl egy csomagfájl, amelyet a [Microsoft Visual Studio](https://visualstudio.microsoft.com/) segítségével hoztak létre, és Windows-alkalmazások (desktop és UWP) terjesztésére használják a [Microsoft Store](https://apps.microsoft.com/store/apps)-ban. Egy alkalmazás egy vagy több verzióját tartalmazza, amelyek meghatározott processzorarchitektúrát céloznak meg, például x86, x64 vagy ARM. Ez lehetővé teszi a végfelhasználó számára, hogy megkapja és telepítse az alkalmazás megfelelő verzióját a számítógép architektúrája alapján. Az APPXBUNDLE fájlok a szabványos [ZIP](/hu/compression/zip/) fájlformátum használatával vannak csoportosítva. A Microsoft Visual Studio Publish metódusa az alkalmazások csomagként történő közzétételére szolgál. Az egycsomagos alkalmazások [APPX](/hu/programming/appx/) fájlként kerülnek terjesztésre.

## APPXBUNDLE fájlformátum

Az APPXBUNDLE fájlokat ZIP fájlformátumban teszik közzé. Ha meg szeretné tekinteni az alkalmazáscsomag tartalmát, kicsomagolhatja annak tartalmát kicsomagoló segédprogramokkal, például a [WinZIP](https://www.winzip.com/en/) vagy a WinRAR segítségével.

## Hivatkozások

* [Függőségi csomagok .appx és .appxbundle csomagokhoz](https://www.ibm.com/docs/en/maas360?topic=catalog-dependency-packages-appx-appxbundle-packages)
* [APPX-fájlok létrehozása a Microsoft Visual Studio segítségével](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

