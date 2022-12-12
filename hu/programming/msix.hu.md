{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - Mi az MSIX fájl?",
  "description":"További információ az MSIX fájlokról és API-król, amelyek MSIX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Mi az MSIX fájl?

Az MSIX-fájl egy Windows-alkalmazás-csomagolási formátum, amelyet alkalmazások létrehozására és terjesztésére használnak a Windows 10 rendszerben. Ez a modern csomagfájlformátum a [APPX](/hu/programming/appx/) és az MSI-hez képest, amelyeket végül kivezetünk. ehhez az új fájlformátumhoz. Használható Win32, WPF és Windows Forms alkalmazások telepítéséhez. Az MSIX fájlok megbízhatóak, és céljuk a hálózat és a lemezterület optimalizálása. A fejlesztők ezek segítségével programokat terjesztenek a végfelhasználókhoz a Microsoft Store-on (korábban Windows Store néven) keresztül.

## MSIX fájlformátum – További információ

Az MSIX fájlok [ZIP](/hu/compression/zip/) tömörítésűek, és az összes fájl a csomagolt fájlban található. Az alkalmazáshoz kapcsolódó fájlok mellett az MSIX fájl [.xml](/hu/web/xml/) konfigurációs fájlokat is tartalmaz, amelyek az alkalmazás telepítésével kapcsolatos információkat tartalmaznak.

## Mit tartalmaz az MSIX csomag?

Egy MSIX-csomag a következő fájlokból áll.

* `AppxBlockMap.xml` – A csomagblokk-leképezési fájlként ismert XML-dokumentum, amely tartalmazza az alkalmazásfájlok listáját indexekkel és kriptográfiai kivonatokkal a csomagban tárolt minden egyes adatblokkhoz.
* `AppxManifest.xml` – Az MSIX-alkalmazások telepítéséhez, megjelenítéséhez és frissítéséhez szükséges információkat tartalmazó XML-dokumentum. Ez az információ tartalmazza a csomagazonosítót, a csomagfüggőségeket, a szükséges képességeket, a vizuális elemeket és a bővíthetőségi pontokat.
* `AppxSignature.p7x` – A csomag aláírásakor generált fájl. Minden MSIX csomagot alá kell írni a telepítés előtt. Az AppxBlockmap.xml segítségével a platform képes telepíteni a csomagot és ellenőrizni.

## Hivatkozások

* [MSIX áttekintés](https://docs.microsoft.com/en-us/windows/msix/overview)
* [APPX-fájlok létrehozása a Microsoft Visual Studio segítségével](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

