{
  "date" : "2022-02-17",
  "keywords" :["gpg fájl", "gpg fájlformátum", "mi az a gpg fájl", "fájl", "gpg példa", "gpg fájl kiterjesztése", "kiterjesztés", "formátum"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPG fájl – GNU Privacy Guard nyilvános kulcstartó fájl",
  "description":"További információ a GPG-fájlokról és az API-król, amelyek GPG-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## Mi az a GPG fájl?

A GPG fájl egy titkosítási/dekódolási kulcsfájl, amelyet a GNU Privacy Guard (GnuPG) titkosító program használ. Maga a GnuPC program az RFC4880 definíció szerinti OpenPGP szabványon alapul, és PGP néven is ismert. A GPG modern operációs rendszerben való sikeres használatának kulcsa a sokoldalú kulcskezelő rendszer. A GPG parancssori segédprogramja lehetővé teszi, hogy könnyen integrálható legyen más alkalmazásokkal.

## GPG fájl formátum

A GPG fájlok titkosított bináris fájlokként kerülnek mentésre, és természetesen nem olvashatók. A titkosított GPG-fájl visszafejtéséhez ugyanazt a biztonsági kulcsot kell használnia. És ezért ezeknek a fájloknak a belső fájlformátuma nem ismert.

## Fájlok titkosítása és visszafejtése GPG-vel Linuxon

A GPG parancssori segédprogram használható fájlok titkosítására és visszafejtésére Linuxon.

### Fájl titkosítása

Egy fájl titkosítható a gpg paranccsal a -c (create) kapcsolóval, az alábbiak szerint.

```
gpg -c file1.txt
```
A parancs futtatása egy kulcskifejezést kér, amellyel az eredeti `file1.txt` fájl tartalmát titkosíthatja. Ez a fájl1.txt.gpg titkosított fájl létrehozását eredményezi.

### Fájl visszafejtése és kibontása

A titkosított fájl visszafejtéséhez és kibontásához a következő parancs használható.

```
gpg cfile.txt.gpg
```

## Hivatkozások

* [GNUPG](https://gnupg.org/)
* [HDF – Wikipédia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

