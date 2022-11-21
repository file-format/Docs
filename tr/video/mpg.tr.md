{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPG Dosya Biçimi",
  "keywords" :[ "MPG", "dosya", "uzantı", "format", "video formatı", "mpg dosya formatı nedir", "mpg dosya formatı", "mpg dosya oynatıcısı", "mpeg sıkıştırması", "video ", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"MPG dosya formatı ve oluşturabilen API'ler hakkında bilgi edinin ve MPG dosyalarının nasıl açılacağını gösterin.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## MPG dosya formatı nedir? ##

.mpg uzantılı dosya, MPEG-1 veya MPEG-2 ses ve video sıkıştırma için dosya uzantıları grubuna aittir. MPEG-1 Kısım 2 videosu kolayca bulunmaz ve bu uzantı (MPG dosya formatı) tipik olarak MPEG-1 ve MPEG-2'de tanımlanan bir MPEG program akışına veya MPEG-2'de tanımlanan bir MPEG aktarım akışına işaret eder. . .m2ts gibi doğru kapsayıcıyı, bu durumda MPEG-2 TS'yi belirten başka uzantılar da mevcuttur, ancak bunun MPEG-1 ortamıyla çok az ilgisi vardır. [.mp3](https://docs.fileformat.com/audio/mp3/), MP3 sesi içeren dosyalar için en yaygın uzantıdır. Bir MP3 dosyası, tipik bir ham ses akışıdır; MP3 dosyalarını etiketlemenin geleneksel yolu, akış verilerini her çerçevenin medya bilgilerini kaydeden ancak **mpg dosya oynatıcısı** tarafından atılan "çöp" bölümlerine yazmaktır. Bu, AAC dosyalarını etiketlemek için kullanılan benzer bir tekniktir, ancak günümüzde daha az desteklenmektedir.

## MPEG Sıkıştırma ##

MPEG adı, Moving Pictures Experts Group'un kısaltmasıdır. MPEG, görüntülerin ve seslerin sıkıştırılmasını ve ikisinin senkronizasyonunu içeren bir video sıkıştırma aracıdır.
Şu anda birkaç MPEG standardı vardır.

- MPEG-1, ara veri hızları için 1,5 Mbit/sn mertebesinde önerilir.
- MPEG-2, en az 10 Mbit/sn'lik yüksek veri hızları için önerilir.
- HDTV sıkıştırması için MPEG-3 önerildi, ancak gereksiz olduğu görüldü ve MPEG-2 ile birleştirildi.
- MPEG-4, 64 Kbit/sn'den daha düşük çok düşük veri hızları için önerilmiştir.


## MPG dosya biçiminin program akışı ##

Program akışı, dijital ses, video ve daha fazlasını çoğullamak için bir kapsayıcıdır. Program Akışı formatı, MPEG-1'in 1. bölümünde (ISO/IEC 11172-1) ve MPEG-2, Sistemlerin 1. bölümünde (ISO/IEC standardı 13818-1/ITU-T H.222.0) belirtilmiştir. MPEG-2 Program Akışı analog tabanlıdır ve ISO/IEC 11172 Sistemleri katmanına benzer ve ileri uyumludur.

### Kodlama ayrıntıları ###

Kısmi MPEG-2 Program Akışı paketi başlık biçiminin kodlama ayrıntıları şunlardır:

| Ad | bit sayısı | Açıklama |
---|---|---|
| bayt eşitleme | 32 | 0x000001BA |
| işaret bitleri | 2 | MPEG-2 sürümü için 01b. MPEG-1 sürümü için işaret bitleri, 0010b değerine sahip 4 bittir. |
| Sistem saati [32..30] | 3 | Sistem Saat Referansı (SCR) bitleri 32 - 30 |
| işaretleyici bit | 1 | 1 Bit her zaman ayarlıdır. |
| Sistem saati [29..15] | 15 | Sistem saati bitleri 29 - 15 |
| işaretleyici bit | 1 | 1 Bit her zaman ayarlıdır. |
| Sistem saati [14..0] | 15 | Sistem saati bitleri 14 - 0 |
| işaretleyici bit | 1 | 1 Bit her zaman ayarlıdır. |
| SCR uzantısı | 9 | |
| işaretleyici bit | 1 | 1 Bit her zaman ayarlıdır. |
| bit hızı | 22 | Saniyede 50 baytlık birimlerde. |
| işaret bitleri | 2 | 11 Bit her zaman ayarlıdır. |
| rezerve | 5 | ileride kullanılmak üzere ayrılmıştır |
| doldurma uzunluğu | 3 | |
| bayt doldurma | 8*doldurma uzunluğu | |
| sistem başlığı (isteğe bağlı) | 0 veya daha fazla | sistem başlığı başlangıç kodu şu şekildeyse: 0x000001BB |

Aşağıdaki tablo, kısmi sistem başlık formatını gösterir:

| İsim | bayt sayısı | Açıklama |
---|---|---|
| bayt eşitleme | 4 | 0x000001BB |
| başlık uzunluğu | 2 | |
| oran sınırı ve işaret bitleri | 3 | |
| ses bağlama ve bayraklar | 1 | |
| bayraklar, işaretçi biti ve video bağlama | 1 | |
| Paket hızı kısıtlaması ve ayrılmış bayt | 1 | |


## Referanslar ##

- [MPEG-1 - Vikipedi](https://en.wikipedia.org/wiki/MPEG-1)



