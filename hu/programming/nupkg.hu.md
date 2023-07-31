{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUPKG fájl - NuGet csomagfájl",
  "description":"További információ a NUPKG fájlformátumról és az API-król, amelyek NUPKG fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## Mi az a NUPKG fájl?

A NUPKG-fájl egy olyan csomagfájl, amely a NuGet szoftver által a .NET-projektekben használható csomagok létrehozásához használandó forráskódot tartalmaz. A NuGet Package Manager összetevő a Microsoft Visual Studio részeként van telepítve a csomagok letöltéséhez az online csomagok tárházából. A NUPKG-fájlok segítenek a fejlesztőknek a legújabb csomagok lekérésében a [Nuget.org](https://nuget.org) webhelyről a NuGet Package Manager használatával a fejlesztői csomagok manuális letöltése és telepítése helyett. A NUPKG fájlok NUSPEC fájlokból épülnek fel, és lekéréskor telepítik a csomagot a felhasználói rendszerre.

## NUPKG fájlformátum

A NUPKG fájlok [ZIP](/hu/compression/zip/) archívumok, amelyek a benne lévő csomagolt könyvtárakat tartalmazzák. Letöltéskor átnevezhető .zip-re, és kibontható bármilyen szabványos zip-segédprogrammal, mint például a WinZIP, a 7-Zip és az Apple Archive Utility.

## Referencia

* [Nuget.org](https://nuget.org)
* [Gyorsindítás: Telepítsen és használjon csomagot a Visual Studióban (csak Windows)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- stúdió)
* [Nuget-csomag létrehozása és közzététele](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- cli)

