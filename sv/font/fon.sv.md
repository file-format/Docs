{
  "date" : "2020-08-20",
  "keywords" :[ "fon-fil", "fon-filformat", "vad är en fon-fil", "fil", "fon-exempel", "fon-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - Font Library File",
  "description":"Läs mer om FON-filformat och API:er som kan skapa och öppna FON-filer.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Vad är FON fil?

En fil med filtillägget .fon är ett Microsoft Windows 3.x-teckensnittsbibliotek som egentligen är en körbar fil men som har bytt namn till .fon. Det är en samling av [.fnt](/sv/font/fnt/)-filer i sig och applikationer hänvisar till den när de kommer åt systemteckensnitt. Det är därför den fungerar som en resursfil. Den kan öppnas på Windows OS med Microsoft Windows Font View-applikation.

## FON filformat

En FON-fil innehåller teckensnittsresurser och har resursfilformat (.res). .res-filformatet anger filhuvudet samt datasektionsspecifikationer. En .fnt är också en resursdatafil som ingår i en resursfil. FON-filer har binärt filformat och har applikation/oktettströms MIME-typ.

Teckensnittsresurser, till skillnad från andra typer av resurser, läggs inte till resurserna i ett program. Istället läggs de till i EXE-filerna och döps om till .fon-filer, vilket resulterar i biblioteksfiler istället för applikationer. Flera individuella teckensnitt utgör komponenter i en teckensnittsgrupp där varje grupp följer en resursgruppstruktur. Teckensnittsresurser använder dessa resursgruppstrukturer. Grupphuvudet har all information som krävs för att komma åt ett specifikt teckensnitt från gruppen. En teckensnittskomponentresurs har följande format.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/sv/font/fnt/) file)
```
En enskild .rc-resursfil kan ha blandade resursdeklarationer. Teckensnittsgrupper kan finnas var som helst i resursfilen och behöver inte vara sammanhängande. Det är ett måste för program som skapar .RES-filer att lägga till manuell inmatning av FONTDIR. Följande är strukturen för grupphuvudet.

```
[Normal resursrubrik (typ = 7)]

WORD NumberOfFonts; // Totalt antal i .RES-filen
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
ORD dfWeight;
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
char szEnhetsnamn[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

