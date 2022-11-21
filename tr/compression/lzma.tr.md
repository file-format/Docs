{
  "date" : "2021-04-08",
  "keywords" :[ "lzma dosyası", "lzma dosya biçimi", "lzma dosyası nedir", "dosya", "lzma örneği", "lzma dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - LZMA Sıkıştırılmış Dosya Formatı",
  "description":"LZMA dosyası ve LZMA dosyalarını oluşturabilen ve açabilen API'ler nedir?",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## LZMA dosyası nedir?

.lzma uzantılı bir dosya, LZMA (Lempel-Ziv-Markov zincir Algoritması) sıkıştırma yöntemi kullanılarak oluşturulan sıkıştırılmış bir arşiv dosyasıdır. Bunlar çoğunlukla Unix işletim sisteminde bulunur/kullanılır ve dosya boyutunu küçültmek için [ZIP](/tr/compression/zip/) gibi diğer sıkıştırma algoritmalarına benzer. LZMA, .xz biçimiyle değiştirilmekte olan veya değiştirilmekte olan eski bir dosya biçimidir. .lzma biçiminin MIME türü \`application/x-lzma' şeklindedir. Bu dosya biçimi, Igor Pavlov tarafından LZMA SDK'da kullanılmak üzere tasarlanmıştır.

## LZMA Dosya Biçimi

LZMA dosyası iki ana bölümden oluşur:

1. Başlık
1. Sıkıştırılmış Veri


### LZMA Başlığı

LZMA dosyaları, LZMA sıkıştırılmış verileri tarafından takip edilen 13 baytlık bir başlığa sahiptir. LZMA başlığı şunlardan oluşur:

* Özellikleri
* Sözlük Boyutu
* Sıkıştırılmamış Boyut

#### LZMA Başlık Özellikleri

Özellikler alanı üç özellik içerir. Parantez içinde bir kısaltma verilir ve ardından özelliğin değer aralığı gelir. alan oluşur

1) gerçek bağlam bitlerinin sayısı (lc, [0, 8]);
2) değişmez konum bitlerinin sayısı (lp, [0, 4]); ve
3) konum bitlerinin sayısı (pb, [0, 4]).

#### LZMA Sözlük Boyutu

Bu, 2^n ve 2^n + 2^(n-1) arasında değişen değerlere sahip, işaretsiz bir 32-bit küçük endian tamsayı olarak saklanır. LZMA Utils, dosyaları herhangi bir sözlük boyutuyla açabilir.

#### Sıkıştırılmamış Boyut
Sıkıştırılmamış Boyut, işaretsiz 64 bit küçük endian tamsayı olarak saklanır. 0xFFFF_FFFF_FFFF_FFFF özel değeri, Sıkıştırılmamış Boyutun bilinmediğini gösterir. Değer, ancak ve ancak Sıkıştırılmamış Boyut bilinmiyorsa Yük Yükü Sonu İşareti (\*) ile temsil edilir.

## Referanslar

* [LZMA Dosya Biçimi](https://svn.python.org/projects/external/xz-5.0.3/doc/lzma-file-format.txt)
* [Lempel–Ziv–Markov zincir algoritması](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)

