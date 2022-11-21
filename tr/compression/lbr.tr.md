{
  "date" : "2021-04-08",
  "keywords" :[ "mst dosyası", "mst dosya biçimi", "mst dosyası nedir", "dosya", "mst örneği", "mst dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
	

},
  "draft" : "false",
  "toc" : true,
  "title" :"LBR - LU Kitaplık Arşiv Dosya Biçimi",
  "description":"LBR dosya formatı ve LBR dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## .lbr dosyası nedir?

.lbr uzantılı bir dosya, LU programı ile oluşturulan ve 1980'li yıllarda CP/M ve DOS işletim sistemlerinde kullanılan bir arşiv dosyasıdır. Artık kullanılmamaktadır ve yerini modern arşivleme dosya biçimleri almıştır. Biçim, üye dosyalarını sıkıştırmaz ve bunlar için kapsayıcı arşiv görevi görür. Arşivleme özelliği daha çok arşivlenen dosyaların internet üzerinden aktarımı için kullanılıyordu. LBR sıkıştırma sunmadığı için, SQ veya CRUNCH gibi diğer yardımcı programlar arşivleme öncesi üye dosyalarını sıkıştırmak için veya sonuçta ortaya çıkan arşiv dosyasını arşivleme sonrası boyutunu küçültmek için kullandı.

## LBR Dosya Biçimi

LBR dosya biçimi Gary P. Novosielski tarafından tasarlanmıştır ve kamuya açık hiçbir teknik ayrıntıya sahip değildir. LBR dosyaları 0x00 bayt ile başlar, ardından 11 boşluk (0x20), ardından iki 0x00 bayt ve ardından her ikisi de 0x00 olmayan iki bayt gelir. Konteyner dosya formatı olduğundan, LU.COM ve NULU.COM kullanılarak çıkarılabilir.

## Referanslar

* [LBR - Wikipedia](https://en.wikipedia.org/wiki/LBR_(file_format))

