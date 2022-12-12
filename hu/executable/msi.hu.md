{
  "date" : "2021-06-30",
  "keywords" :[ "msi fájl", "MSI fájlformátum", "mi az msi fájl", "fájl", "msi példa", "msi fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az MSI-fájlformátumról és az MSI-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"MSI - Windows Installer csomagfájl",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Mi az MSI fájl?
A Windows programok telepítésére és indítására használt MSI-fájl; egy komplett csomag Microsoft Windowshoz, amely egy tipikus szoftverprogram telepítési információit tartalmazza, beleértve a telepítendő fontos fájlokat és a telepítés helyére vonatkozó információkat. Az MSI-fájlok tartalmazhatják a szoftverfrissítések csomagját is. Az MSI fájlok hasonlóak az [EXE](/hu/executable/exe/) fájlhoz, de az EXE néha nem tartalmazza a telepítői információkat, és a szoftver közvetlenül futhat az EXE fájl futtatásakor.

## MSI fájlformátum
A Windows Installer valójában a Microsoft Windows API (Application Programming Interface) és szoftverkomponense, amelyet szoftverprogramok telepítésére, eltávolítására és karbantartására használnak. A telepítési információk és az opcionális fájlok telepítési csomagokba és laza relációs adatbázisokba vannak csomagolva, amelyek COM Structured Storage-ként vannak felszerelve; jól ismert **MSI-fájlok**, .msi fájlkiterjesztéssel. A **.mst** kiterjesztésű csomagok a Windows Installer **Transformation Scripts**-jét, az **.msm** kiterjesztésű fájlok a **Merge Modules** kiterjesztést és a **.pcp** fájlkiterjesztést tartalmazzák. a **Patch Creation Properties**-hoz használatos. A Windows Installer fejlettebbé válik, miután jelentős változtatásokat hajt végre korábbi verzióihoz, a Setup API-hoz képest. A Windows Installer új szolgáltatásai a grafikus felhasználói felület keretrendszere és az eltávolítási folyamat automatikus generálása. Mostanra az önálló végrehajtható telepítő keretrendszerek alternatívájaként tartják számon.

### Az MSI-csomagok logikai felépítése
A csomag egy vagy több teljes termék telepítését jelöli, és általában egy **GUID** azonosítja. Egy termék egy vagy több összetevőből áll, és különböző jellemzők szerint csoportosul. A Windows Installer nem kezeli egyszerre a különböző termékek közötti függőséget. A csomagok logikai felépítése a következő elemekből áll:

- **Termékek**: Egyetlen, telepített, működő program vagy több program együttese egy termék. A terméket egyedi GUID azonosítja.
- **Jellemzők**: Tetszőleges számú összetevőt és egyéb alfunkciót tartalmazhat. A kisebb csomagok egyetlen szolgáltatásból is állhatnak.
- **Alkatrészek**: Az összetevőt a Windows Installer egységként kezeli; tartalmazhat programfájlokat, mappákat, rendszerleíró kulcsokat, COM-összetevőket és parancsikonokat.
- **Kulcsútvonalak**: A kulcs elérési útja egy adott fájl, ODBC adatforrás vagy beállításkulcs, amelyet a csomag szerzője kritikusként határoz meg egy adott összetevőhöz.

## Hivatkozások

* [Windows Installer – Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


