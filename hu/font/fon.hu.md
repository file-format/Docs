{
  "date" : "2020-08-20",
  "keywords" :[ "fon fájl", "fon fájlformátum", "mi az a fon fájl", "fájl", "fon példa", "fon fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - Font Library File",
  "description":"További információ a FON fájlformátumról és az API-król, amelyek FON fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Mi az a FON fájl?

A .fon kiterjesztésű fájl egy Microsoft Windows 3.x betűkészlet-könyvtár, amely valójában egy végrehajtható fájl, de átnevezték .fon-ra. Ez önmagában [.fnt](/hu/font/fnt/) fájlok gyűjteménye, és az alkalmazások hivatkoznak rá, miközben hozzáférnek a rendszer betűtípusához. Ezért működik erőforrásfájlként. Megnyitható Windows operációs rendszeren a Microsoft Windows Font View alkalmazással.

## FON Fájlformátum

A FON fájl betűkészlet-erőforrásokat tartalmaz, és erőforrás (.res) fájlformátummal rendelkezik. A .res fájlformátum határozza meg a fájl fejlécét, valamint az adatszakasz specifikációit. Az .fnt egy erőforrás-adatfájl is, amely egy erőforrásfájlhoz tartozik. A FON fájlok bináris fájlformátumúak, és alkalmazás/octet-stream MIME típusúak.

A betűtípus-erőforrások a többi erőforrástípustól eltérően nem kerülnek hozzáadásra az alkalmazások erőforrásaihoz. Ehelyett hozzáadódnak az EXE-fájlokhoz, és átnevezik őket .fon-fájlokra, így az alkalmazások helyett könyvtári fájlok jelennek meg. A több egyedi betűtípus egy betűtípuscsoport összetevőit alkotja, ahol minden csoport egy erőforráscsoport-struktúrát követ. A betűtípus-erőforrások ezeket az erőforráscsoport-struktúrákat használják. A csoportfejléc tartalmazza az összes olyan információt, amely a csoportból egy adott betűtípus eléréséhez szükséges. A betűtípus-összetevő erőforrásának formátuma a következő.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/hu/font/fnt/) file)
```
Egyetlen .rc erőforrásfájl vegyes erőforrás-deklarációkat tartalmazhat. A betűtípuscsoportok bárhol lehetnek az erőforrásfájlban, és nem kell összefüggőnek lenniük. A .RES fájlokat létrehozó programok számára kötelező a FONTDIR kézi bevitele. A következő a csoportfejléc szerkezete.

```
[Normál erőforrásfejléc (típus = 7)]

WORD NumberOfFonts; // Teljes szám a .RES fájlban
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fontOrdinal;
struct FontDirEntry {
WORD dfVersion;
DWORD dfSize;
char dfCopyright[60];
WORD dfType;
WORD dfPoints;
WORD dfVertRes;
WORD dfHorizRes;
WORD dfAscent;
WORD dfInternalLeading;
WORD dfExternalLeading;
BYTE dfItalic;
BYTE dfUnderline;
BYTE dfStrikeOut;
WORD dfWeight;
BYTE dfCharSet;
WORD dfPixWidth;
WORD dfPixHeight;
BYTE dfPitchAndFamily;
WORD dfAvgWidth;
WORD dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
WORD dfWidthBytes;
DWORD dfDevice;
DWORD dfFace;
DWORD dfReserved;
char szDeviceName[];
char szArcnév[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

