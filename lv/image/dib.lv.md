{
  "date": "2020-01-10",
  "keywords": [
"dib fails",
"dib faila formātā",
"kas ir dib fails",
"failu",
"dib piemērs",
"dib faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DIB",
  "description": "Uzziniet par DIB faila formātu un API, kas var izveidot un atvērt DIB failus.",
  "linktitle": "DIB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-di-lvb"
}
},
  "lastmod": "2020-01-10"
}

## Kas ir DIB fails?

No ierīces neatkarīga bitkarte (DIB) ir rastra attēla fails, kas pēc struktūras ir līdzīgs standarta bitkartes failiem ([BMP]()/image/bmp/)). Tajā ir krāsu tabula, kas apraksta RGB krāsu kartēšanu ar pikseļu vērtībām. Tas ļauj DIB attēlot attēlu jebkurā ierīcē. To var atvērt ar gandrīz visām lietojumprogrammām, kas var atvērt standarta BMP failu operētājsistēmā Windows, kā arī MacOS. DIB ir bināri faili, un tiem ir sarežģīts faila formāts, kas līdzīgs BMP. DIB attēli krāsu dziļuma un pikseļu collā ziņā nav atkarīgi no renderēšanas ierīču izvades iespējām.

## DIB faila formāta specifikācijas ##
DIB satur šādu krāsu un izmēru informāciju:

  * Ierīces krāsu formāts, kurā tika izveidots taisnstūra attēls.
  * Tās ierīces izšķirtspēja, kurā tika izveidots taisnstūra attēls.
  * Ierīces palete, kurā tika izveidots attēls.
  * Bitu masīvs, kas attēlo sarkano, zaļo, zilo (RGB) tripletus ar pikseļiem taisnstūrveida attēlā.
  * Datu saspiešanas identifikators, kas norāda datu saspiešanas shēmu (ja tāda ir), ko izmanto, lai samazinātu bitu masīva lielumu.

### DIB datu bloka formāts ###

DIB tiek izmantots atmiņas bloka kontekstā, salīdzinot ar diskā saglabātajiem .DIB failiem. Atmiņas bloks sastāv no struktūras, kas atbilst Windows API specifikācijām DIB. Faktiskais DIB sastāv no:
  * Virsraksts
  * Krāsu palete
  * Pikseļu dati

Praktiski darbs ar paleti, galvenes un attēla datiem notiek tā, it kā tie būtu trīs atsevišķi atmiņas bloki. Šim izplatītajam atmiņas blokam tiek piešķirts rokturis, izmantojot GlobalAlloc, un tas ir pazīstams kā HDIB, ko izmanto, lai iegūtu galveni, krāsu tabulu un pikseļu datus un strādātu ar tiem.

### Struktūras ###
DIB ietvertā informācija ir attēlota ar dažādām struktūrām. Tie ietver:

BITMAPIinfo — definē DIB izmēru un krāsu informāciju
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Tas sastāv no BITMAPINFOHEADER:

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
kam seko divas vai vairākas RGBQAD struktūras.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Datu biti ###
|Bits|Apraksts|
---|---|
|1 bita formāts (vienkrāsains)|Melnkrāsas bitkartes sastāv no divām krāsām (melnā un baltā). Ierobežotā krāsu skaita dēļ šīs bitkartes aizņem mazāk vietas diskā. BitBitCount atgriež patiesu vai nepatiesu abu krāsu attēlojumam. Lielākā daļa lietojumprogrammu pilnībā izlaiž paleti, ja bitBitCount==1.
|4 bit format (VGA or 16 color)|Each byte of image data represents two pixels and bitBitCount==4. Šie biti attēlo pikseļa krāsu dilstošā secībā.
|8 bitu formāts (256 krāsas)|Šis 8 bitu formāts var attēlot ne vairāk kā 256 krāsas. Katrs baits attēla bitkartes datu masīvā apzīmē vienu pikseļu. Šī baita vērtība ir krāsu paletes ieraksta numurs, kas jāizmanto no 256 ierakstiem, ko attēlo bmciColors.
|24 bit format (TrueColor)|These bitmaps can have a maximum of 2^24 colors (biBitCount == 24).Each three-byte sequence in the bitmap data array represents the relative intensities of the three primary hues of a pixel. The hues are described as values ranging from 0 to 255 and are stored in the three bytes in the order Blue, Green and Red. This is an important distinction, because most references to colors in Windows use the opposite order: Red/Green/Blue, so think "BGR" when working with TrueColor images instead of "RGB". A color palette can be specified to accelerate the drawing process for Windows, in which case biClrUsed will not be 0. Bet, kā redzat, tas nav vajadzīgs, jo pikseļu dati satur informāciju par krāsu.
|32 bitu formāts|32 bitu attēliem ir ne vairāk kā 2^24 krāsas (biBitCount == 24).

## Atsauces Nr.
  * [No ierīces neatkarīgas bitkartes — Microsoft](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

