{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Torrent Dosya Biçimi - BitTorrent Dosyası",
  "description":"TORRENT dosyaları ve TORRENT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## TORRENT dosyası nedir?

TORRENT dosyası, BitTorrent ve diğer P2P (eşler arası) programlar tarafından içerik indirmek ve değiş tokuş etmek için kullanılan bir metin dosyasıdır. İndirilebilir içerik, internette bulunan belgeleri, videoları, oyunları, filmleri ve diğer ortamları içerebilir. İndirilecek ortamın içeriği ve konumu hakkında meta veri bilgilerini içerir. BitTorrent gibi yazılımlar, verileri indirmek için bu dosyadaki ad, dosya boyutu ve klasör yapısı gibi bilgileri kullanır. Torrent dosyaları çevrimiçi olarak [PDF](/tr/pdf/) gibi diğer dosya biçimlerine dönüştürülebilir.

## Torrent nedir? Veri Alışverişi için TORRENT Dosya Formatı

Torrenting, BitTorrent ağını kullanarak veri dosyalarının değiş tokuşu (indirme ve yükleme) kavramıdır. Verilerin başkalarının erişmesi ve indirmesi için yüklendiği geleneksel sunucuların aksine, torrent dosyaları torrent ağı kullanılarak alınır ve gönderilir. Bir kullanıcı BitTorrent gibi uygulamalarda bir .torrent dosyasını açtığında, yazılım dosyanın içeriğini bit bazında indirmeye başlar. Birden fazla kullanıcı aynı dosyaya sahipse, BitTorrent indirme işlemini hızlandırmak için indirmeleri tüm kullanıcılar arasında böler. Aynı zamanda dosyayı indiren kullanıcının bilgisayarı, aynı dosyayı indiren diğer kullanıcılara göndermek için dosyanın kaynağı olur.

### TORRENT Dosyasının Yapısı

Bir torrent dosyası, indirilecek dosyanın tüm parçaları hakkında bir dosya listesi ve meta veri bilgilerinin birleşimidir. Anahtar şeklinde aşağıdaki bilgileri içerir.

- `announce` — Dosyanın kullanılabilirliği hakkında bilgi vermek için diğer eşlere duyurulan izleyicinin URL'si
- "bilgi" — Bu, anahtarları bir veya daha fazla dosyanın paylaşılıp paylaşılmadığına bağlı olan bir sözlüğe eşlenir:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `uzunluk` — dosyanın bayt cinsinden boyutu.
- "yol" — sonuncusu gerçek dosya adı olan alt dizin adlarına karşılık gelen dizelerin bir listesi
- `uzunluk` — dosyanın bayt cinsinden boyutu (yalnızca bir dosya paylaşılırken)
- `ad` — dosyanın kaydedileceği dosya adı
- "parça uzunluğu" — parça başına bayt sayısı. Bu genellikle 28 KiB = 256 KiB = 262.144 B'dir.
- "parçalar" — her bir parçanın SHA-1 karmasının bir birleşimi olan bir karma listesi.

## Torrent Güvenli ve Yasal mı?

P2P kullanıcıları arasında veri alışverişi için torrent protokolü, herhangi bir dosya türünü paylaşmanın tek yolu olduğu için güvenlidir. Bu nedenle, protokolün kendisi güvensiz veya yasa dışı değildir. Ancak ağ üzerinden paylaşılan içerikler, paylaşılan belgelerin yasal statüsünü ihlal edebilecek dosyalar veya ortamlar içerebilir. Böyle bir durumda, bu tür verilerin değişimi, bu tür dosyaların alenen paylaşılmasına dahil olan taraflara karşı yasal işlemlere neden olabilir.

## Referanslar

* [TORRENT Dosyası - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)

