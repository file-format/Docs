{
  "date" : "2019-10-11",
  "keywords" :[ "bz2 dosyası", "bz2 dosya biçimi", "bz2 dosyası nedir", "dosya", "bz2 örneği", "bz2 dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - Sıkıştırılmış Dosya Biçimi",
  "description":"BZ2 dosyasının ne olduğunu ve BZ2 dosyalarını oluşturabilen ve açabilen API'leri öğrenin.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## BZ2 dosyası nedir?

BZ2, çoğunlukla UNIX veya Linux sisteminde [BZIP2](http://www.bzip.org/) açık kaynak sıkıştırma yöntemi kullanılarak oluşturulan sıkıştırılmış dosyalardır. Tek bir dosyanın sıkıştırılması için kullanılır ve birden fazla dosyanın arşivlenmesi amaçlanmamıştır. Bu, birden çok dosyayı tek bir dosyada ancak sıkıştırma olmadan arşivleyen aynı platformlardaki TAR dosya biçiminin tersidir. BZ2 olarak sıkıştırılan dosyalar, [WinZip](https://www.winzip.com/win/en/) gibi uygulamalarla açılabilir. BZIP2, yüksek düzeyde sıkıştırma elde etmek için Run-Length Encoding (RLE) veya [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) sıkıştırma algoritmasını kullanır.

## BZ2 Dosya Biçimi

Bu dosya biçimi için resmi bir belirtim yoktur. Bununla birlikte, resmi olmayan bir [tersine mühendislik spesifikasyonu](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf), bir .bz2 akışının 4 baytlık bir başlıktan oluştuğunu ve bunu izleyen sıfır veya daha fazla sıkıştırılmış blok ile. Bunun hemen ardından, işlenen tüm akış düz metin için 32 bitlik bir CRC içeren bir akış sonu işaretçisi gelir. Sıkıştırılmış bloklar arasında dolgu yoktur ve tüm bloklar bit hizalıdır.

## BZ2 Dosyasını Açın/Çıkarın

WinZip gibi bir yazılım kullanarak Windows ve Mac OS'de bir BZ2 dosyasını açabilirsiniz. Linux'ta, terminalde aşağıdaki komut.

```
bzip2 -d filename.bz2
```

## Referanslar

* [BZIP2 Biçim Özellikleri](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

