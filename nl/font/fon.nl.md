{
  "date" : "2020-08-20",
  "keywords" :[ "fon file", "fon file format", "wat is een fon file", "file", "fon example", "fon file extension","extension", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - Lettertypebibliotheekbestand",
  "description":"Meer informatie over de FON-bestandsindeling en API's die FON-bestanden kunnen maken en openen.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Wat is een FON-bestand?

Een bestand met de extensie .fon is een lettertypebibliotheek van Microsoft Windows 3.x die eigenlijk een uitvoerbaar bestand is, maar hernoemd naar .fon. Het is een verzameling van [.fnt](/nl/font/fnt/)-bestanden op zich en toepassingen verwijzen ernaar tijdens het openen van het systeemlettertype. Daarom fungeert het als een bronbestand. Het kan worden geopend op Windows OS met behulp van de Microsoft Windows Font View-toepassing.

## FON-bestandsindeling

Een FON-bestand bevat bronnen voor lettertypen en heeft de bestandsindeling Resource (.res). Het .res-bestandsformaat specificeert zowel de bestandskop als de specificaties van de gegevenssectie. Een .fnt is ook een brongegevensbestand dat bij een bronbestand wordt gevoegd. FON-bestanden hebben een binair bestandsformaat en hebben het MIME-type application/octet-stream.

Fontbronnen worden, in tegenstelling tot andere typen bronnen, niet toegevoegd aan de bronnen van een toepassing. In plaats daarvan worden ze toegevoegd aan de EXE-bestanden en hernoemd naar .fon-bestanden, wat resulteert in bibliotheekbestanden in plaats van toepassingen. Meerdere afzonderlijke lettertypen vormen componenten van een lettertypegroep waarbij elke groep een resourcegroepstructuur volgt. Fontresources gebruiken deze resourcegroepstructuren. De groepskop bevat alle informatie die nodig is om toegang te krijgen tot een specifiek lettertype uit de groep. Een bron voor lettertypecomponenten heeft de volgende indeling.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/nl/font/fnt/) file)
```
Een enkel .rc-bronbestand kan gemengde brondeclaraties hebben. Lettertypegroepen kunnen overal in het bronbestand staan en hoeven niet aaneengesloten te zijn. Het is een must voor programma's die .RES-bestanden maken om handmatige invoer van FONTDIR toe te voegen. Hieronder volgt de structuur van de groepskop.

```
[Normale bronkop (type = 7)]

WORD NumberOfFonts; // Totaal aantal in .RES-bestand
```     
The remaining data is repeated for every font in the .RES file.

```
WORD-lettertypeOrdinaal;
struct FontDirEntry {
WORD dfVersie;
DWORD dfSize;
char dfCopyright[60];
WOORD dfType;
WORD dfPunten;
WOORD dfVertRes;
WOORD dfHorizRes;
WOORD dfAscent;
WOORD dfInternLeading;
WORD dfExternalLeading;
BYTE dfItalic;
BYTE dfOnderstrepen;
BYTE dfStrikeOut;
WOORD dfGewicht;
BYTE dfCharSet;
WOORD dfPixWidth;
WOORD dfPixHeight;
BYTE dfPitchAndFamily;
WOORD dfAvgWidth;
WOORD dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
WOORD dfWidthBytes;
DWORD dfApparaat;
DWORD dfFace;
DWORD dfGereserveerd;
char szApparaatnaam[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

