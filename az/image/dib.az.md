{
  "date": "2020-01-10",
  "keywords": [
"dib faylı",
"dib fayl formatı",
"dib faylı nədir",
"fayl",
"dib nümunəsi",
"dib fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DIB",
  "description": "DIB fayl formatı və DIB fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "DIB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-di-azb"
}
},
  "lastmod": "2020-01-10"
}

## DIB faylı nədir?

Cihazdan Müstəqil bitmap (DIB) standart Bitmap fayllarına ([BMP]()/image/bmp/) strukturuna bənzəyən rastr təsvir faylıdır. Bu, RGB rənglərinin piksel dəyərlərinə uyğunlaşdırılmasını təsvir edən rəng cədvəlini ehtiva edir. Bu, DIB-yə istənilən cihazda təsviri təmsil etməyə imkan verir. Windows və macOS-da standart BMP faylını aça bilən demək olar ki, bütün proqramlarla açıla bilər. DIB ikili fayllardır və BMP-yə bənzər mürəkkəb fayl formatına malikdir. DIB təsvirləri rəng dərinliyi və hər düymdə piksel baxımından göstərmə cihazlarının çıxış imkanlarından müstəqildir.

## DIB Fayl Formatının Xüsusiyyətləri ##
DIB aşağıdakı rəng və ölçü məlumatlarını ehtiva edir:

  * Düzbucaqlı şəklin yaradıldığı cihazın rəng formatı.
  * Düzbucaqlı təsvirin yaradıldığı cihazın həlli.
  * Təsvirin yaradıldığı cihaz üçün palitrası.
  * Qırmızı, yaşıl, mavi ( RGB ) üçlüyü düzbucaqlı şəkildəki piksellərlə əlaqələndirən bitlər massivi.
  * Bit massivinin ölçüsünü azaltmaq üçün istifadə edilən verilənlərin sıxılma sxemini (əgər varsa) göstərən verilənlərin sıxılma identifikatoru.

### DIB Məlumat Bloku formatı ###

DIB diskdə saxlanılan .DIB faylları ilə müqayisədə yaddaş bloku kontekstində gəlir. Yaddaş bloku DIB-lər üçün Windows API spesifikasiyasına uyğun olan strukturdan ibarətdir. Faktiki DIB aşağıdakılardan ibarətdir:
  * Başlıq
  * Rəng palitrası
  * Pixel Data

Praktiki olaraq, palitra, başlıq və təsvir məlumatları ilə işləmək, sanki üç ayrı yaddaş bloku kimi aparılır. Bu ümumi yaddaş blokuna dəstək GlobalAlloc istifadə edərək təyin edilir və başlıq, rəng cədvəli və piksel məlumatlarını çıxarmaq və işləmək üçün istifadə olunan HDIB kimi tanınır.

### Strukturlar ###
DİB-də olan məlumatlar müxtəlif strukturlarla təmsil olunur. Bunlara daxildir:

BITMAPInfo - DIB üçün ölçü və rəng məlumatını müəyyən edir
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
O, BITMAPINFOHEADER-dən ibarətdir:

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
sonra iki və ya daha çox RGBQAD strukturu.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Məlumat bitləri ###
|Bits|Təsvir|
---|---|
|1-bit format (monoxrom)|Monoxrom bitmaps iki rəngdən (qara və ağ) ibarətdir. Bu məhdud sayda rəng sayəsində bu bitmaplar diskdə daha az yer tutur. BitBitCount hər iki rəngin təmsili üçün doğru və ya yalanı qaytarır. Əgər bitBitCount==1 olarsa, tətbiqlərin əksəriyyəti palitranı tamamilə atlayır.
|4 bit format (VGA or 16 color)|Each byte of image data represents two pixels and bitBitCount==4. Bu bitlər azalan ardıcıllıqla pikselin rəngini təmsil edir.
|8 bit format (256 rəng)|Bu 8 bit format maksimum 256 rəngi təmsil edə bilər. Şəklin bitmap məlumat massivindəki hər bayt bir pikseli təmsil edir. Həmin baytın dəyəri bmciColors ilə təmsil olunan 256 girişdən istifadə ediləcək rəng palitrası girişinin sayıdır.
|24 bit format (TrueColor)|These bitmaps can have a maximum of 2^24 colors (biBitCount == 24).Each three-byte sequence in the bitmap data array represents the relative intensities of the three primary hues of a pixel. The hues are described as values ranging from 0 to 255 and are stored in the three bytes in the order Blue, Green and Red. This is an important distinction, because most references to colors in Windows use the opposite order: Red/Green/Blue, so think "BGR" when working with TrueColor images instead of "RGB". A color palette can be specified to accelerate the drawing process for Windows, in which case biClrUsed will not be 0. Ancaq gördüyünüz kimi, buna ehtiyac yoxdur, çünki piksel məlumatının özü rəng məlumatını ehtiva edir.
|32 bit format|32 bitlik şəkillər maksimum 2^24 rəngə malikdir (biBitCount == 24).

## İstinadlar ##
  * [Cihazdan Müstəqil Bitmaps - Microsoft tərəfindən](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

