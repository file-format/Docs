{
  "date" : "2020-01-11",
  "keywords" :[ "x fájl", "x fájl formátum", "mi az x fájl", "fájl", "x példa", "x fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - DirectX 2.0 fájlformátum",
  "description":"További információ a DirectX X fájlformátumról és az API-król, amelyek képesek megnyitni és létrehozni DirectX X fájlokat.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## Mi az az X fájl?

Az .x kiterjesztésű fájl a [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics régi fájlformátumára vonatkozik, amelyet a Microsoft DirectX 2.0-val vezettek be. A játékok 3D-s grafikai megjelenítésére használták, és meghatározza a hálók, textúrák, animációk és a felhasználó által definiált objektumok struktúráit. 2014 óta elavulttá vált, mivel az Autodesk FBX fájlformátum jobban szolgál modernebb formátumként. Az X sablonvezérelt, és mentes a használati ismeretektől.

A DirectX X fájlokat Microsoft DirectX és általános szövegszerkesztők segítségével nyithatja meg.

## X Fájlformátum

Az [X fájl hivatkozás](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) hivatkozási információkat tartalmaz az API-elemekről, amelyeket dolgozni DirectX .x fájlokkal. A formátum alacsony szintű adatprimitíveket biztosít, amelyeket más alkalmazások használnak magasabb szintű primitívek meghatározására adatsablonokon keresztül. A DirectX 6.0 olyan felületeket és módszereket vezetett be, amelyek lehetővé teszik az .x fájlok olvasását és írását. A DirectX 3.0 bevezette ennek a fájlformátumnak a bináris változatát.

A DirectX 9 által meghatározott [X fájlformátum hivatkozás](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) referencia információkat tartalmaz a .x fájlhoz bináris fájlokat, valamint szövegkódolásokat.

### Bináris kódolás

A [bináris formátum](https://docs.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) a DirectX X formátumot a szövegformátum tokenizált megjelenítéseként határozza meg. Ezek a tokenek lehetnek önállóak, hogy nyelvtani szerkezetet adjanak, vagy lehetnek rekordot hordozó tokenek, amelyek biztosítják a szükséges adatokat.

#### Fejléc

A bináris fejléc a következő definíciók használatával olvasható és írható.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Szövegkódolás

A DirectX .x fájlok nem függenek a fájl felhasználási módjától, és nem specifikusak egyetlen alkalmazásra sem. Ez a sablonvezérelt megközelítés lehetővé teszi az .x fájlformátum használatát bármely ügyfélalkalmazás számára.


#### Fejléc

A változó hosszúságú fejléc kötelező, és az adatfolyam elején kell lennie. A fejléc a következő adatokat tartalmazza.

|Típus |Altípus |Méret |Tartalom |Tartalom Jelentés|
---|---|---|---|---|
|Mágikus szám (kötelező)| | 4 bájt |xof |
|Verziószám (kötelező) |Főszám |2 bájt |03 |Fő verzió 3|
| |Minor Number |2 byte |02 |Minor version 2|
|Formátum típusa (kötelező)| |4 bájt |"txt" |Szövegfájl|
| | | |"bin "| Bináris fájl|
| | | |"tzip"| MSZip tömörített szövegfájl|
| | | |"bzip"| MSZip tömörített bináris fájl|
|Úszóméret (kötelező)| |4 bájt| 0064| 64 bites lebegés|
| | | |0032 |32 bites lebegés|


## Hivatkozások

* [X Files Legacy](https://docs.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [DirectX 9 fájlformátum-referencia](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

