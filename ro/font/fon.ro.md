{
  "date" : "2020-08-20",
  "keywords" :[ "fișier fon", "format fișier fon", "ce este un fișier fon", "fișier", "exemplu fon", "extensie fișier fon", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON – fișier bibliotecă de fonturi",
  "description":"Aflați despre formatul de fișier FON și despre API-urile care pot crea și deschide fișiere FON.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Ce este un fișier FON?

Un fișier cu extensia .fon este o bibliotecă de fonturi Microsoft Windows 3.x care este de fapt un fișier executabil, dar redenumit în .fon. Este o colecție de fișiere [.fnt](/ro/font/fnt/) în sine și aplicațiile îl fac referire în timp ce accesează fontul sistemului. De aceea acționează ca un fișier de resurse. Poate fi deschis pe sistemul de operare Windows folosind aplicația Microsoft Windows Font View.

## Format de fișier FON

Un fișier FON conține resurse de font și are formatul de fișier Resurse (.res). Formatul de fișier .res specifică antetul fișierului, precum și specificațiile secțiunii de date. Un .fnt este, de asemenea, un fișier de date de resurse care este inclus cu un fișier de resurse. Fișierele FON au format de fișier binar și au tipul MIME aplicație/octet-stream.

Resursele de font, spre deosebire de alte tipuri de resurse, nu sunt adăugate resurselor unei aplicații. În schimb, acestea sunt adăugate la fișierele EXE și redenumite în fișiere .fon, rezultând fișiere de bibliotecă în loc de aplicații. Fonturile individuale multiple constituie componente ale unui grup de fonturi în care fiecare grup urmează o structură de grup de resurse. Resursele de fonturi folosesc aceste structuri de grup de resurse. Antetul grupului conține toate informațiile necesare pentru a accesa un anumit font din grup. O resursă de componentă a fonturilor are următorul format.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/ro/font/fnt/) file)
```
Un singur fișier de resurse .rc poate avea declarații de resurse mixte. Grupurile de fonturi pot fi oriunde în fișierul de resurse și nu trebuie să fie împreună. Este necesar ca programele care creează fișiere .RES să adauge introducerea manuală a FONTDIR. Mai jos este structura antetului grupului.

```
[Antet resursă normală (tip = 7)]

WORD NumberOfFonts; // Numărul total în fișierul .RES
```     
The remaining data is repeated for every font in the .RES file.

```
font WORDOrdinal;
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
WORD dfGreutate;
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

