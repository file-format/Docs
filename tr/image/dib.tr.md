{
  "date" : "2020-01-10",
  "keywords" :[ "dib dosyası", "dib dosya formatı", "dib dosyası nedir", "dosya", "dib örneği", "dib dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DİB",
  "description":"DIB dosya formatı ve DIB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## .dib dosyası nedir?

Aygıttan Bağımsız bir bitmap (DIB), yapı olarak standart Bitmap dosyalarına ([BMP]()/image/bmp/) benzeyen bir raster görüntü dosyasıdır. RGB renklerinin piksel değerlerine eşlenmesini açıklayan bir renk tablosu içerir. Bu, DIB'nin görüntüyü herhangi bir cihazda temsil etmesini sağlar. MacOS'un yanı sıra Windows'ta standart bir BMP dosyası açabilen hemen hemen tüm uygulamalarla açılabilir. DIB, ikili dosyalardır ve BMP'ye benzer karmaşık bir dosya biçimine sahiptir. DIB görüntüleri, renk derinliği ve inç başına piksel açısından işleme cihazlarının çıktı kapasitelerinden bağımsızdır.

## DIB Dosya Biçimi Özellikleri ##
Bir DIB, aşağıdaki renk ve boyut bilgilerini içerir:

* Dikdörtgen görüntünün oluşturulduğu cihazın renk formatı.
* Dikdörtgen görüntünün oluşturulduğu cihazın çözünürlüğü.
* Görüntünün oluşturulduğu cihazın paleti.
* Dikdörtgen görüntüdeki kırmızı, yeşil, mavi (RGB) üçlülerini piksellere eşleyen bir bit dizisi.
* Bit dizisinin boyutunu azaltmak için kullanılan veri sıkıştırma şemasını (varsa) gösteren bir veri sıkıştırma tanımlayıcısı.

### DIB Veri Bloğu formatı ###

DIB, diskte depolanan .DIB dosyalarına kıyasla bellek bloğu bağlamında gelir. Bellek bloğu, DIB'ler için Windows API belirtimlerine uygun yapıdan oluşur. Gerçek DIB şunlardan oluşur:
* Bir başlık
* Renk paleti
* Piksel Verileri

Pratik olarak, palet, başlık ve görüntü verileriyle çalışmak, sanki üç ayrı bellek bloğuymuş gibi yapılır. Bu ortak bellek bloğuna GlobalAlloc kullanılarak bir tanıtıcı atanır ve başlık, renk tablosu ve piksel verilerini ayıklamak ve bunlarla çalışmak için kullanılan HDIB olarak bilinir.

### Yapılar ###
Bir DIB'de bulunan bilgiler farklı yapılarla temsil edilir. Bunlar şunları içerir:

BITMAPInfo - DIB'ler için boyut ve renk bilgilerini tanımlar
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Bir BITMAPINFOHEADER'dan oluşur:

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
ardından iki veya daha fazla RGBQAD yapısı.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Veri bitleri ###
|Bit|Açıklama|
---|---|
|1-bit formatı (tek renkli)|Tek renkli bit eşlemler iki renkten (siyah ve beyaz) oluşur. Bu sınırlı sayıda renk nedeniyle, bu bit eşlemler diskte daha az yer kaplar. bitBitCount, her iki rengin temsili için doğru veya yanlış döndürür. bitBitCount==1 ise, uygulamaların çoğu paleti tamamen atlar.
|4 bit formatı (VGA veya 16 renk)|Görüntü verilerinin her baytı iki pikseli temsil eder ve bitBitCount==4. Bu bitler, azalan sırada pikselin rengini temsil eder.
|8 bit format (256 renk)|Bu 8 bit format maksimum 256 rengi temsil edebilir. Görüntünün bitmap veri dizisindeki her bayt, tek bir pikseli temsil eder. Bu baytın değeri, bmciColors tarafından temsil edildiği şekliyle 256 girişten kullanılacak renk paleti girişinin numarasıdır.
|24 bit format (TrueColor)|Bu bitmap'ler maksimum 2^24 renge sahip olabilir (biBitCount == 24). Bitmap veri dizisindeki her üç baytlık dizi, bir pikselin üç ana tonunun göreli yoğunluğunu temsil eder. Tonlar, 0 ile 255 arasında değişen değerler olarak tanımlanır ve Mavi, Yeşil ve Kırmızı sırasıyla üç baytta saklanır. Bu önemli bir ayrımdır, çünkü Windows'ta renk referanslarının çoğu ters sırayı kullanır: Kırmızı/Yeşil/Mavi, bu nedenle TrueColor görüntülerle çalışırken "RGB" yerine "BGR"yi düşünün. Windows için çizim sürecini hızlandırmak için bir renk paleti belirtilebilir, bu durumda biClrUsed 0 olmaz. Ancak gördüğünüz gibi, piksel verilerinin kendisi renk bilgisini içerdiğinden buna gerek yoktur.
|32 bit biçim|32 bit görüntülerde maksimum 2^24 renk bulunur (biBitCount == 24).

## Referanslar ##
* [Aygıttan Bağımsız Bit Eşlemler - Microsoft Tarafından](https://docs.Microsoft.com/en-us/windows/win32/gdi/device-in Depended-bitmaps)

