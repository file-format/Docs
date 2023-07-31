{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - TrueType Koleksiyon Dosya Biçimi",
  "description":"Bir TrueType Koleksiyonu (TTC) dosyası, birden çok yazı tipini tek bir dosyada birleştirir. Hem Apple hem de Microsoft, Mac ve Windows İşletim sistemlerinde TTF kullanmıştır.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## .tc dosyası nedir?
TTC, TrueType Koleksiyonu olarak kısaltılır, True Type formatının bir uzantısıdır. Bir TTC dosyası, birden çok yazı tipi dosyasını içinde birleştirebilir. Bu dosyalar, birçok glifi ortak olarak paylaşan birden çok yazı tipini birleştirmek için faydalıdır. Windows 2000'den önce, TTC dosyaları Windows'un Çince, Japonca ve Korece sürümlerinde kullanılıyordu, ancak daha sonra destek tüm bölgeler için mevcuttu.


## Font Toplama Dosyasının Yapısı
Bir TTC dosyası, bir TTC Başlık tablosundan, Tablo Dizinlerinden ve birden çok OpenType tablosundan oluşur. TTC Başlığı, dosyanın başında bulunmalıdır. Her yazı tipi için eksiksiz bir tablo dizini bulunmalıdır. TableDirectory formatı, koleksiyon dışı bir dosyada var olana benzer olmalıdır. Bir TTC dosyası içindeki tüm dizinlerdeki tablo sayıları, bir TTC dosyasının başlangıcından itibaren hesaplanır.
Bir TTC dosyasındaki tablolara ilgili yazı tiplerinin tablo dizini aracılığıyla başvurulur. OpenType tablolarından birkaçı, TTC'ye eklenen her yazı tipi için bir kez olmak üzere birden çok kez görünmelidir. Diğer tablolar ise TTC dosyasında birden fazla yazı tipi tarafından paylaşılabilir.

### TTC Başlığı
TTC Başlık tablosunun şu ana kadar iki sürümü mevcuttur:
- Sürüm 1.0, dijital imzaları olmayan TTC dosyaları için kullanılır.
- Sürüm 2.0, dijital imzalı veya dijital imzasız TTC dosyaları için kullanılabilir.
Her iki versiyonun da TTC Başlık tabloları şunlardır:

**TTC Başlığı Sürüm 1.0:**

|Tür|Ad|Açıklama|
---|---|---|
|TAG|ttcTag|Yazı Tipi Koleksiyonu Kimliği dizesi: 'ttcf' (CFF veya CFF2 ana hatları ile TrueType ana hatları olan yazı tipleri için kullanılır)|
|uint16|majorVersion|TTC Başlığının ana sürümü, = 1.|
|uint16|minorVersion|TTC Başlığının küçük sürümü, = 0.|
|uint32|numFonts|TTC'deki yazı tipi sayısı|
|Offset32|tableDirectoryOffsets[numFonts]|Dosyanın başından itibaren her yazı tipi için TableDirectory'deki ofset dizisi|

**TTC Başlığı Sürüm 2.0:**

|Tür|Ad|Açıklama|
---|---|---|
|TAG|ttcTag |Yazı Tipi Koleksiyonu Kimliği dizesi: 'ttcf'|
|uint16| majorVersion |TTC Başlığının ana sürümü, = 2.|
|uint16| minorVersion |TTC Başlığının küçük versiyonu, = 0.|
|uint32| numFonts |TTC'deki yazı tipi sayısı|
|Ofset32| tableDirectoryOffsets[numFonts] |Dosyanın başlangıcından itibaren her yazı tipi için TabloDirectory'deki ofset dizisi|
|uint32| dsigTag |Bir DSIG tablosunun var olduğunu gösteren etiket, 0x44534947 ('DSIG') (imza yoksa boş)|
|uint32| dsigLength |DSIG tablosunun uzunluğu (bayt olarak) (imza yoksa boş)|
|uint32| dsigOffset |DSIG tablosunun TTC dosyasının başından farkı (bayt cinsinden) (imza yoksa boş)|

## Referanslar
* [OpenType Yazı Tipi Dosyası](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

