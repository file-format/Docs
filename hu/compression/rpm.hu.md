{
  "date" : "2021-04-08",
  "keywords" :[ "rpm fájl", "rpm fájlformátum", "mi az rpm fájl", "fájl", "rpm példa", "rpm fájlkiterjesztés", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM – Red Hat csomagkezelő fájl",
  "description":"További információ az RPM-fájlformátumról és az RPM-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Mi az RPM fájl?

Az .rpm kiterjesztésű fájl egy Red Hat Linux operációs rendszercsomag, amely programok Linux rendszerekre történő telepítéséhez használható. A Red Hat Package Manager az RPM fájlformátumot használja, és ingyenes és nyílt forráskódú csomagkezelő rendszer. Bár az RPM fájlok a programok telepítéséhez használhatók, ezek más csomagformátumokká konvertálhatók, például [DEB](/hu/compression/deb/) az Alien nevű Debian programmal.

## RPM fájlformátum

Az RPM-fájl egy bináris fájl, amely fájlkészletet tartalmazhat. Az RPM fájlok legtöbbször "bináris RPM-ek", amelyek a szoftver lefordított végrehajtható fájljai. Az RPM-fájl tartalmazhat forrás-RPM-eket (SRPM-eket), amelyek felhasználhatók a csomag forráskódból való összeállítására. Az RPM fájlformátum négy részből áll.

* Lead – RPM-fájlként azonosítja a fájlt
* Aláírás – Az integritás és/vagy hitelesség biztosítására használható
* Fejléc – Metaadatokat tartalmaz, beleértve a csomag nevét, verzióját, architektúráját, fájllistáját stb.
* Fájlarchívum – más néven hasznos adat, amely általában cpio formátumú, [GZIP]-vel tömörítve (/hu/compression/gz/)

## Hivatkozások

* [RPM – Wikipédia](https://rpm.org)
* [RPM-dokumentáció](https://rpm.org/documentation.html)

