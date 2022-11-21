{
  "date" : "2019-10-11",
  "keywords" :[ "tbz dosyası", "tbz dosya biçimi", "tbz dosyası nedir", "dosya", "tbz örneği", "tbz dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Bzip Sıkıştırılmış Tar Arşivi",
  "description":"TBZ dosya formatı ve TBZ dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## .tbz dosyası nedir?

.tbz uzantılı bir dosya, içerik dosyalarının boyutunu küçültmek için BZIP sıkıştırması kullanan sıkıştırılmış bir arşivdir. TBZ dosyaları aslında BZIP ile sıkıştırılmış UNIX [TAR](/tr/compression/tar/) arşivlenmiş dosyalardır. En son ikinci düzey sıkıştırma, BZIP'in yerini alan [BZIP2](/tr/compression/bz2/)'dir. TBZ dosya biçimi, büyük dosyaların aktarımı için uygundur. TBZ dosyaları, 7-Zip, PeaZip ve jZip gibi yazılım uygulamaları kullanılarak açılabilir/çıkarılabilir. Linux ve macOS kullanıcıları ayrıca bir terminal penceresinden BZIP2 komutuyla bir TBZ açabilir.

## TBZ Dosya Biçimi

TBZ dosyaları aslında BZIP/[BZIP2](/tr/compression/bz2) sıkıştırmasıyla oluşturulan sıkıştırılmış arşivlerdir. Bu dosya biçimi için resmi bir belirtim yoktur. Bununla birlikte, resmi olmayan bir [tersine mühendislik spesifikasyonu](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf), bir .bz2 akışının 4 baytlık bir başlıktan oluştuğunu ve bunu izleyen sıfır veya daha fazla sıkıştırılmış blok ile.

## Referanslar ##

* [BZIP2 Biçim Özellikleri](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

