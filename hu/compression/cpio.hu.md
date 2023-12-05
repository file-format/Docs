{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPIO fájl - Unix CPIO archív fájlformátum",
  "description":"Tanulja meg, hogy mi az a CPIO-fájl és az API-k, amelyek CPIO-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Mi az a CPIO fájl?

A CPIO fájl egy archív fájl, amelyet a Unix Copy In Copy Out (CPIO) formátumában hoztak létre. Hasonló a TAR fájlformátumhoz, kivéve, hogy tömörítetlen. A CPIO-fájlok eszközfájlokat, szimbolikus hivatkozásokat és kiterjesztett fájlattribútumokat tárolhatnak.

## CPIO fájlformátum

A CPIO archívum bináris fájlként jön létre, amely ember által nem olvasható. Fájlok és könyvtárak gyűjteményét tárolja. A CPIO archívum tartalmát metaadat-információk, például fájlnevek, engedélyek, tulajdonjog és időbélyegek azonosítják. Ezeket a metaadat-információkat az archív fájlban is tárolja a rendszer oldalsó hozzáférése érdekében.

## A CPIO archívum formátuma

A CPIO-fájl egy vagy több összefűzött tagfájlból áll. Az archívumban lévő minden fájl egy fejlécből áll, amelyet opcionálisan követ a fejlécben említett fájltartalom. Az archívum egy másik fejlécet tartalmaz a végén, amelyet egy TRAILER!! nevű üres fájl ír le.

### A CPIO-archívumok típusai

A CPIO archívumoknak két típusa van. Ezek csak a fejléc stílusában különböznek.

* ASCII archívumok – Ezek a CPIO archívumok nyomtatható fejléccel rendelkeznek, amely a CPIO archívum részévé válik, ha maga az archívum ASCII fájlokból áll
* Bináris archívumok – Ezek a CPIO archívumok bináris fejlécekkel rendelkeznek.

## A CPIO Archívum használata

### Hogyan készítsünk CPIO archívumot?

Unix-szerű rendszereken a **cpio** paranccsal hozhat létre CPIO-t. A következő parancs megkeresi az összes fájlt és könyvtárat az aktuális könyvtárban és annak alkönyvtáraiban. Ezt a kimenetet ezután a cpio parancshoz továbbítják, amely egy új CPIO archívumot generál archive.cpio néven.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Hogyan lehet fájlokat kivonni a CPIO archívumból?

A következő parancs kicsomagolja a fájlokat egy meglévő archívumból.

```
cpio -id < archive_cpio.cpio
```
Beolvassa az archive.cpio fájlt a szabványos bemenetről, és kibontja a fájlokat az aktuális könyvtárba.


## Hivatkozások

* [CPIO – a Wikipedia által](https://en.wikipedia.org/wiki/Cpio)
* [CPIO-fájlformátum](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

