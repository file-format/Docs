{
  "date" : "2020-01-10",
  "keywords" :[ "soubor dib", "formát souboru dib", "co je soubor dib", "soubor", "příklad dib", "přípona souboru dib", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"Další informace o formátu souborů DIB a rozhraních API, která mohou vytvářet a otevírat soubory DIB.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Co je soubor DIB?

Bitmapa nezávislá na zařízení (DIB) je soubor rastrového obrázku, který má podobnou strukturu jako standardní bitmapové soubory ([BMP]()/image/bmp/)). Obsahuje tabulku barev, která popisuje mapování barev RGB na hodnoty pixelů. To umožňuje DIB reprezentovat obraz na jakémkoli zařízení. Lze jej otevřít téměř všemi aplikacemi, které dokážou otevřít standardní soubor BMP ve Windows i macOS. DIB jsou binární soubory a mají složitý formát souborů podobný BMP. Obrazy DIB jsou nezávislé na výstupních možnostech vykreslovacích zařízení, pokud jde o barevnou hloubku a pixel na palec.

## Specifikace formátu souboru DIB ##
DIB obsahuje následující informace o barvě a rozměrech:

* Formát barev zařízení, na kterém byl vytvořen obdélníkový obrázek.
* Rozlišení zařízení, na kterém byl vytvořen obdélníkový obrázek.
* Paleta pro zařízení, na kterém byl obrázek vytvořen.
* Pole bitů, které mapuje červené, zelené, modré (RGB) trojice na pixely v obdélníkovém obrázku.
* Identifikátor komprese dat, který označuje schéma komprese dat (pokud existuje) používané ke zmenšení velikosti pole bitů.

### Formát datového bloku DIB ###

DIB přichází v kontextu paměťového bloku ve srovnání se soubory .DIB uloženými na disku. Paměťový blok obsahuje strukturu, která je v souladu se specifikacemi Windows API pro DIB. Aktuální DIB se skládá z:
* Záhlaví
* Paleta barev
* Údaje o pixelech

Prakticky se práce s paletou, záhlavím a obrazovými daty provádí tak, jako by šlo o tři samostatné bloky paměti. Úchyt k tomuto společnému bloku paměti je přiřazen pomocí GlobalAlloc a je známý jako HDIB, který se používá k extrahování a práci s daty záhlaví, tabulky barev a pixelů.

### Struktury ###
Informace obsažené v DIB jsou reprezentovány různými strukturami. Tyto zahrnují:

BITMAPInfo - Definuje informace o rozměrech a barvách pro DIB
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Skládá se z BITMAPINFOHEADER:

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
následované dvěma nebo více strukturami RGBQAD.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Datové bity ###
|Bity|Popis|
---|---|
|1bitový formát (monochromatický)|Monochromatické bitmapy se skládají ze dvou barev (černá a bílá). Kvůli tomuto omezenému počtu barev zabírají tyto bitmapy méně místa na disku. BitBitCount vrací hodnotu true nebo false pro reprezentaci obou barev. Většina aplikací paletu úplně přeskočí, pokud bitBitCount==1.
|4bitový formát (VGA nebo 16 barev)|Každý bajt obrazových dat představuje dva pixely a bitBitCount==4. Tyto bity představují barvu pixelu v sestupném pořadí.
|8bitový formát (256 barev)|Tento 8bitový formát může reprezentovat maximálně 256 barev. Každý bajt v poli bitmapových dat obrázku představuje jeden pixel. Hodnota tohoto bajtu je číslo položky palety barev, která má být použita z 256 položek reprezentovaných bmciColors.
|24bitový formát (TrueColor)|Tyto bitmapy mohou mít maximálně 2^24 barev (biBitCount == 24). Každá tříbajtová sekvence v poli bitmapových dat představuje relativní intenzity tří primárních odstínů pixelu. Odstíny jsou popsány jako hodnoty v rozsahu od 0 do 255 a jsou uloženy ve třech bytech v pořadí modrá, zelená a červená. Toto je důležitý rozdíl, protože většina odkazů na barvy ve Windows používá opačné pořadí: Červená/Zelená/Modrá, takže při práci s obrázky TrueColor myslete na „BGR“ místo „RGB“. Pro urychlení procesu kreslení pro Windows lze zadat barevnou paletu, v takovém případě nebude biClrUsed 0. Ale jak vidíte, není to potřeba, protože samotná data pixelů obsahují informace o barvě.
|32bitový formát|32bitové obrázky mají maximálně 2^24 barev (biBitCount == 24).

## Reference ##
* [Bitmapy nezávislé na zařízení – od společnosti Microsoft](https://docs.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

