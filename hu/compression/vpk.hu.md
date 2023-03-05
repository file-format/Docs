{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VPK fájl – PlayStation Vita alkalmazáscsomag fájlformátuma",
  "description":"További információ a VPK fájlformátumról és az API-król, amelyek VPK-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## Mi az a VPK fájl?

A .vpk kiterjesztésű fájl egy tömörített archív csomagfájl, amely harmadik féltől származó alkalmazások telepítésére szolgál a Sony PlayStation Vita játékkonzolra. Ezeket a fájlokat csak a HENkaku jailbreak Vita PlayStation rendszerére lehet telepíteni, amely lehetővé tette a PS Vita és a PSTV számára, hogy testreszabott, felhasználó által létrehozott tartalmat használjanak. A VPK archív fájl tartalmazza a játékot alkotó összes tartalmat, beleértve a képeket, például a [PNG](/hu/image/png/) fájlokat, a beállítási fájlokat, mint például a [.bin](/hu/disc-and-media/bin/), és bármilyen konfiguráció [XML](/hu/web/xml/) fájlformátumban.

## VPK fájl formátum

A VPK-fájlok szabványos tömörített [ZIP](/hu/compression/zip/) archívumként kerülnek lemezre. Ezek több mappát és egyéb kapcsolódó fájlokat tartalmazhatnak a Vita Gaming Console-ra telepítendő, harmadik féltől származó alkalmazásokhoz. A VPK-csomagfájl tartalmának megtekintéséhez nevezze át a kiterjesztését .vpu-ról .zip-re, és bontsa ki a tartalmat szabványos kicsomagoló segédprogramokkal, például WinZip vagy WinRAR segítségével.

A Valvesoftware részletes információkat tartalmaz a [VPK fájlformátumról](https://developer.valvesoftware.com/wiki/VPK_File_Format), amelyre a fejlesztő szemszögéből hivatkozni lehet.

## Hogyan telepítsünk VPK fájlokat?

A VPK-fájlok a VPK.exe parancssori segédprogramból telepíthetők. Windows operációs rendszeren a fájlok eldobhatók a vpk.exe fájlba, amely az összes csomagolt fájlt tartalmazó \*.vpk fájlt adja vissza. Alternatív megoldásként a parancssori eszköz a következőképpen használható.

### VPK létrehozása és fájlok hozzáadása

```
vpk <dirname>
```

### VPK fájlok kibontása

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK Viewer

* [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## Hivatkozások

* [VPK fájlformátum](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [VPK-fájlok](https://developer.valvesoftware.com/wiki/VPK)

