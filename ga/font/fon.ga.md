{
  "date": "2020-08-20",
  "keywords": [
"fonchomhad",
"formáid comhaid fon",
"cad is fonchomhad ann",
"comhad",
"shampla fon",
"síneadh comhad fon",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FON - Comhad Leabharlainne Cló",
  "description": "Foghlaim faoi fhormáid comhaid FON agus APIanna ar féidir leo comhaid FON a chruthú agus a oscailt.",
  "linktitle": "FON",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-fo-gan"
}
},
  "lastmod": "2020-10-30"
}

## Cad is comhad FON ann?

Is éard atá i gcomhad le síneadh .fon ná leabharlann cló Microsoft Windows 3.x ar comhad inrite é i ndáiríre ach a athainmnítear go .fon. Is bailiúchán de [.fnt](/font/fnt/) comhad ann féin é agus déanann feidhmchláir tagairt dó agus cló an chórais á rochtain. Sin é an fáth go bhfeidhmíonn sé mar chomhad acmhainne. Is féidir é a oscailt ar Windows OS ag baint úsáide as feidhmchlár Microsoft Windows Font View.

## Formáid Chomhaid FON

Tá acmhainní cló i gcomhad FON agus tá formáid comhaid Resource (.res). Sonraíonn formáid comhaid .res an ceanntásc comhaid chomh maith le sonraíochtaí na rannóige sonraí. Is comhad sonraí acmhainne é .fnt freisin a chuimsítear le comhad acmhainne. Tá formáid dhénártha comhaid ag comhaid FON agus tá cineál MIME application/octet-stream acu.

Ní chuirtear acmhainní cló, murab ionann agus cineálacha eile acmhainní, le hacmhainní feidhmchláir. Ina ionad sin cuirtear leis na comhaid EXE iad agus athainmnítear iad go comhaid .fon, agus mar thoradh air sin cuirtear comhaid leabharlainne in ionad feidhmchláir. Comhpháirteanna de ghrúpa clónna is ea clónna aonair iolracha ina leanann gach grúpa struchtúr grúpa acmhainne. Úsáideann acmhainní cló na struchtúir ghrúpa acmhainní seo. Tá an fhaisnéis go léir ag ceanntásc an ghrúpa chun cló ar leith a rochtain ón ngrúpa. Tá an fhormáid seo a leanas ag acmhainn comhpháirte cló.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/font/fnt/) file)
```
Féadfaidh dearbhuithe acmhainní measctha a bheith i gcomhad acmhainne .rc amháin. Is féidir le grúpaí cló a bheith áit ar bith sa chomhad acmhainne agus ní gá dóibh a bheith tadhlach. Ní mór do chláir a chruthaíonn comhaid .RES iontráil láimhe FONTDIR a chur leis. Seo a leanas an struchtúr ceanntásc grúpa.

```
[Gnáthcheannteideal acmhainne (cineál = 7)]

WORD NumberOfFonts; // Líon iomlán i gcomhad .RES
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fontOrdinal;
struct FontDirEntry {
dfVersion WORD;
DWORD dfSize;
char dfCóipcheart[60];
Cineál dfType WORD;
dfPoints WORD;
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

