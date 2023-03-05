{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - Mi az APPX fájl?",
  "description":"További információ az APPX fájlformátumról és az API-król, amelyek APPX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Mi az APPX fájl?

Az APPX-fájl egy terjeszthető csomagfájlformátum, amelyet egy alkalmazások terjesztésére és telepítésére használnak. A Windows 8 rendszerrel került bevezetésre, hogy megjelenjen a Microsoft Windows Store-ban. Tartalmazza a Windows alkalmazás telepítéséhez szükséges összes fájlt. Ide tartoznak a metaadatok, a fájlok és a hitelesítő adatok. Egy modernebb csomagolási fájlformátum az MSIX, amelyet jelenleg gyakrabban használnak, mint az APPX.

## APPX fájlformátum - További információ

Az APPX-fájlok tömörített fájlokként kerülnek mentésre [ZIP](/hu/compression/zip/) fájlformátumban. Ezáltal a teljes csomag egy archív fájl, csökkentett fájlmérettel, amely könnyen feltölthető a Microsoft Store-ba.

## Hogyan lehet megtekinteni a fájlokat APPX fájlban?

Az APPX-fájl tartalmának vagy fájljainak megtekintéséhez kövesse az alábbi lépéseket.

1. Mivel az APPX-fájlok tömörített ZIP-fájlokként vannak tárolva, nevezze át a fájlt .zip kiterjesztésre
1. Használjon bármilyen kicsomagoló eszközt, például 7-Zip, WinZip vagy WinRAR, hogy kicsomagolja az APPX fájlban található fájlokat.

## Hogyan lehet APPX fájlt létrehozni?

Az APPX-fájlok létrehozásához két módszer használható.

1. A MakeApp.exe használatával – a [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) mindkettő létrehozására szolgál alkalmazáscsomagok (.msix vagy .appx) és alkalmazáscsomag-csomagfájlok (.msixbundle vagy .appxbundle). Ezen túlmenően ki tudja bontani a fájlokat egy alkalmazáscsomagból. A MakeApp.exe a Windows 10 SDK-val érhető el, és parancssorból használható.
1. A Microsoft Visual Studio használata – A fejlesztők általában [hoznak létre APPX fájlokat](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) a Microsoft Visual Studio használatával. Miután az alkalmazás fejlesztése befejeződött, és az alkalmazás készen áll a közzétételre, az APPX-csomagfájl létrehozása a Visual Studióból való közzététellel lehetséges.

## Hivatkozások

* [MSIX-csomag vagy csomag létrehozása a MakeAppx.exe segítségével](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [APPX-fájlok létrehozása a Microsoft Visual Studio segítségével](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

