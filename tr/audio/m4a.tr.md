{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "dosya", "uzantı", "biçim", "m4a dosya biçimi nedir", "müzik", "m4a dosya biçimi", "M4A ve MP3", "m4a dosya biçimi belirtimi "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"M4A dosya formatı ve M4A dosyalarını oluşturabilen, dönüştürebilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"M4A - MPEG-4 Ses Dosyası",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## M4A dosyası nedir?

**M4A dosya biçimi**, kayıplı sıkıştırma olarak bilinen AAC (Gelişmiş Ses Kodlaması) kullanılarak oluşturulmuş bir ses dosyasıdır. M4A kelimesi MPEG 4 Audio olarak kısaltılmıştır. Bu ses dosyaları genellikle .m4a dosya uzantısına sahiptir. Bu, özellikle korumasız içerik için geçerlidir. Sesli kitaplar, şarkılar ve podcast'ler gibi çeşitli ses içeriği türlerini depolayabilir. M4A genellikle, tipik olarak yalnızca ses için tasarlanmamış olan MP3'ten daha gelişmiş bir biçim olarak gerçekleştirilir. MPEG 1 veya 2 video dosyalarında sadece bir ses katmanıdır.

M4A formatı, iTunes Store aracılığıyla satılan .m4p uzantısını kullandığından, FairPlay Dijital Haklar Yönetimi tarafından şifrelenir. Apple iPhone'lar zil sesleri için MPEG-4 sesi kullanır, ancak bu ses dosyaları .m4r uzantısını kullanır.


## M4A ve MP3

Hem M4A hem de [MP3](https://docs.fileformat.com/audio/mp3/) yalnızca ses dosya biçimleridir.

**M4A**: Aynı bit hızında kodlandığında kalite ve boyutlar açısından MP3'ten daha iyidir. .m4a dosya uzantısı çok yaygındır çünkü Apple tarafından iTunes Music Store'da kullanılmak üzere kullanılmıştır. M4A, MPEG-4 teknolojisi kullanılarak sıkıştırılmış bir ses dosyasıdır; kayıplı sıkıştırma için bir algoritma. Temel olarak “MPEG-4 Ses Katmanı” ile ilişkilendirilir, .m4a uzantılı dosyalar MPEG-4 filmlerin ses katmanıdır. MP3'ü geçmesi ve ses sıkıştırmada yeni standart olması amaçlanmıştır. Birçok yönden MP3'e çok yakındır, ancak aynı veya daha küçük dosya boyutunda daha iyi bir kaliteye sahip olması için sunulmuştur. M4A formatı ilk olarak Apple tarafından tanıtıldı. Biçim türü de Apple kayıpsız Kodlayıcı (ALE) olarak gerçekleştirilir.

Bu nedenle, şu anda M4A, ses formatı henüz genel olarak çalınamadığı için MP3'ün ana akım başarısını elde edemedi. Bir şekilde yalnızca MacOS, iPod ve diğer Apple ürünleriyle sınırlıdır.

**Mp3**: En ünlü dijital ses formatı. Aynı zamanda sahnedeki ilk sıkıştırma formatlarından biriydi ve müzikseverler arasında çok popüler oldu. Yaygın başarısı o kadar hızlıdır ki, dosya türü evrensel olarak ve neredeyse her şeyle, donanım veya yazılımla oynatılabilir. Genel anlamda, M4A daha iyi ses kalitesi üretecek, ancak birçok kişi, doğru olsun ya da olmasın, ses farkının ayırt edilemez olduğunu ve MP3 dosyalarını M4A dosyalarına dönüştürmeye çalışmanın zaman kaybı olacağını iddia edecek. Sonunda, dönüştürme yalnızca orijinal ses kalitesini kaybetmenize neden olur.

## M4A dosya biçimi belirtimi

M4A dosyaları ardışık parçalardan oluşur. Her yığın 8 bayt başlığa sahiptir ve şu şekilde alt bölümlere ayrılmıştır:
- 4 bayt yığın boyutu (big-endian, önce yüksek bayt)
- 4 bayt yığın türü - önceden tanımlanmış imzalardan biri: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "geniş", "yük", "ctab", "imap", "mat", "kmat", "klip", "crgn", "sync", "chap", "tmcd", "scpt "," ssrc", "PICT".

İlk yığın "ftype" türünde olacak ve 8 ofsetinde bir alt türe sahip olacak. "M4A_" olması gereken alt tür tarafından tanımlanan M4A, M4B alt türü için "M4B_" ve M4P alt türü için "M4B_" olmalıdır "M4P_" olsun.

Parçalar, bilinmeyen türde bir yığın algılanana kadar yinelenir, M4A (MPEG-4 Audio) dosyası oluşturur.

## Referanslar ##

* [MPEG-4 Bölüm 14 - Wikipedia'dan](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Kısım 14 Ses (M4A,M4B,M4P) Biçimi ve Kurtarma Örneği](https://www.file-recovery.com/m4a-signature-format.htm)

