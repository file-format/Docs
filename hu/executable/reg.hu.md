{
  "date" : "2021-08-02",
  "keywords" :[ "reg fájl", "reg fájl formátum", "mi az a reg fájl", "fájl", "reg példa", "reg fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a REG fájlformátumról és az API-król, amelyek REG fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"REG - Windows rendszerleíró fájl",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Mi az a REG fájl?
A REG fájl egyszerűen egy szöveges fájl .reg kiterjesztéssel. Ezeket a fájlokat általában a rendszerleíró adatbázisból tipikus kulcsok exportálásával hozzák létre. Ezek a fájlok a rendszerleíró adatbázis biztonsági másolataként is használhatók (különösen ez a lépés a módosítások elvégzése előtt fontos!). Látható, hogy egyesek letölthető fájlként tették elérhetővé ugyanazokon a webhelyeken, amelyek bemutatják, hogyan kell végrehajtani a rendszerleíró adatbázis feltörését. A REG-fájl hasznos lehet a beállításjegyzék kézi módosításához és a módosítások exportálásához. Csak tisztítsa meg egy kicsit a fájlt, majd ossza meg másokkal.

## REG fájlformátum
A REG fájlformátumot a Windows rendszerleíró adatbázis részeinek exportálására és importálására tervezték INI-alapú szintaxis használatával. A Windows Registry egy relációs vagy hierarchikus adatbázis, amely megőrzi a Microsoft Windows operációs rendszer és a Windows rendszerleíró adatbázist használó egyéb alkalmazások alacsony szintű beállításait. Alternatív megoldásként azt is mondhatjuk, hogy a rendszerleíró adatbázis vagy a Windows Registry a Microsoft Windows operációs rendszerek összes verziójára telepített programok és hardverek információiból, opcióiból, beállításaiból és egyéb értékéből áll.
### A REG fájl szintaxisa
Íme néhány kulcselem a REG fájl szintaxisának részeként:
- **RegistryEditorVersion**: Pl. "Windows Registry Editor Version 5.00" Windows 2000, Windows XP és Windows Server 2003 rendszerekhez.
- **Üres sor**: Egy új beállításjegyzék-útvonal kezdetét jelzi.
- **RegistryPathx**: Az első importált értéket tartalmazó alkulcs elérési útja.
- **DataItemNamex**: Az importálni kívánt adatelem neve.
- **DataTypex**: A beállításjegyzék értékének adattípusa.

A kulcsok .reg fájlokban tárolódnak a következő szintaxis használatával:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
A kulcs alapértelmezett értékét az "Értéknév" helyett a "@" használatával módosíthatja:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Példa
Íme egy példa a REG fájlra
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## Hivatkozások

* [Windows Registry- by Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [A beállításjegyzék alkulcsainak és értékeinek hozzáadása, módosítása vagy törlése .reg fájl használatával](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)
