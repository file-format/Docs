{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "kiterjesztés", "fájl", "formátum", "rendszer", "LNK-fájl", "link", "LNK-fájlok", "LNK-dokumentumok", "alkalmazás", "programok" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Link fájlformátum",
  "description":"További információ az LNK fájlformátumról és az LNK-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Mi az LNK fájl? ##

Az LNK-fájl, amely a Mac rendszeren található identitáshoz hasonló, egy Windows-alternatíva vagy „hivatkozás”, amely egy eredeti képes dokumentummappához vagy programhoz való kapcsolatként szolgál. Tartalmazza a parancsikon célhelyének típusát, pozícióját és fájlnevét, valamint a céldokumentumot megnyitó alkalmazást és egy további gyorsbillentyűt.

Windows rendszerben egyenesítsen egy fájlt, mappát vagy végrehajtható programot, és válassza a Parancsikon létrehozása lehetőséget. A fájlformátum helye és a „Kezdő” könyvtár az LNK-fájlok két alapvető jellemzője. Az LNK-fájlok fájlformátuma maszkolt, és egy ívelt nyíl jelzi, hogy parancsikonokról van szó.

## LNK fájlformátum ##

Az LNK-fájlformátumok általában ugyanazzal az ikonnal rendelkeznek, mint a célfájlok, de egy kis görbült nyíl hozzáadásával jelzi, hogy a fájl más helyre mutat. Ha a parancsikonra duplán kattint, az úgy viselkedik, mintha a felhasználó duplán kattintott volna a tényleges fájlra.

Az alkalmazás-parancsikonokat tartalmazó LNK-fájlok olyan tulajdonságokkal rendelkezhetnek, amelyek befolyásolják a program futását. Az attribútumok módosításához kattintson a jobb gombbal a parancsikonfájlra, válassza a **Tulajdonságok** lehetőséget, majd módosítsa a Cél mezőt.

A fájlkiterjesztések helyett az LNK fájlok Windows Intéző kiterjesztések. Terminálkiterjesztésként az .lnk dokumentumok csak a Windows Intézőben használhatók fájl helyettesítésére, és a Windows Intézőben más célokat is szolgálnak, azon kívül, hogy parancsikonként szolgálnak egy helyi dokumentumhoz. Ezek a fájlok is "L" betűvel kezdődnek.

Míg a parancsikonok meghatározott fájlokra és könyvtárakra hivatkoznak létrehozásukkor, működésképtelenné válhatnak, ha a célt egy másik helyre módosítják. Az Explorer elkezdi javítani egy parancsikon mappát, amely megnyitásakor egy halott célpontra mutat.


## Műszaki specifikáció ##

A Windows csak akkor nem jeleníti meg az .lnk dokumentumkiterjesztést a dokumentum-parancsikonokhoz, ha a „Felismert fájltípusok kiterjesztésének elrejtése” mappamegtekintési beállítás nincs bejelölve. Bár nem ajánlott, engedélyezheti a fájlkiterjesztés megjelenítését, ha eltávolítja a "NeverShowExt" tulajdonságot a HKEY_CLASSES_ROOT\lnk fájl Windows rendszerleíró adatbázisából.

Ehhez hajtsa végre az alábbi lépéseket:

* Nyissa meg a "Regisztrációs szerkesztőt" a "Regedit" szó beírásával a tálca keresőmezőjébe, és válassza ki a programot
* Az alkalmazásban lépjen a Computer\HKEY HKEY_CLASSES_ROOT\lnkfile helyre
* Készítsen biztonsági másolatot az elemről a jobb gombbal kattintva, és válassza az Exportálás lehetőséget
* Válassza ki és törölje a "NeverShowExt" attribútumot
* A Windowst újra kell indítani


## Hivatkozási szám

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
