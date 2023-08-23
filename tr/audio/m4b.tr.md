{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "dosya", "uzantı", "biçim", "m4b dosya biçimi nedir", "müzik", "m4b dosya biçimi", "M4b ve MP3", "m4b dosya biçimi belirtimi "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"M4B dosya formatı ve M4B dosyalarını oluşturabilen, dönüştürebilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"M4B - MPEG-4 Sesli Kitap Dosya Biçimi",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## M4B dosyası nedir?

.m4b uzantılı dosya, genellikle Apple Books ve iTunes tarafından kullanılan bir sesli kitaptır. Bu formatta kullanılan Ses, MPEG-4'te saklanır ve AAC kodlaması kullanılarak sıkıştırılır. Bir M4B dosyası, M4A'ya çok benzer, ancak yer imi ve bölüm sonları gibi sesli kitapla ilgili özellikleri destekler. M4B dosyaları, hem DRM özellikli hem de DRM'siz sürümlerde mevcuttur. DRM şifreli sesli kitaplar genellikle iTunes Store'dan alınan ücretli sesli kitaplardır. Oysa DRM'siz, internet üzerinden kolayca bulunabilir.

## M4B Dosya Biçimi

Meta veri, resim, yer imleri ve köprüler içeren sesli kitap dosyaları .m4a uzantısıyla kaydedilebilir ancak genellikle dosyanın sesli kitap dosya formatına sahip olduğunu belirtmek için kaydederken .m4b uzantısı kullanılır. Fairplay DRM (Dijital Haklar Yönetimi), M4B dosyalarını korumak için başvuru tarafından kullanılır. Böylece iTunes'dan indirilen dosyalar yalnızca yetkili cihazlarda veya bilgisayarlarda oynatılabilir.


## M4B ve M4A

Hem M4B hem de [MP3](/audio/mp3/) yalnızca ses dosya biçimleridir.

**M4B**: Her ikisini de aynı bit hızında kodlarsanız, kalite açısından MP3 ile karşılaştırıldığında kazanır. M4B, AAC kodlaması kullanılarak sıkıştırılmış bir sesli kitap dosyasıdır. Temel olarak “MPEG-4 Ses Katmanı” ile ilişkilendirilir, .m4b uzantılı dosyalar MPEG-4 filmlerin ses katmanıdır, ancak sesli kitapla ilgili ekstra özelliklere sahiptir. Amacı, MP3'ü geçmek ve ses sıkıştırmada yeni standart haline gelmektir. Birçok yönden MP3'e çok yakındır, ancak aynı veya daha küçük dosya boyutunda daha iyi kaliteye sahip olması için geliştirilmiştir. M4B formatı ilk olarak Apple tarafından tanıtıldı. Biçim türü de Apple kayıpsız Kodlayıcı (ALE) olarak gerçekleştirilir.

Bu nedenle, şu anda M4B, ses formatı henüz genel olarak çalınamadığı için MP3'ün ana akım başarısını elde edemedi.

**Mp3**: Herkesin aşina olduğu bir dijital ses formatı. Sahnedeki ilk sıkıştırma formatı ve müzik dinleyicileri arasında çok ünlü oldu. Yaygın başarısı o kadar hızlı ki, dosya türü evrensel olarak oynatılabiliyor ve neredeyse her şeyle, donanım veya yazılımla uyumlu hale geliyor. Genel anlamda, M4A daha iyi ses kalitesi üretecek, ancak çoğu kişi, doğru olsun ya da olmasın, ses farkının karşılaştırılabilir olmadığını ve MP3 dosyalarını M4A dosyalarına dönüştürmeye çalışmanın zaman kaybı olacağını iddia edecek. Son olarak, dönüştürme yalnızca orijinal ses kalitesini kaybetmenize neden olur.

## M4B dosya biçimi belirtimi

[M4A](/tr/audio/m4a/)'ya benzer şekilde, M4B dosyaları da ardışık parçalardan oluşur. Her yığın 8 bayt başlığa sahiptir ve şu şekilde alt bölümlere ayrılmıştır:
- 4 bayt yığın boyutu (big-endian, önce yüksek bayt)
- 4 bayt yığın türü - önceden tanımlanmış imzalardan biri: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "atla", "jP2", "geniş", "yükle", "imap", "mat", "çap", "kmat", "klip", "crgn", "sync", "tmcd", "PICT "," scpt", "ssrc".

M4A'ya benzer şekilde, M4B'deki İlk öbek "ftype" tipinde olacaktır ve ofset 8'de bir alt tipe sahiptir. M4B, "M4B_" olması gereken alt tip tarafından tanımlanır.

Parçalar, bilinmeyen türde bir yığın algılanana kadar yinelenir, M4B (MPEG-4 Audio) dosyası oluşturur.

## Referanslar

* [MPEG-4 Bölüm 14 - Wikipedia'dan](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Kısım 14 Ses (M4A,M4B,M4P) Formatı ve Kurtarma Örneği](https://www.file-recovery.com/m4a-signature-format.htm)

