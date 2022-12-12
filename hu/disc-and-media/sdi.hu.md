{
  "date" : "2021-08-13",
  "keywords" :[ "sdi fájl", "sdi fájl formátum", "mi az sdi fájl", "fájl", "sdi példa", "sdi fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"További információ az SDI fájlformátumról és az SDI-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"SDI – Windows rendszertelepítési képfájl",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## Mi az SDI fájl?
Az .sdi kiterjesztésű fájl egy betöltési blobot, rendszerindítási blobot és rész blobot tartalmaz; általában a Windows Embedded Studio használja RAM lemezek vagy rendszerindító lemezek létrehozására a Windows betöltéséhez és telepítéséhez. Az SDI a System Deployment Image rövidítése. A Windows Embedded Studio egy olyan program, amely lemezképek létrehozására szolgál Windows rendszerhez. Valójában ez a program tartalmazza az SDI fájlkezelő programot és az **sdimgr.exe** nevű parancssori eszközt, mindkettő használható SDI-képfájlok feltöltésére, létrehozására és szerkesztésére.

## SDI fájlformátum
Az SDI fájlformátumot széles körben használják virtuális lemez használatának lehetővé tételére a rendszer indításához. A Microsoft Windows egyes verziói lehetővé teszik a **RAM rendszerindítást**, ami fontos, hogy egy SDI fájlt betöltsünk a memóriába, majd elinduljunk onnan. Az SDI fájlformátum lehetővé teszi a hálózati rendszerindítást is a PXE (Preboot Execution Environment) használatával. Merevlemezes képalkotáshoz is használják.
### SDI fájlszakaszok
Maga az SDI-fájl a következő részekre osztható:
- **Boot BLOB**: Ez tartalmazza a tényleges rendszerindító programot, a STARTROM.COM. Ez hasonló a merevlemez rendszerindítási szektorához.
- **BLOB betöltése**: Ez általában NTLDR-t tartalmaz, és a rendszerindító BLOB indítja el.
- **Part BLOB**: Ez tartalmazza a tényleges rendszerindítási futásidőt; tartalmazza a boot.ini és ntdetect.com fájlokat is, amelyeknek a futási környezet gyökérkönyvtárában kell elhelyezkedniük.
- **Disk BLOB**: Ez egy lapos HDD kép, amely MBR-rel kezdődik. Indítás helyett merevlemez-képalkotásra használják. Ezenkívül csak a Disk BLOB-ok csatlakoztathatók a Microsoft segédprogramjaival.


## Hivatkozások

* [Rendszertelepítési kép – Wikipédia](https://en.wikipedia.org/wiki/System_Deployment_Image)


