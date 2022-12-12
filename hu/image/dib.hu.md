{
  "date" : "2020-01-10",
  "keywords" :[ "dib fájl", "dib fájl formátum", "mi az a dib fájl", "fájl", "dib példa", "dib fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"További információ a DIB fájlformátumról és az API-król, amelyek DIB fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Mi az a DIB fájl?

Az eszközfüggetlen bittérkép (DIB) egy raszteres képfájl, amely szerkezetében hasonló a szabványos bittérképes fájlokhoz ([BMP]()/image/bmp/)). Tartalmaz egy színtáblázatot, amely leírja az RGB színek pixelértékekhez való hozzárendelését. Ez lehetővé teszi, hogy a DIB bármilyen eszközön megjelenítse a képet. Szinte minden olyan alkalmazással megnyitható, amely képes megnyitni egy szabványos BMP-fájlt Windowson és macOS-en is. A DIB bináris fájlok, és összetett fájlformátumuk hasonló a BMP-hez. A DIB képek a színmélység és a pixel per hüvelyk aránya tekintetében függetlenek a renderelő eszközök kimeneti képességeitől.

## DIB fájlformátum specifikációi ##
A DIB a következő szín- és méretinformációkat tartalmazza:

* Annak az eszköznek a színformátuma, amelyen a téglalap alakú képet létrehozták.
* Annak az eszköznek a felbontása, amelyen a téglalap alakú képet létrehozták.
* Annak az eszköznek a palettája, amelyen a képet létrehozták.
* Bittömb, amely a piros, zöld, kék (RGB) hármasokat képpontokká képezi le a téglalap alakú képen.
* Adattömörítési azonosító, amely jelzi a bittömb méretének csökkentésére használt adattömörítési sémát (ha van ilyen).

### DIB adatblokk formátum ###

A DIB a memóriablokk kontextusában jelenik meg, összehasonlítva a lemezen tárolt .DIB fájlokkal. A memóriablokk olyan szerkezetből áll, amely megfelel a Windows API DIB-ekre vonatkozó specifikációinak. A tényleges DIB a következőkből áll:
* Egy fejléc
* Szín paletta
* Pixel adatok

Gyakorlatilag a paletta, fejléc és képadatokkal való munka úgy történik, mintha három különálló memóriablokkról lenne szó. Ehhez a közös memóriablokkhoz a GlobalAlloc segítségével van hozzárendelve egy fogantyú, HDIB néven ismert, amely a fejléc, a színtábla és a pixeladatok kinyerésére és kezelésére szolgál.

### Struktúrák ###
A DIB-ben található információkat különböző struktúrák képviselik. Ezek tartalmazzák:

BITMAPIinfo – Meghatározza a DIB méret- és színinformációit
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Egy BITMAPINFOHEADER-ből áll:

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
két vagy több RGBQAD struktúra követi.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Adatbitek ###
|Bits|Leírás|
---|---|
|1 bites formátum (monokróm)|A monokróm bittérképek két színből állnak (fekete és fehér). A korlátozott számú szín miatt ezek a bittérképek kevesebb helyet foglalnak el a lemezen. A bitBitCount értéke igaz vagy hamis mindkét szín megjelenítéséhez. A legtöbb alkalmazás teljesen kihagyja a palettát, ha bitBitCount==1.
|4 bites formátum (VGA vagy 16 szín)|A képadatok minden bájtja két képpontot jelent, és bitBitCount==4. Ezek a bitek a pixel színét jelzik csökkenő sorrendben.
|8 bites formátum (256 szín)|Ez a 8 bites formátum maximum 256 színt képes megjeleníteni. A kép bittérképes adattömbjének minden bájtja egyetlen képpontot jelent. Ennek a bájtnak az értéke a színpaletta-bejegyzés száma, amelyet a bmciColors által képviselt 256 bejegyzés közül kell használni.
|24 bites formátum (TrueColor)|Ezek a bittérképek legfeljebb 2^24 színt tartalmazhatnak (biBitCount == 24). A bittérképes adattömb minden hárombájtos sorozata egy képpont három elsődleges színárnyalatának relatív intenzitását jelenti. A színárnyalatokat 0 és 255 közötti értékként írják le, és három bájtban tárolják őket kék, zöld és piros sorrendben. Ez egy fontos különbség, mert a legtöbb színre való utalás a Windowsban fordított sorrendben történik: Piros/Zöld/Kék, ezért gondoljon a „BGR”-re, ha TrueColor-képekkel dolgozik az „RGB” helyett. Színpaletta megadható a rajzolási folyamat felgyorsítására a Windows számára, ebben az esetben a biClrUsed nem lesz 0. De mint látható, nincs rá szükség, mivel a pixeladatok magukban foglalják a színinformációkat.
|32 bites formátum|32 bites képek maximum 2^24 színt tartalmazhatnak (biBitCount == 24).

## Referenciák ##
* [Eszközfüggetlen bittérképek – Microsoft](https://docs.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

