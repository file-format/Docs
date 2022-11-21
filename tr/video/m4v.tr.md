{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "dosya", "uzantı", "biçim", "MPEG-4", "Dijital Haklar Yönetimi", "DRM", "Apple", "video"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"M4V dosya formatı ve M4V dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## M4V dosyası nedir?

Apple tarafından geliştirilen **M4V** dosya biçimi, gizliliği veya kopyalamayı korumak için Dijital Haklar Yönetimi (DRM) kopya korumasıyla isteğe bağlı olarak korunan bir video kapsayıcısıdır. Videolar ve ses parçaları, oynatma akışlarını dizine eklemek ve düzenlemek için kap dosyaları tarafından sarılır. Ek olarak, konteynerler ayrıca DVD'lerdekine benzer bölümler özelliği sağlar. Apple, iTunes Store'daki videoları kodlamak için M4V kullanır. M4V dosyalarının yalnızca videoyu satın almak için kullanılan hesaplara sahip yetkili bilgisayarlarda oynatılmasına izin vererek, Apple'ın FairPlay kopya koruması aracılığıyla yetkisiz çoğaltmayı korur. Ancak, M4V dosyalarından DRM koruması kaldırılırsa, bu dosyalar .m4v'den .mp4'e uzantı değiştirilerek diğer video oynatıcılarda oynatılabilir, bu nedenle M4V dosyaları MPEG-4 ile ilişkilendirilir. M4V, video için H.264 ve ses kodlama ve kod çözme için **[AAC](/tr/audio/aac/)** ve Dolby Digital kullanır.

## M4V Dosya Yapısı ##

M4V dosyaları, her yığında 8 bayt başlık, 4 bayt yığın boyutu ve 4 bayt yığın türü ile sürekli parçalara sahiptir. İlk öbek "ftype" ve ofset 8'de bir alt tipe sahip. M4V, "M4V_" olması gereken alt tip tarafından tanımlanıyor. Diğer yığın türleri önceden tanımlanmış imzalardır: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "geniş" , "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " PİK". Bilinmeyen tür tespit edilene kadar yığınları yineleyerek, M4V dosyasını oluşturuyoruz.

İşte bir örneğin incelenmesi: Örnek bir m4v dosyasının ikili verileri Hex Viewer aracılığıyla incelenir ve QuickTime'ı tanımlayan 4. ofsette **ftyp** (hex: 66 74 79 70) imzasıyla başladığı gözlemlenebilir. Konteyner Dosya Türü. Dosya alt tipi, M4V (MPEG-4) dosya tipine işaret eden **M4V_** (hex: 4D 34 56 20) şeklindedir. İlk blok boyutu 32'dir (hex: 00 00 00 20, big-endian, high byte first), boyut ofset 0'da yer alır. Offset 32'de (hex: 20), 30.322 (hex) boyuta sahip ikinci yığın bulunur : 00 00 76 72, big-endian, önce alt bayt) ve **moov** (hex: 6D 6F 6F 76) yazın. Bir sonraki öbek ofset 32+30,322#30,354 (onaltılık: 00 00 76 92) konumunda bulunur ve 8 boyutuna (onaltılık: 00 00 00 08) sahiptir ve **ücretsiz** (onaltılık: 66 72 65 65) yazın.
### M4V'de Kullanılan Codec'ler ###

#### Video Kodlayıcı H.264 ####

H.264, dijital videoyu gerekli iletim veya depolama sırasında daha az alan gerektiren bir biçime dönüştüren bir video sıkıştırma standardıdır. M4V, video sıkıştırma için H.264 kullanır. Uygulaması DVD, TV, Video konferans ve internet üzerinden video akışı arasında değişir. H.264 iki ana bölümden oluşur: Kodlayıcı – Videoyu sıkıştırır, Kod Çözücü – Sıkıştırılmış videoyu geri açar. Aşağıdaki şekilde, kodlama ve kod çözme işlemleri vurgulanmış ve diğer işlemler H.264 standardında ele alınmıştır.

##### H.264'te Video Kodlama ve Kod Çözme İşlemi #####

Sıkıştırılmış H.264 bit akışı için video kodlayıcı tahmin, dönüştürme ve kodlama sürecini yürütür. Aynı zamanda, kod çözücü, video dosyasını geri üretmek için ters kod çözme, ters dönüştürme ve yeniden oluşturma işlemlerini gerçekleştirir. H.264, MPEG'in yarısını alır.

#### Ses Codec'i ####

Advanced Audio Coding (AAC), kayıplı dijital ses sıkıştırma için bir ses codec bileşenidir ve bir M4V kapsayıcısında kullanılır. AAC, [MP3](/tr/audio/mp3/) formatının halefidir ve aynı bit hızında MP3'ten daha iyi kalite sağlar. AAC biçimi, sıkıştırma işlemi sırasında daha az önemli olan bazı bilgileri atar. AAC, her bloğun 1024 zaman alanı örneğine kod çözdüğü, değişken bit hızı (VBR) blok tabanlı bir codec bileşenidir.

### Referanslar ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipedia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

