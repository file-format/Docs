{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCX Dosya Biçimi - Paintbrush Bitmap Görüntü Dosyası",
  "description":"PCX dosya formatı ve PCX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## PCX dosyası nedir?

Bir PCX dosyası, Picture Exchange dosyası, PC Paintbrush uygulaması için yerel dosya formatı olarak kullanılan bir raster görüntü dosyası formatıdır. ZSoft Corporation, ABD tarafından DOS ve Windows platformları için geliştirildi ve [BMP](/tr/image/bmp/), [JPEG](/tr/image/jpeg/) ve [ PNG](/tr/image/png/) dosya biçimleri. PCX dosyalarının boyutu, RLE kodlaması kullanılarak sıkıştırıldıklarından daha küçüktür. Öncelikle dijital faks dosyaları oluşturmak için kullanılan çok sayfalı [DCX](/tr/image/dcx/) dosyasında kullanılır.

## PCX Dosya Biçimi

PCX dosyaları, ikili dosya biçiminde diske kaydedilir. Dahili dosya formatı yapısı, küçük endian bayt sıralamasını takip eder ve aşağıdaki üç bölümden oluşur:

**`PCX Başlığı`** - Bir PCX Başlığı 128 bayt uzunluğundadır. Bir tanımlayıcı, sürüm numarası, görüntü boyutları, 16 palet rengi, sayı renk düzlemleri ve her düzlemin bit derinliği ve sıkıştırma yöntemi için bir değer içerir.

PCX Başlığı, Ansiklopedi grafik dosyası formatlarından (2. baskı) referans alınarak aşağıda gösterildiği gibidir.
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`Görüntü Verileri`** - PCX görüntü verileri başlıktan hemen sonra gelir. Görüntü verileri, başlıktaki alan ayarına bağlı olarak sıkıştırılabilir. Verilerin PCX dosyasında saklanması, belirtilen renk düzlemlerinin sayısına bağlıdır. Görüntü verileri satırlar halinde düzenlenir. Birden çok düzlem olması durumunda, bunlar kırmızı, yeşil ve mavi verilerin sıralı düzeninde satır içinde düzleme göre depolanır. Bu model, düzlemdeki her çizgi için tekrarlanır.

## Referanslar

* [PCX - Wikipedia'dan](https://en.wikipedia.org/wiki/PCX)

