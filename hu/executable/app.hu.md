{
"dátum": "2023-02-02",
  "keywords": [
"app fájl",
"mi az alkalmazásfájl",
"fájl",
"hogyan kell megnyitni az alkalmazásfájlt",
"app fájlkiterjesztés",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
  "description":"További információ az APP fájlformátumról és az API-król, amelyek APP fájlokat hozhatnak létre és nyithatnak meg.",
"title": "APP File Format - macOS Application Bundle",
  "linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app",
      "parent": "executable"
}
},
"lastmod": "2023-02-02"
}

## Mi az APP fájl?

Az .app fájl a macOS rendszeren egy speciális típusú könyvtár, amely egy adott alkalmazás futtatásához szükséges összes fájlt tartalmazza, beleértve a végrehajtható kódot, az erőforrásokat és a metaadatokat. Az .app kiterjesztés jelzi az operációs rendszernek, hogy ezt a könyvtárat egyetlen egységként kell kezelni, nem pedig különálló fájlok gyűjteményeként, és hogy közvetlenül a Finderből vagy a Dockból indítható.

A Finder a macOS alapértelmezett fájlkezelő alkalmazása. Lehetővé teszi a fájlok és könyvtárak böngészését és rendszerezését a számítógépén. A Dock a macOS olyan funkciója, amely gyors hozzáférést biztosít a gyakran használt alkalmazásokhoz és dokumentumokhoz. Mind a Finder, mind a Dock lehetővé teszi az alkalmazások elindítását az .app fájljaikra kattintva, ami megnyitja a megfelelő alkalmazáscsomagot. Amikor elindít egy alkalmazást, az .app csomagban lévő végrehajtható kód lefut, így az alkalmazás elérhetővé válik. Az .app fájl az alkalmazást reprezentálja a fájlrendszerben, és lehetőséget biztosít a felhasználó számára az alkalmazás eléréséhez és elindításához.

Ha jobb gombbal kattint egy .app fájlra a Finderben MacOS rendszeren, és kiválasztja a „Csomag tartalmának megjelenítése” lehetőséget, megtekintheti az alkalmazáscsomag belső szerkezetét. Ez akkor hasznos, ha az alkalmazás által használt erőforrásokhoz vagy fájlokhoz szeretne hozzáférni, vagy ha hibaelhárítási célból meg szeretné tekinteni az alkalmazás tartalmát. Az .app fájlok csomagtartalma általában olyan erőforrások könyvtárait tartalmazza, mint a képek és hangok, valamint az alkalmazás végrehajtható kódja. Egy .app fájl tartalmának felfedezésével mélyebb betekintést nyerhet az alkalmazás összeállításába és működésébe.

## APP fájl hogyan nyitható meg?

Egy .app fájl megnyitásához macOS rendszeren egyszerűen kattintson duplán a fájlra a Finderben. Ezzel elindítja az .app csomagban található alkalmazást. Ha az alkalmazás telepítve van a rendszerére, és az .app fájltípushoz van társítva, a fájlra duplán kattintva az alkalmazás automatikusan elindul. Ha az alkalmazás nincs társítva az .app fájltípushoz, akkor előfordulhat, hogy jobb gombbal kell rákattintania a fájlra, és ki kell választania a „Megnyitás ezzel” lehetőséget a megfelelő alkalmazás kiválasztásához.

Az „open” paranccsal megnyithat egy .app fájlt a macOS terminálján. Ehhez a "cd" paranccsal navigáljon abba a könyvtárba, ahol az .app fájl található, majd futtassa a következő parancsot:

```
open <AppName>.app 
```

ahol<AppName> az elindítani kívánt alkalmazás neve. Ezzel elindítja az alkalmazást, mintha duplán kattintott volna rá a Finderben. Az "open" parancs egy általános célú segédprogram, amellyel számos különböző típusú fájlt lehet megnyitni, beleértve az alkalmazásokat, dokumentumokat és könyvtárakat. Amikor az „open” parancsot használja egy .app fájlon, az elindítja a csomagban található alkalmazást.

## Hivatkozások
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
