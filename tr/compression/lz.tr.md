{
  "date" : "2021-04-08",
  "keywords" :[ "lz dosyası", "lz dosya biçimi", "lz dosyası nedir", "dosya", "lz örneği", "lz dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Lzip Sıkıştırılmış Dosya Biçimi",
  "description":"LZ dosya formatı ve LZ dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## .lz dosyası nedir?

.lz uzantılı bir dosya, sıkıştırma için ücretsiz bir komut satırı aracı olan Lzip ile oluşturulan sıkıştırılmış bir arşiv dosyasıdır. Destek dosyalarını sıkıştırmak için birleştirmeyi destekler. LZ dosyalarının uygulama/lzip ortam türü vardır ve [BZ2](/tr/compression/bz2/)'den daha yüksek sıkıştırma oranlarını destekler. LZ, LZMA (Lempel-Ziv-Markov zinciri) algoritmasına dayalıdır ve dosyanın bütünlüğünü kontrol etmek için 32 bitlik bir CRC sağlama toplamı ve kimlik baytları içerir.

## LZMA Sıkıştırılmış Format

LZMA sıkıştırılmış biçimi, uyarlanabilir ikili aralık kodlayıcı kullanılarak kodlanan sıkıştırılmış bir bit akışından oluşur. Akış paketlere bölünmüştür. Her paket, tek bir baytı veya bir LZ77 dizisini tanımlar. Her paketin uzunluğu ve mesafesi dolaylı veya açık bir şekilde kodlanmıştır.

Yedi paket türü aşağıdaki gibidir ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Paket kodu (bit dizisi) |Paket adı |Paket açıklaması|
---|---|---|
|0 + baytKodu| AYDINLATMA | Uyarlanabilir bir ikili aralık kodlayıcı kullanılarak kodlanmış tek bir bayt.|
|1+0 + uzunluk + mesafe| MAÇ| Dizi uzunluğu ve mesafesini tanımlayan tipik bir LZ77 dizisi.|
|1+1+0+0| KISA REP| Bir baytlık LZ77 dizisi. Mesafe, son kullanılan LZ77 mesafesine eşittir.|
|1+1+0+1 + uzunluk| UZUNGREP[0]| Bir LZ77 dizisi. Mesafe, son kullanılan LZ77 mesafesine eşittir.|
|1+1+1+0 + uzunluk| UZUNGREP[1]| Bir LZ77 dizisi. Mesafe, son kullanılan ikinci LZ77 mesafesine eşittir.|
|1+1+1+1+0 + uzunluk| UZUNGREP[2]| Bir LZ77 dizisi. Mesafe, son kullanılan üçüncü LZ77 mesafesine eşittir.|
|1+1+1+1+1 + uzunluk| UZUNGREP[3]| Bir LZ77 dizisi. Mesafe, son kullanılan dördüncü LZ77 mesafesine eşittir.|


## Referanslar

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

