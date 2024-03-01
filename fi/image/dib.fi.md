{
  "date": "2020-01-10",
  "keywords": [
"dib-tiedosto",
"dib-tiedostomuoto",
"mikä on dib-tiedosto",
"tiedosto",
"dib esimerkki",
"dib tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DIB",
  "description": "Opi DIB-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DIB-tiedostoja.",
  "linktitle": "DIB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-di-fib"
}
},
  "lastmod": "2020-01-10"
}

## Mikä on DIB-tiedosto?

Laitteesta riippumaton bittikartta (DIB) on rasterikuvatiedosto, joka on rakenteeltaan samanlainen kuin tavalliset bittikarttatiedostot ([BMP]()/image/bmp/)). Se sisältää väritaulukon, joka kuvaa RGB-värien yhdistämisen pikseliarvoihin. Näin DIB voi edustaa kuvaa missä tahansa laitteessa. Se voidaan avata melkein kaikilla sovelluksilla, jotka voivat avata tavallisen BMP-tiedoston Windowsissa sekä macOS:ssä. DIB ovat binääritiedostoja ja niillä on monimutkainen tiedostomuoto, joka muistuttaa BMP:tä. DIB-kuvat ovat riippumattomia renderöintilaitteiden tulostusominaisuuksista värisyvyyden ja pikselin tuuman suhteen.

## DIB-tiedostomuodon tekniset tiedot ##
DIB sisältää seuraavat väri- ja mittatiedot:

  * Sen laitteen värimuoto, jolla suorakaiteen muotoinen kuva luotiin.
  * Sen laitteen resoluutio, jolla suorakaiteen muotoinen kuva luotiin.
  * Sen laitteen paletti, jolla kuva luotiin.
  * Joukko bittejä, jotka yhdistävät punaiset, vihreät, siniset ( RGB ) -triplet pikseleiksi suorakaiteen muotoisessa kuvassa.
  * Tietojen pakkaustunniste, joka ilmaisee datan pakkausmenetelmän (jos sellainen on), jota käytetään pienentämään bittijoukon kokoa.

### DIB-tietolohkomuoto ###

DIB tulee muistilohkon yhteydessä levylle tallennettuihin .DIB-tiedostoihin verrattuna. Muistilohko koostuu rakenteesta, joka on DIB:iden Windows API -spesifikaatioiden mukainen. Todellinen DIB koostuu:
  * Otsikko
  * Väripaletti
  * Pikselitiedot

Käytännössä paletti-, otsikko- ja kuvadatan kanssa työskentely tapahtuu ikään kuin ne olisivat kolme erillistä muistilohkoa. Tälle yleiselle muistilohkolle osoitetaan kahva GlobalAllocilla, ja se tunnetaan nimellä HDIB, jota käytetään otsikon, väritaulukon ja pikselitietojen poimimiseen ja käsittelemiseen.

### Rakenteet ###
DIB:n sisältämät tiedot esitetään erilaisilla rakenteilla. Nämä sisältävät:

BITMAPIinfo - Määrittää DIB:n mitta- ja väritiedot
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Se koostuu BITMAPINFOHEADER:stä:

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
jota seuraa kaksi tai useampi RGBQAD-rakenne.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Databitit ###
|Bits|Kuvaus|
---|---|
|1-bittinen muoto (yksivärinen)|Mustavalkoiset bittikartat koostuvat kahdesta väristä (musta ja valkoinen). Tämän rajallisen värimäärän vuoksi nämä bittikartat vievät vähemmän tilaa levyllä. BitBitCount palauttaa tosi tai epätosi molempien värien esittämiseksi. Useimmat sovellukset ohittavat paletin kokonaan, jos bitBitCount==1.
|4 bit format (VGA or 16 color)|Each byte of image data represents two pixels and bitBitCount==4. Nämä bitit edustavat pikselin väriä laskevassa järjestyksessä.
|8-bittinen muoto (256 väriä)|Tämä 8-bittinen muoto voi edustaa enintään 256 väriä. Kukin tavu kuvan bittikarttatietotaulukossa edustaa yhtä pikseliä. Tämän tavun arvo on käytettävän väripalettimerkinnän numero 256 merkinnästä bmciColorsin edustamana.
|24 bit format (TrueColor)|These bitmaps can have a maximum of 2^24 colors (biBitCount == 24).Each three-byte sequence in the bitmap data array represents the relative intensities of the three primary hues of a pixel. The hues are described as values ranging from 0 to 255 and are stored in the three bytes in the order Blue, Green and Red. This is an important distinction, because most references to colors in Windows use the opposite order: Red/Green/Blue, so think "BGR" when working with TrueColor images instead of "RGB". A color palette can be specified to accelerate the drawing process for Windows, in which case biClrUsed will not be 0. Mutta kuten näet, sitä ei tarvita, koska itse pikselitiedot sisältävät väritiedot.
|32-bittinen muoto|32-bittinen kuvissa on enintään 2^24 väriä (biBitCount == 24).

## Viitteet ##
  * [Laitteesta riippumattomat bittikartat – Microsoft](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

