{
  "date": "2020-01-11",
  "keywords": [
"x fails",
"x faila formātā",
"kas ir x fails",
"failu",
"x piemērs",
"x faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "X — DirectX 2.0 faila formāts",
  "description": "Uzziniet par DirectX X failu formātu un API, kas var atvērt un izveidot DirectX X failus.",
  "linktitle": "X",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d--lvx"
}
},
  "lastmod": "2020-01-11"
}

## Kas ir X fails?

A file with .x extension refers to [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics legacy file format that was introduced with Microsoft DirectX 2.0. To izmantoja 3D grafikas renderēšanai spēlēs, un tajā ir norādītas režģu, faktūru, animāciju un lietotāja definētu objektu struktūras. Kopš 2014. gada tas ir novecojis, jo Autodesk FBX faila formāts labāk kalpo kā modernāks formāts. X ir balstīta uz veidnēm, un tajā nav nekādu lietošanas zināšanu.

Varat atvērt DirectX X failus, izmantojot Microsoft DirectX un parastos teksta redaktorus.

## X faila formāts

[X file reference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) satur atsauces informāciju par API elementiem, kas tiek izmantoti darbam ar DirectX .x failiem. Formāts nodrošina zema līmeņa datu primitīvus, ko izmanto citas lietojumprogrammas, lai definētu augstāka līmeņa primitīvus, izmantojot datu veidnes. DirectX 6.0 ieviesa saskarnes un metodes, kas ļauj lasīt un rakstīt no .x failiem. DirectX 3.0 ieviesa šī faila formāta bināro versiju.

DirectX 9 definētā [X file format reference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) satur atsauces informāciju par .x failiem binārajā formātā, kā arī teksta kodējumos.

### Binārā kodēšana

[binary format](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) definē DirectX X formātu kā teksta formāta marķierizētu attēlojumu. Šie marķieri var būt atsevišķi, lai nodrošinātu gramatisko struktūru, vai arī var būt ierakstu marķieri, kas nodrošina nepieciešamos datus.

#### Galvene

Bināro galveni var lasīt un rakstīt, izmantojot šādas definīcijas.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Teksta kodēšana

DirectX .x faili nav atkarīgi no veida, kā tie tiek izmantoti, un tie nav specifiski nevienai lietojumprogrammai. Šī uz veidni balstītā pieeja ļauj .x faila formātu izmantot jebkura klienta lietojumprogramma.


#### Galvene

Mainīga garuma galvene ir obligāta, un tai ir jāatrodas datu straumes sākumā. Galvenē ir šādi dati.

|Veids |Apakštips |Izmērs |Saturs |Satura nozīme|
---|---|---|---|---|
|Maģiskais numurs (nepieciešams)| | 4 baiti |xof |
|Versijas numurs (nepieciešams) |Galvenais numurs |2 baiti |03 |Galvenā versija 3|
| |Mazais numurs |2 baiti |02 |Neliela versija 2|
|Formāta veids (obligāts)| |4 baiti |txt |Teksta fails|
| | | |bin | Binārais fails|
| | | |tzip| MSZip saspiesta teksta fails|
| | | |bzip| MSZip saspiests binārais fails|
|Pludiņa izmērs (obligāts)| |4 baiti| 0064| 64 bitu pludiņi|
| | | |0032 |32 bitu pludiņi|


## Atsauces

 * [X Files Legacy](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
 * [DirectX 9 faila formāta uzziņa](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

