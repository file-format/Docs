{
  "date" : "2021-04-08",
  "keywords" :[ "deb fájl", "deb fájl formátum", "mi az a deb fájl", "fájl", "deb példa", "deb fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB – Bzip tömörített tar archívum",
  "description":"További információ a DEB fájlformátumról és az API-król, amelyek DEB fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Mi az a DEB fájl?

A .deb kiterjesztésű fájl egy Debian bináris csomagfájlformátum, amely szoftvercsomagok Linux operációs rendszeren való terjesztéséhez érhető el. Két [TAR](/hu/compression/tar/) archív fájlból áll. A DPKG biztosítja a DEB-csomagok olvasásának és telepítésének mechanizmusát. A DEB csomagok az APT csomagszoftver-kezelő felület segítségével telepíthetők. A DEB fájlok internetes médiatípusa `application/vnd.debian.binary-package`.

## DEB fájl formátum

Egy DEB fájl két [TAR](/hu/compression/tar/) archív fájlból áll. Az egyik archívum a vezérlő információkat, a másik pedig a telepíthető adatokat tartalmazza.

### Csomagszervezés

A DEB fájl egy **ar** archív fájl, amelynek varázsértéke `!<arch> `. A Debian 0.93 óta a DEB fájlok archiválási mechanizmusa három fájlt tartalmaz meghatározott sorrendben.

1. `Debian Binary` - Egy sor sorra van szánva, újsorokkal elválasztva. Jelenleg csak egyetlen sor található, amely leírja a verziószámot. A jelenlegi verziószám 2.0.
1. "Vezérlőarchívum" - Tartalmaz egy control.tar archívumot, amely karbantartói szkriptekkel és metainformációkkal rendelkezik a csomagról, például csomagnév, verzió, függőségek és karbantartó.
1. `Adatarchívum` – Ez egy data.tar nevű tar archívum, amely a ténylegesen telepíthető médiafájlokat tartalmazza. Az archívum tömöríthető gz-vel, bz2-vel, lzma-val vagy xz-vel, és ennek megfelelően változik az adatarchívum fájlkiterjesztése.

### Vezérlőarchívum

A vezérlő archívum a következő tartalmat tartalmazhatja.

* `control` – A csomag rövid leírását, valamint egyéb információkat, például a függőségeit tartalmazza.
* `md5sums` - A csomagban lévő összes fájl MD5 ellenőrző összegét tartalmazza a sérült vagy hiányos fájlok észlelése érdekében.
* `conffiles` - Felsorolja a csomag azon fájljait, amelyeket konfigurációs fájlként kell kezelni. A konfigurációs fájlok nem íródnak felül a frissítés során, hacsak nincs megadva.
* `preinst`, postinst, prerm és postrm - Opcionális szkriptek, amelyek a csomag telepítése vagy eltávolítása előtt vagy után futnak le
* A `config` egy opcionális szkript, amely támogatja a debconf konfigurációs mechanizmust.
* `shlibs` - Ez a megosztott könyvtári függőségek listája.

## Hivatkozások

* [DEB – Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Debian bináris csomagformátum](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

