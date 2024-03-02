{
  "date": "2020-01-10",
  "keywords": [
"comhad dib",
"formáid comhaid dib",
"cad is comhad dib ann",
"comhad",
"sampla dib",
"síneadh comhad dib",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DIB",
  "description": "Foghlaim faoi fhormáid comhaid DIB agus APIanna ar féidir leo comhaid DIB a chruthú agus a oscailt.",
  "linktitle": "DIB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-di-gab"
}
},
  "lastmod": "2020-01-10"
}

## Cad is comhad DIB ann?

Is comhad íomhá raster é léarscáil ghiotán Neamhspleách (DIB) atá cosúil le struchtúr na gcomhaid Giotán caighdeánach ([BMP]()/image/bmp/)). Tá tábla datha ann a chuireann síos ar mhapáil dathanna RGB chuig na luachanna picteilín. Cuireann sé seo ar chumas DIB íomhá a léiriú ar ghléas ar bith. Is féidir é a oscailt le beagnach gach feidhmchlár ar féidir leo comhad BMP caighdeánach a oscailt ar Windows chomh maith le macOS. Is comhaid dhénártha iad DIB agus tá formáid comhaid chasta acu cosúil le BMP. Tá íomhánna DIB neamhspleách ar chumais aschuir feistí rindreála i dtéarmaí doimhneacht datha agus picteilín in aghaidh an orlach.

## Sonraíochtaí Formáid Chomhaid DIB ##
Tá an fhaisnéis datha agus toise seo a leanas in DIB:

  * Formáid dath an fheiste ar a cruthaíodh an íomhá dronuilleogach.
  * Rún na feiste ar a cruthaíodh an íomhá dronuilleogach.
  * An pailéad don fheiste ar a cruthaíodh an íomhá.
  * Sraith giotán a mhapálann triplets dearg, glas, gorm ( RGB ) go picteilíní san íomhá dhronuilleogach.
  * Aitheantóir comhbhrú sonraí a léiríonn an scéim comhbhrú sonraí (más ann di) a úsáidtear chun méid an tsraithe giotán a laghdú.

### Formáid Bloc Sonraí DIB ###

Tagann DIB i gcomhthéacs bloc cuimhne i gcomparáid le comhaid .DIB atá stóráilte ar diosca. Cuimsíonn an bloc cuimhne struchtúr atá i gcomhréir le sonraíochtaí Windows API do DIBanna. Cuimsíonn iarbhír DIB:
  * Ceanntásc
  * Pailéad dathanna
  * Sonraí picteilíní

Go praiticiúil, déantar oibriú le sonraí pailéad, ceanntásca agus íomhá amhail is dá mba thrí bhloc cuimhne ar leith iad. Sanntar hanla don bhloc cuimhne coitianta seo trí úsáid a bhaint as GlobalAlloc agus tugtar HDIB air, a úsáidtear chun an ceanntásc, an tábla datha agus na sonraí picteilín a bhaint agus oibriú leis.

### Struchtúir ###
Léiríonn struchtúir éagsúla an fhaisnéis atá i DIB. Ina measc seo tá:

BITMAPInfo - Sainmhíníonn sé an fhaisnéis toise agus datha do DIBs
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Tá sé comhdhéanta de BITMAPINFOHEADER:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
ina dhiaidh sin dhá struchtúr RGBQAD nó níos mó.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Giotán Sonraí ###
|Giotán|Cur Síos|
---|---|
| Formáid 1 ghiotán (monacrómach)|Tá dhá dhath (dubh agus bán) ar ghiotán monacrómacha. Mar gheall ar an líon teoranta dathanna seo, glacann na bitmaps seo níos lú spáis ar dhiosca. Filleann an bitBitCount fíor nó bréagach chun an dá dhath a léiriú. Ní dhéanann an chuid is mó de na feidhmchláir an pailéad go hiomlán más rud é bitBitCount==1.
|4 bit format (VGA or 16 color)|Each byte of image data represents two pixels and bitBitCount==4. Léiríonn na giotáin seo dath na picteilíní san ord íslitheach.
| Formáid 8 giotán (256 dath)|Is féidir leis an bhformáid 8-giotán seo 256 dath ar a mhéad a léiriú. Is ionann gach beart in eagar sonraí léarscáil ghiotán na híomhá agus picteilín amháin. Is é luach an bhirt sin uimhir na hiontrála pailéad dathanna atá le húsáid as na 256 iontráil arna léiriú ag na Dathanna bmci.
|24 bit format (TrueColor)|These bitmaps can have a maximum of 2^24 colors (biBitCount == 24).Each three-byte sequence in the bitmap data array represents the relative intensities of the three primary hues of a pixel. The hues are described as values ranging from 0 to 255 and are stored in the three bytes in the order Blue, Green and Red. This is an important distinction, because most references to colors in Windows use the opposite order: Red/Green/Blue, so think "BGR" when working with TrueColor images instead of "RGB". A color palette can be specified to accelerate the drawing process for Windows, in which case biClrUsed will not be 0. Ach mar a fheiceann tú, níl sé ag teastáil, ós rud é go bhfuil an fhaisnéis dath sna sonraí picteilín féin.
|Formáid 32 giotán|Tá 2^24 dathanna ar a mhéad ag íomhánna 32 ghiotán (biBitCount == 24).

## Tagairtí ##
  * [Device-Independent Bitmaps - Le Microsoft]( https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

