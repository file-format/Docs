{
  "date": "2020-08-20",
  "keywords": [
"fon failą",
"fon failo formatas",
"kas yra fon failas",
"failą",
"fon pavyzdys",
"fon failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FON – šriftų bibliotekos failas",
  "description": "Sužinokite apie FON failo formatą ir API, kurios gali kurti ir atidaryti FON failus.",
  "linktitle": "FON",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-fo-ltn"
}
},
  "lastmod": "2020-10-30"
}

## Kas yra FON failas?

Failas su plėtiniu .fon yra Microsoft Windows 3.x šriftų biblioteka, kuri iš tikrųjų yra vykdomasis failas, bet pervadintas į .fon. Tai yra [.fnt](/font/fnt/) failų rinkinys, o programos nurodo jį, kai pasiekia sistemos šriftą. Štai kodėl jis veikia kaip išteklių failas. Jį galima atidaryti Windows OS naudojant Microsoft Windows Font View programą.

## FON failo formatas

FON faile yra šrifto išteklių ir jis turi išteklių (.res) failo formatą. .res failo formatas nurodo failo antraštę ir duomenų skyriaus specifikacijas. .fnt taip pat yra išteklių duomenų failas, įtrauktas į išteklių failą. FON failai turi dvejetainį failo formatą ir turi programos / okteto srauto MIME tipą.

Šrifto ištekliai, skirtingai nei kitų tipų ištekliai, nėra pridedami prie programos išteklių. Vietoj to jie pridedami prie EXE failų ir pervadinami į .fon failus, todėl vietoj programų atsiranda bibliotekos failai. Keli atskiri šriftai sudaro šriftų grupės komponentus, kur kiekviena grupė atitinka išteklių grupės struktūrą. Šrifto ištekliai naudoja šias išteklių grupių struktūras. Grupės antraštėje yra visa informacija, reikalinga norint pasiekti konkretų šriftą iš grupės. Šrifto komponento išteklių formatas yra toks.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/font/fnt/) file)
```
Viename .rc išteklių faile gali būti mišrių išteklių deklaracijų. Šriftų grupės gali būti bet kurioje išteklių failo vietoje ir neturi būti gretimos. Programoms, kuriančioms .RES failus, būtina rankiniu būdu įvesti FONTDIR. Toliau pateikiama grupės antraštės struktūra.

```
[Įprasta išteklių antraštė (tipas = 7)]

WORD NumberOfFonts; // Bendras skaičius .RES faile
```     
The remaining data is repeated for every font in the .RES file.

```
WORD šriftasOrdinal;
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
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

