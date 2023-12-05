{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH2 fájl – iOS SHSH Blob fájlformátum",
  "description":"További információ arról, hogy mi az SHSH2 fájl.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Mi az SHSH2 fájl?

Az SHSH2 fájl, más néven SHSH blob vagy ECID SHSH, egy digitális aláírás, amelyet az Apple használ az iOS-eszközök (például iPhone, iPad és iPod) firmware-frissítéseinek hitelesítésére és ellenőrzésére. Az eszköz egyedi azonosítóját tartalmazza, amely ECID (Exclusive Chip ID) néven ismert. Ezenkívül információkat tartalmaz az eszközre telepített firmware verziójáról.

## SHSH2 fájlformátum – További információ

Az SHSH2 fájlok bináris fájlformátumban kerülnek a lemezre, és ennek a fájlformátumnak a belső fájlszerkezetének részletei nem érhetők el nyilvánosan.

Amikor az iOS új verzióját telepítik egy Apple-eszközre, például iPhone-ra, iPadre vagy Mac-re, egy SHSH2-fájl jön létre. Ezt az SHSH2 fájlt elküldi az Apple szervereinek, amelyek beolvassák és ellenőrzik ezt a digitális aláírási fájlt. Ezen információk alapján a szerver engedélyezi vagy megakadályozza a telepítést.

Ugyanez történik, amikor frissítést kérnek. Amikor egy felhasználó az iTunes-on vagy más szoftveren keresztül kéri eszköze frissítését vagy visszaállítását, az Apple szerverei a frissítés folytatása előtt ellenőrzik, hogy az SHSH2-fájl megegyezik-e az eszköz ECID- és firmware-verziójával.

## Hivatkozások

* [SHSH Blob – a Wikipedia által](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Saver](https://tsssaver.1conan.com/v2/)

