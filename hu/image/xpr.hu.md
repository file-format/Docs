{
  "date" : "2022-03-21",
  "keywords" :[ "xpr fájl", "xpr fájlformátum", "mi az xpr fájl", "fájl", "xpr példa", "xpr fájlkiterjesztés", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPR fájlformátum - Microsoft Expression Design grafikus fájl",
  "description":"További információ az XPR fájlformátumról és az XPR-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "XPR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-21"
}

## Mi az XPR fájl?

Az XPR-fájl egy vektorképfájl, amelyet a már megszűnt Microsoft Expression Graphics (EGD) szoftverrel hoztak létre. Grafikus információkat tartalmaz, amelyek felhasználói felület makettjeként használhatók. Az XPR fájlokat később .design fájlok váltották fel a Microsoft Expression Design programban. Az XPR fájlok megnyithatók a Microsoft Expression Studio segítségével, amely már jó ideje megszűnt.

## XPR fájlformátum biztonsági rése

Az XPR-fájlokról megállapították, hogy a Microsoft Expression Design biztonsági résének javát szolgálják, ami távoli kódfuttatást tesz lehetővé. A jelentett probléma esetén, ha a felhasználó megnyitott egy legitim .xpr fájlt, amely a hálózati könyvtárban található a dinamikus hivatkozási könyvtár (DLL) fájllal együtt, a Microsoft Expression Design megpróbálhatja betölteni a DLL fájlt, és végrehajtani a benne lévő kódot. Ezt később a Microsoft egy biztonsági frissítésben javította.

## Hivatkozások

* [A kifejezéstervezés biztonsági rése távoli kódfuttatást tehet lehetővé (2651018)](https://docs.microsoft.com/en-us/security-updates/securitybulletins/2012/ms12-022)

