{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGZ fájl – Gzipped Tar fájl",
  "description":"Tudjon meg többet a TGZ fájlformátumról és az API-król, amelyek TGZ fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## Mi az a TGZ fájl?

A .tgz kiterjesztésű fájl egy TAR archív fájl, amely több fájlból és mappából áll, és amelyet a Gnu Zip (gzip) tömörítő szoftverrel tömörítettek. A [TAR](/hu/compression/tar/) fájl általában több fájlt egyesít egyetlen fájlba biztonsági mentés vagy az interneten történő terjesztés céljából. Ez a fájl kicsomagolása mindaddig, amíg a gzip szoftver nem tömöríti, majd TGZ fájl lesz belőle. A TGZ fájlok, mivel tömörített fájlok, kevesebb helyet foglalnak el a lemezen, és könnyen átvihetők e-mailben az interneten keresztül. Néhány alkalmazás, amely képes megnyitni a TGZ fájlokat, többek között a WinZip, az Apple Archive Utility, a 7-Zip és a WinRAR. A TGZ fájlokat többnyire UNIX és Linux rendszerekben használják.

## TGZ fájlformátum

A TGZ-fájlok tömörített bináris fájlként kerülnek mentésre a [GZ](/hu/compression/gz/) tömörítési algoritmussal.

## A .tgz fájl kicsomagolása Linux rendszeren

Linux/Unix operációs rendszeren a következő paranccsal lehet kicsomagolni a TGZ fájlokat a parancssorból.

```
tar zxvf tgzCompressedFile.tgz
```

A fenti parancs kicsomagolja a tömörített TGZ fájlt, és a TAR archívum fájljait lemezre bontja.
## Hivatkozások ##

* [TGS](https://core.telegram.org/animated_stickers)
* [gzip - Wikipédia](https://en.wikipedia.org/wiki/Gzip)

