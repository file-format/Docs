{
  "date": "2020-08-20",
  "keywords": [
"fon failu",
"fon faila formātā",
"kas ir fon fails",
"failu",
"labs piemērs",
"fon faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FON — fontu bibliotēkas fails",
  "description": "Uzziniet par FON faila formātu un API, kas var izveidot un atvērt FON failus.",
  "linktitle": "FON",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-fo-lvn"
}
},
  "lastmod": "2020-10-30"
}

## Kas ir FON fails?

Fails ar paplašinājumu .fon ir Microsoft Windows 3.x fontu bibliotēka, kas faktiski ir izpildāms fails, bet pārdēvēts par .fon. Tā ir [.fnt](/font/fnt/) failu kolekcija, un lietojumprogrammas atsaucas uz to, piekļūstot sistēmas fontam. Tāpēc tas darbojas kā resursu fails. To var atvērt operētājsistēmā Windows, izmantojot programmu Microsoft Windows Font View.

## FON faila formāts

FON fails satur fontu resursus, un tam ir resursu (.res) faila formāts. .res faila formāts nosaka faila galveni, kā arī datu sadaļas specifikācijas. .fnt ir arī resursu datu fails, kas ir iekļauts resursa failā. FON failiem ir binārais faila formāts, un tiem ir lietojumprogrammas/okteta straumes MIME tips.

Fontu resursi, atšķirībā no cita veida resursiem, netiek pievienoti lietojumprogrammas resursiem. Tā vietā tie tiek pievienoti EXE failiem un pārdēvēti par .fon failiem, kā rezultātā lietojumprogrammu vietā tiek izveidoti bibliotēkas faili. Vairāki atsevišķi fonti veido fontu grupas sastāvdaļas, kur katra grupa seko resursu grupas struktūrai. Fontu resursi izmanto šīs resursu grupu struktūras. Grupas galvenē ir visa informācija, kas nepieciešama, lai piekļūtu konkrētam fontam no grupas. Fonta komponenta resursam ir šāds formāts.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/font/fnt/) file)
```
Vienam .rc resursu failam var būt jauktas resursu deklarācijas. Fontu grupas var atrasties jebkur resursu failā, un tām nav jābūt blakus. Programmām, kas veido .RES failus, ir jāpievieno manuāla FONTDIR ievade. Tālāk ir norādīta grupas galvenes struktūra.

```
[Parasta resursa galvene (tips = 7)]

WORD NumberOfFonts; // Kopējais skaits .RES failā
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fontsOrdinal;
struct FontDirEntry {
WORD dfVersion;
DWORD dfSize;
char dfCopyright[60];
WORD dfType;
WORD dfPoints;
VĀRDS dfVertRes;
VĀRDS dfHorizRes;
VĀRDS dfAscent;
WORD dfInternalLeading;
WORD dfExternalLeading;
BAITS dfItalic;
BYTE dfUnderline;
BYTE dfStrikeOut;
VĀRDS dfSvars;
BYTE dfCharSet;
WORD dfPixWidth;
WORD dfPixHeight;
BAITS dfPitchAndFamily;
WORD dfAvgWidth;
VĀRDS dfMaxWidth;
BAITS dfFirstChar;
BAITS dfLastChar;
BAITS dfDefaultChar;
BAITS dfBreakChar;
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

