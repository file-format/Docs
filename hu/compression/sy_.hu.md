{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SY_ fájlformátum - tömörített SYS fájl",
  "description":"További információ a SY_ fájlformátumról és az API-król, amelyek SY_ fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Mi az a SY_ fájl?

A SY_ fájl egy tömörített .sys fájl, amelyet a szoftvertelepítők a telepítőbe csomagolt telepítőfájlok méretének csökkentésére használnak. Ez csökkenti a telepítő teljes méretét. Az SY_ fájlok a Microsoft Expand parancssori segédprogrammal bővíthetők, amely egy vagy több tömörített fájlt is kibont.

## SY_ Fájlformátum - További információ

A SY_ fájlok tömörített bináris fájlként kerülnek a lemezre. Belső fájlformátumuk azonban nem elérhető nyilvánosan. A Microsoft Expand parancssori segédprogram a következő parancssorok valamelyikével bővítheti ki az SY_ fájlokat.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Kibontáskor a SY_ fájlok [SYS](https://docs.fileformat.com/system/sys/) fájllá alakulnak.

A SY_ fájlok hasonlóak az EX_ és DL_ fájlokhoz.

## Hivatkozások

* [StuffIt – a Wikipédia által](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

