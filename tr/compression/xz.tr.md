{
  "date" : "2022-01-23",
  "keywords" :[ "xz dosyası", "dosya formatı", "xz dosyası nedir", "dosya", "xz örneği", "xz dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XZ Dosyası - XZ Sıkıştırılmış Arşiv",
  "description":"XZ dosya formatı ve XZ dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## Bir XZ dosyası nedir?

XZ, LZMA2 sıkıştırma algoritmasını kullanan sıkıştırılmış bir dosya biçimidir. Popüler gzip ve bzip2 biçimlerinin yerine geçecek şekilde tasarlanmıştır ve bu eski standartlara göre bir dizi avantaj sunar. XZ dosyaları birçok platformda iyi desteklenir ve hızlı ve kolay bir şekilde sıkıştırılmış dosyaları açılabilir. [ZIP](/tr/compression/zip/) veya [RAR](/tr/compression/rar/) dosyaları kadar yaygın olmasalar da, XZ arşivleri, sıkıştırma kalitesinden ödün vermeden büyük miktarda veri depolamak için kullanılabilir. Büyük dosyaları sıkıştırmanız veya açmanız gerekirse, XZ dosya uzantısı dikkate alınmaya değer.

## XZ Dosya Biçimi

XZ dosyası oluşturulur ve diske ikili dosyalar olarak kaydedilir. Verileri sıkıştırmak için LZMA algoritmasını kullanır ve %50'ye kadar sıkıştırma oranı elde edebilir. XZ dosyaları genellikle yazılım dağıtımları ve yedekleme arşivleri için kullanılır. Çoğu Linux dağıtımında bulunan XZ yardımcı programı kullanılarak sıkıştırılmış dosyaları açılabilirler.

## XZ Dosyalarını Linux/Unix'te Açın

XZ dosyalarını açmak için önce `xz-utils` paketini kurun:
```
$ sudo apt-get install xz-utils
```

.xz dosyalarını ayıklamak için "unxz" komutunu kullanın:
```
$ unxz compressed_xz_file.xz
```

veya XZ'nin --decompress seçeneğini kullanarak:
```
$ xz --decompress compressed_xz_file.xz
```

## Referanslar

* [XZ Araçları](https://en.wikipedia.org/wiki/XZ_Utils)

