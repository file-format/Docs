{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC – TrueType gyűjteményfájl formátum",
  "description":"A TrueType Collection (TTC) fájl több betűtípust egyesít egyetlen fájlba. Mind az Apple, mind a Microsoft TTF-et használt Mac és Windows operációs rendszereken.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Mi az a TTC fájl?
A TTC rövidítése TrueType Collection a True Type formátum kiterjesztése. Egy TTC-fájl egyesítheti a több fontfájlt. Ezek a fájlok előnyösek több, sok közös karakterjelet használó betűtípus kombinálásához. A Windows 2000 előtt a TTC-fájlokat a Windows kínai, japán és koreai verziói használták, de később a támogatás minden régióban elérhető volt.


## A betűtípusgyűjtemény-fájl szerkezete
A TTC-fájl egy TTC-fejléc táblából, táblakönyvtárakból és több OpenType-táblából áll. A TTC fejlécnek a fájl elején kell lennie. Minden fonthoz léteznie kell egy teljes táblázatkönyvtárnak. A TableDirectory formátumának hasonlónak kell lennie a nem gyűjtőfájlban létezőhöz. A TTC-fájlon belüli összes könyvtárban található táblázatok számának kiszámítása a TTC-fájl elejétől kezdődik.
A TTC-fájlban lévő táblázatokra a megfelelő betűtípusok táblázatkönyvtárában hivatkozunk. Néhány OpenType-táblázatnak többször is meg kell jelennie, egyszer a TTC-ben hozzáadott minden betűtípushoz. Míg a többi táblázatot több betűtípus is megoszthatja a TTC-fájlban.

### TTC fejléc
A TTC fejléctáblázatnak eddig két változata érhető el:
- Az 1.0-s verzió a digitális aláírás nélküli TTC-fájlokhoz használatos.
- A 2.0-s verzió használható TTC-fájlokhoz digitális aláírással vagy anélkül.
Íme mindkét verzió TTC fejléctáblázata:

**TTC fejléc 1.0-s verziója:**

|Típus|Név|Leírás|
---|---|---|
|TAG|ttcTag|Betűkészlet-azonosító karakterlánc: 'ttcf' (CFF- vagy CFF2-körvonalú, valamint TrueType-körvonalú betűtípusokhoz használatos)|
|uint16|majorVersion|A TTC fejléc fő verziója, = 1.|
|uint16|minorVersion|A TTC fejléc kisebb verziója, = 0.|
|uint32|numFonts|Betűtípusok száma a TTC-ben|
|Offset32|tableDirectoryOffsets[numFonts]|Eltolások tömbje a TableDirectoryhoz minden betűtípushoz a fájl elejétől kezdve|

**TTC fejléc 2.0-s verziója:**

|Típus|Név|Leírás|
---|---|---|
|TAG|ttcTag |Betűkészlet-azonosító karakterlánc: 'ttcf'|
|uint16| majorVersion |A TTC fejléc fő verziója, = 2.|
|uint16| minorVersion |A TTC fejléc kisebb változata, = 0.|
|uint32| numFonts |Betűtípusok száma a TTC-ben|
|Eltolás32| tableDirectoryOffsets[numFonts] |A TableDirectory eltolásainak tömbje minden betűtípushoz a fájl elejétől kezdve|
|uint32| dsigTag | DSIG-tábla létezését jelző címke, 0x44534947 ('DSIG') (null, ha nincs aláírás)|
|uint32| dsigLength |A DSIG tábla hossza (byte-ban) (null, ha nincs aláírás)|
|uint32| dsigOffset |A DSIG tábla eltolása (bájtban) a TTC fájl elejétől (null, ha nincs aláírás)|

## Hivatkozások
* [Az OpenType betűtípusfájl](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

