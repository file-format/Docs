{
  "date" : "2019-12-09",
  "keywords" :[ "zl dosyası", "zl dosya biçimi", "zl dosyası nedir", "dosya", "zl örneği", "zl dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - ZLIP Sıkıştırılmış Dosya Biçimi",
  "description":"ZL dosya formatı ve ZL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## .zl dosyası nedir?

.zl uzantılı bir dosya, dosyaları sıkıştırmak için DEFLATE sıkıştırma algoritmasının bir çeşidini kullanan bir ZLIP sıkıştırılmış dosya biçimidir. CPU tipi, işletim sistemi, dosya sistemi ve karakter setinden bağımsızdır ve bu nedenle bilgi alışverişi için kullanılabilir. ZLIP sıkıştırmasının teknik özellikleri [IETF sitesinde](https://tools.ietf.org/html/rfc1950) mevcuttur ve geliştiricinin bakış açısıyla belirtilebilir.

## ZL Dosya Biçimi

Bir zlib akışı aşağıdaki yapıya sahiptir:

* `CMF (Compression Method and flags)` - Bu bayt, sıkıştırma yöntemine bağlı olarak 4 bitlik bir sıkıştırma yöntemine ve 4 bitlik bir bilgi alanına bölünmüştür.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (Sıkıştırma yöntemi)` - Dosyada kullanılan sıkıştırma yöntemini tanımlar. Değerleri ve karşılık gelen sıkıştırma yöntemi aşağıdaki gibidir.

| CM Değeri| Sıkıştırma|
|---|---|
|CM = 8|DEFLATE, 32K'ya kadar bir pencere boyutuyla|
|CM = 15|Ayrılmış|

* `CINFO (Sıkıştırma bilgisi)' - CM = 8 için CINFO, LZ77 pencere boyutunun 2 tabanlı logaritmasıdır, eksi sekizdir (CINFO=7, 32K pencere boyutunu gösterir).

* `FLG (FLaGs)` - Bu bayrak baytı aşağıdaki gibi bölünür:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Referanslar ##

* [Zlib Dosya Biçimi Özellikleri](https://tools.ietf.org/html/rfc1950)

