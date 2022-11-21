{
  "date" : "2020-08-20",
  "keywords" :[ "cff dosyası", "cff dosya biçimi", "cff dosyası nedir", "dosya", "cff örneği", "cff dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - Kompakt Yazı Tipi Dosya Biçimi",
  "description":"CFF Dosya Biçimi ve CFF dosyaları oluşturmak ve açmak için API'ler hakkında bilgi edinin.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## .cff dosyası nedir?

.cff uzantılı bir dosya, Kompakt Yazı Tipi Biçimidir ve PostScript Type 1 veya CIDFont olarak da bilinir. CFF, FontSet olarak bilinen tek bir birimde birden çok yazı tipini bir arada depolamak için bir kap görevi görür. CFF yazı tiplerinin tasarımı, yazıcı ortamlarında kullanım için biçimin ek esnekliğine ve genişletilebilirliğine izin veren PostScript dil kodunun yerleştirilmesine izin verir. CFF yazı tipi dosyaları [Aspose.Font](https://products.aspose.com/font) gibi API'ler kullanılarak açılıp dönüştürülebilir.

## CFF Dosya Biçimi

CFF dosyaları, yapılandırılmış bir veri düzeni içeren, tanımlanmış veri türleri, bir başlık, glif organizasyonu ve tablo sözlükleri içeren ikili dosyalardır. Bunlar hakkında daha fazla ayrıntı [kompakt yazı tipi biçimi belirtimlerinde](https://docs.Microsoft.com/en-us/typography/opentype/spec/cff) bulunabilir.

### Veri Düzeni
CFF dosya formatının veri düzeni aşağıda gösterildiği gibidir.

|Giriş|Yorumlar|
---|---|
|Başlık|–|
|AdINDEX|–|
|Üst DICT ENDEKSİ|–|
|Dize DİZİNİ|–|
|Küresel Subr ENDEKSİ|–|
|Kodlamalar–Karakter Kümeleri|–|
|FDSelect|Yalnızca CIDFontlar|
|CharStrings INDEX|yazı tipi başına|
|Font DICT INDEX|yazı tipi başına, yalnızca CIDFonts|
|Özel DICT|yazı tipi başına|
|Yerel Subr INDEX|yazı tipi başına veya CIDFonts için Özel DICT başına|
|Telif Hakkı ve Ticari Marka Bildirimleri|–|

### Veri tipleri

CFF veri türleri aşağıdaki tabloda gösterildiği gibidir.

|Ad|Aralık|Açıklama|
---|---|---|
|Card8|0 –255|1 bayt işaretsiz sayı|
|Kart16|0 – 65535|2 bayt işaretsiz sayı|
|Ofset|değişir|1, 2, 3 veya 4 bayt ofset (Offset alanı tarafından belirlenir)|
|OffSize|1–4|1 baytlık işaretsiz sayı, Ofset alanının veya alanların boyutunu belirtir|
|SID|0 – 64999|2 bayt dizi tanımlayıcısı|

### Başlık

İkili veriler, aşağıdaki tabloda gösterilen formata sahip bir başlık ile başlar.

|Tür|Ad|Açıklama|
---|---|---|
|Card8|major|Ana sürümü biçimlendir (1'den başlayarak)|
|Kart8|küçük|Küçük sürümü biçimlendir (0'dan başlayarak)|
|Kart8|hdrSize| Başlık boyutu (bayt)|
|OffSize|offSize|Mutlak ofset (0) boyutu|

## Referanslar

* [Kompakt Yazı Tipi Biçimi Tablosu](https://docs.microsoft.com/en-us/typography/opentype/spec/cff)
* [CFF Dosya Biçimi](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [CFF2 Chartset](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

