{
  "date": "2020-08-20",
  "keywords": [
"fon fil",
"fon filformat",
"hvad er en fon-fil",
"fil",
"fon eksempel",
"fon filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FON - Skriftbiblioteksfil",
  "description": "Lær om FON filformat og API'er, der kan oprette og åbne FON filer.",
  "linktitle": "FON",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-fo-dan"
}
},
  "lastmod": "2020-10-30"
}

## Hvad er FON fil?

En fil med filtypenavnet .fon er et Microsoft Windows 3.x-skrifttypebibliotek, der faktisk er en eksekverbar fil, men omdøbt til .fon. Det er en samling af [.fnt](/font/fnt/) filer i sig selv, og applikationer refererer til det, mens de får adgang til systemskrifttypen. Det er derfor, det fungerer som en ressourcefil. Det kan åbnes på Windows OS ved hjælp af Microsoft Windows Font View-applikationen.

## FON filformat

En FON-fil indeholder skrifttyperessourcer og har Resource (.res) filformat. .res-filformatet angiver filoverskriften samt datasektionsspecifikationer. En .fnt er også en ressourcedatafil, der er inkluderet i en ressourcefil. FON-filer har binært filformat og har application/octet-stream MIME-type.

Skrifttyperessourcer, i modsætning til andre typer ressourcer, føjes ikke til ressourcerne i en applikation. I stedet føjes de til EXE-filerne og omdøbes til .fon-filer, hvilket resulterer i biblioteksfiler i stedet for applikationer. Flere individuelle skrifttyper udgør komponenter i en skrifttypegruppe, hvor hver gruppe følger en ressourcegruppestruktur. Skrifttyperessourcer bruger disse ressourcegruppestrukturer. Gruppehovedet har alle de oplysninger, der kræves for at få adgang til en bestemt skrifttype fra gruppen. En skrifttypekomponentressource har følgende format.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/font/fnt/) file)
```
En enkelt .rc-ressourcefil kan have blandede ressourceerklæringer. Skrifttypegrupper kan være hvor som helst i ressourcefilen og behøver ikke at være sammenhængende. Det er et must for programmer, der opretter .RES-filer, at tilføje manuel indtastning af FONTDIR. Følgende er strukturen af gruppeoverskriften.

```
[Normal ressourceoverskrift (type = 7)]

WORD NumberOfFonts; // Samlet antal i .RES-fil
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
ORD dfVægt;
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
char szEnhedsnavn[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

