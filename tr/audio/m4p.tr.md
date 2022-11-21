{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "dosya", "uzantı", "biçim", "m4p dosya biçimi nedir", "müzik", "m4p dosya biçimi", "M4b ve MP3", "m4p dosya biçimi belirtimi "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"M4P dosya formatı ve M4P dosyalarını oluşturabilen, dönüştürebilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"M4P - MPEG-4 Sesli Kitap Dosya Biçimi",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## M4P dosyası nedir?
.m4p uzantılı dosya, genellikle Apple iTunes mağazasında indirilebilen bir ses dosyasıdır. Başka bir deyişle, M4P'nin bir AAC dosyası olduğunu ancak bir Dijital Haklar Yönetimi (DRM) kullanarak kopya korumalı olduğunu söyleyebiliriz. Bu, M4P dosyalarının yalnızca yetkili sistemlerde veya cihazlarda oynatılabileceği anlamına gelir. Genellikle M4P dosyaları Apple multimedya cihazlarına özeldir. Yani bu dosyalar sadece Apple macbook'larda, podcast'lerde, iPhone 6 veya iPhone 7 gibi akıllı telefonlarda oynatılabiliyor.

## M4P Dosya Biçimi
M4P, MPEG 4 Korumalı (ses) anlamına gelir ve sesi gelişmiş ses codec'i (AAC) ile kodlar ve dosyayı izinsiz kullanıma karşı korur. Bu dosya formatı genellikle bir iTunes Music Store'un ses dosyası formatı olarak kabul edilir. Apple, M4P dosyalarını korumak için FairPlay Dijital Haklar Yönetimi (DRM) sistemini kullanır. FairPlay DRM, Veridisc tarafından geliştirilen teknolojiye dayalıdır. Koruma mekanizması, AES şifrelemesini kullanarak AAC ses akışını şifreleyerek çalışır. Kullanıcı, şifre çözme için hesabına atanan bir ana anahtar alır. Bu dosya formatı, MP3 dosya formatının yerini alması için tanıtıldı, çünkü MP3 orijinal olarak bir ses dosyası olarak değil, bir MPEG 1 veya 2 video dosyasında katman III olarak tasarlandı.


## M4P Dosya Biçimi Özellikleri

[M4A](/tr/audio/m4a/)'ya benzer şekilde, M4P dosyaları da ardışık parçalardan oluşur. Her yığın 8 bayt başlığa sahiptir ve şu şekilde alt bölümlere ayrılmıştır:
- 4 bayt yığın boyutu (big-endian, önce yüksek bayt)
- 4 bayt yığın türü - önceden tanımlanmış imzalardan biri: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", "jP2", "geniş", "yük", "imap", "mat", "çap", "kmat", "klip", "crgn", "sync", "tmcd", "PICT", "scpt "," ctab", "ssrc".

M4A'ya benzer şekilde, M4P'deki İlk öbek "ftype" tipinde olacaktır ve ofset 8'de bir alt tipe sahiptir. M4P, "M4P_" olması gereken alt tip tarafından tanımlanır.

Parçalar, bilinmeyen türde bir yığın algılanana kadar yinelenir, M4P (MPEG-4 Audio) dosyası oluşturur.

## Referanslar ##

* [MPEG-4 Bölüm 14 - Wikipedia'dan](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Kısım 14 Ses (M4A,M4B,M4P) Biçimi ve Kurtarma Örneği](https://www.file-recovery.com/m4a-signature-format.htm)

