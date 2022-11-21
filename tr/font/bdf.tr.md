{
  "date" : "2021-02-25",
  "keywords" :[ "bdf dosyası", "bdf dosya biçimi", "bdf dosyası nedir", "dosya", "bdf örneği", "bdf dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - Glyph Bitmap Dağıtım Formatı",
  "description":"BDF dosya formatı ve BDF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## .df dosyası nedir?
BDF dosyaları insanlar tarafından okunabilir formdadır ve genellikle bir ASCII kodlamasıyla dağıtılır. Dosya, tam yazı tipiyle ilgili genel bilgilerle başlar, ardından bireysel glifler için bilgiler ve bit eşlemler gelir. İçindeki veriler, tek boyutlu yönlendirme için yazı tipini gösterir. Birden fazla yönde kullanılacak metrikler tek bir dosyada yer alabilir. BDF dosyasında, her öğe, dosyadaki ayrı bir metin satırında yer alır. Boşluklar, bir satırdaki öğeleri ayırmak için kullanılır.

## BDF dosya biçimi
Glif Bitmap Dağıtım Formatı için BDF kısaltması; Adobe'ye ait olan, bitmap tipindeki yazı tiplerini kaydetmek için bir dosya formatıdır. İçerik, hem bilgisayar hem de insan tarafından okunabilir olması amaçlanan bir metin dosyası biçimini alır. BDF, özellikle Unix X Pencere ortamlarında kullanılır. Daha verimli olması beklenen PCF yazı tipi formatı ve OpenType ve TrueType yazı tipleri ile yaygın olarak değiştirildi.
### BDF dosya yapısı
Bir BDF yazı tipi dosyası üç bölümden oluşur:

- bir yazı tipindeki tüm glifler için geçerli olan genel bir bölüm.
- her glif için ayrı bir giriş içeren bir bölüm.
- ENDFONT ifadesi.

## Örnek
İşte ASCII büyük 'A' için bir glif içeren örnek bir yazı tipi. Global bildirimleri "STARTFONT" satırı ile başlar ve "CHARS" satırı ile biter.
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## Referanslar
* [Glyph Bitmap Dağıtım Formatı](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Glif Bit Eşlem Dağıtım Biçimi (BDF) Spesifikasyonu](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

