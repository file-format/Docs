{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az ACCDB fájlformátumról és az API-król, amelyek ACCDB fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"ACCDB fájlformátum - Microsoft Access 2007 adatbázisfájl",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Mi az ACCDB fájl?

Az .accdb kiterjesztésű fájl egy Microsoft Access 2007 adatbázisfájl, amely táblázatokban tárolja a felhasználók adatait. Támogatja a tárolást
egyéni űrlapok, SQL-lekérdezések és egyéb adatok. Az ACCDB-fájlok felváltották az [MDB](/hu/database/mdb/) fájlokat, miután a Microsoft áttért az XML-alapú fájlstruktúrára. Az ACCDB fájlok továbbra is konvertálhatók MDB-vé a régi kompatibilitás mellett. Az ACCDB azonban jelenleg a széles körben használt Access adatbázis-fájlformátum. A Microsoft további funkciókat is támogatott ACCDB formátumban, például fájlmellékletek tárolását, bináris adatokat és többértékű mező támogatást.

## ACCDB fájlformátum

Az MDB-hez hasonlóan az ACCDB fájlformátumhoz sem állnak rendelkezésre nyilvános specifikációk. A Microsoft támogatja a fájlok programozott elérését az Open Database Connectivity (ODBC) szabványon és a Visual Basic for Applications (VBA) segítségével.

### Betekintés

Egy egyszerű ACCDB fájl hexadecimális kiíratása azt sugallja, hogy általános hasonlóságok vannak a szerkezetben az előd MDB formátumcsalád legújabb verzióival. Mindkét fájlformátum fix, 4096 bájtos oldalméretet használ. Egy másik hasonlóság az ACCDB és az MDB között a mágikus szám formája, amely tartalmazza az ACCDB "Standard ACE DB" karakterláncát. A verzió vagy a kompatibilitási kód mindkét formátumban ugyanazon a helyen található. Az mdbtools | A HACKING fájl kijelenti, hogy "Offset 0x14 tartalmazza ennek az adatbázisnak a Jet verzióját", és a nem hivatalos MDB útmutató is egyetért vele. Az ezekben a forrásokban található információk a [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine) Wikipédia-bejegyzésével kombinálva arra utalnak, hogy a 0x02 érték az ACE 12-t (Access 2007), a 0x03 pedig az ACE-t jelzi. 14 (Hozzáférés 2010). Azonban az Access 2010-ben létrehozott minimális adatbázis és az Access 2016-ban létrehozott hasonló adatbázis is 0x02-t tartalmaz ezen a helyen. Az Access 2016-ban létrehozott minimális adatbázis, amely az újonnan bevezetett "nagy egész" adattípussal határoz meg egy oszlopot, 0x05 értéket kapott. Az ACCDB-fájlokban ez a jelző a fájl kompatibilitását tükrözi, nem pedig a létrehozásához használt ACE-motor verzióját.

## Hivatkozások

* [Access 2016 Specifications](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Melyik Access-fájlformátumot használjam?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
