{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKV Dosya Biçimi",
  "keywords" :[ "mkv", "matroska video", "mkv formatı", "mkv dosyaları nasıl oynatılır", "video", "dosya", "format"],
  "description":"MKV dosya formatı ve MKV dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## MKV Dosyası Nedir? ##

MKV (Matroska Video), [MOV](/tr/video/mov/) ve [AVI](/tr/video/avi/) biçimine benzer bir multimedya kabıdır ancak aynı dosyada birden fazla ses ve altyazı parçasını destekler. Bir MKV dosyası, video için kullanılan Matroska multimedya kapsayıcı biçimidir. MKV, Genişletilebilir İkili Meta Dilini temel alır ve çeşitli video ve ses sıkıştırma formatlarını destekler. MKV ve diğer video formatları arasındaki en büyük fark, MKV'nin bir codec değil, bir konteyner olmasıdır. MKV dosyaları .mkv dosya uzantısıyla kaydedilir. MKV, ses, video ve altyazıları, bu öğeler farklı türde kodlama kullansa bile tek bir dosyada birleştirebilir. Örneğin, ses için H.264 video ve MP3 veya AAC içeren bir MKV dosyanız olabilir. MKV ayrıca açıklamaları, derecelendirmeleri, kapak resmini ve hatta bölüm noktalarını destekler. MKV'nin geleceğe hazır olmasının birkaç temel özelliği vardır. Bu özellikler şunları içerir:

- Hızlı arama desteği.
- Farklı ses ve video akışlarını seçebilme.
- Altyazı desteği (sabit kodlanmış ve yumuşak kodlanmış).
- Meta veriler, bölümler ve menüler için destek.
- Çevrimiçi akış yeteneği.
- Bozuk dosyaları oynatma yeteneği sağlayan hatalı dosyaları kurtarma yeteneği.

## Kısa Tarih ##

MKV dosyası 2002 yılında Rusya'da ortaya çıkmıştır. Baş geliştirici, Matroska'nın kurucusu Steve Lhomme ve bir programcı ekibiyle çalışan Lasse Kärkkäinen'di. MKV, açık standartlar projesi olarak geliştirildi, yani açık kaynaklı ve kullanımı ücretsiz. Zaman geçtikçe format geliştirildi ve 2010 yılında WebM multimedya formatının temeli oldu.

## Matroska Tasarım ##

Matroska, EBML spesifikasyonuna aşağıdaki kısıtlamaları ekler.

- **EBML Başlığı**'nın **docType**'ı 'matroska' olmalıdır.
- **EBML Başlığı**'nın **EBMLMaxIDLength** değeri 4 olmalıdır.
- **EBML Başlığı**'nın **EBMLMaxSizeLength** değeri 1 ile 8 (dahil) arasında olmalıdır.

Tüm üst düzey öğeler 4 sekizli olarak kodlanmıştır.

- Dil kodları: Matroska (sürüm 1'den 3'e kadar), 3 harfli bibliyografik ISO-639-2 formu (fransızca için "fre" gibi) veya "fre-ca" gibi ek ülke kodu kullanılabilen dil kodları kullandı " Kanada Fransızcası için. Matroska sürüm 4'ten başlayarak, dil kodları için ISO 639-2 veya BCP 47 KULLANILABİLİR, ancak BCP 47 tavsiye edilir.
- Fiziksel Türler: Bunlar hem ses hem de video dosyaları için farklı anlamlara sahiptir. Örneğin, ChapterPhysicalEquiv = 60, ses için (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) ve video için (DVD / VHS / LASERDISC) anlamına gelir.
- Blok Yapısı - Blok Başlığı: Blok başlığı, parça numarası, zaman damgaları, bağlama türü vb. ile ilgili bilgileri içerir.
- Bağlama: Genellikle küçük veri blokları (çerçeveler) için kullanılan verileri depolarken yerden tasarruf sağlayan bir mekanizmadır. 3 çeşit bağlama vardır:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- SimpleBlock Yapısı: **Blok yapısından** esinlenilmiştir, temel fark **Keyframe** ve **Discardable** bayraklarının eklenmesidir. Bunun dışında her şey aynı.

## Matroska Yapısı ##

Bir Matroska belgesi, **Matroska Belge Türü** kullanılarak en az bir **EBML Belgesinden** oluşmalıdır. Her **EBML Belgesi** bir **EBML Başlığı** ile başlamalı ve bunu bir Segment olarak tanımlanan **EBML Kök Öğesi** takip etmelidir. Matroska, **Segment** içinde oluşabilecek birkaç Üst Düzey Öğeyi tanımlar.

EBML, bir EBML Belgesi oluşturmak için bir Öğeler sistemi kullanır. Matroska dosyasındaki Üst Düzey öğelerin listesi aşağıdadır:

- **EBML Belgesi**: Dosyanın tamamı için sarmalayıcı.
- **EBML Header**: DocType gibi dosyanın başlık bilgisini içerir.
- **Segment**: Diğer tüm üst düzey öğeleri içeren üst öğe.
- **SeekHead**: Diğer Üst Düzey Öğelerin Segmentlerinin konumunu içerir.
- **Bilgi**: Segment ile ilgili genel bilgileri içerir.
- **Parçalar**: Birçok parçanın tanımlandığı Üst Düzey Bilgi Unsuru.
- **Bölümler**: Temel menüleri ve bölüm verilerini tanımlamak için kullanılır.
- **Küme**: Blok yapısını içeren Üst Düzey Öğe.
- **İpuçları**: Erişimi hızlandıran Segmente yerel tüm girişleri içeren bir Üst Düzey Öğe.
- **Ekler**: Bu, ekli dosyaları içerir.
- **Etiketler**: Bu öğe, Parçaları, Sürümleri, Bölümleri, Ekleri veya Segmenti bir bütün olarak açıklayan meta verileri içerir.

Aşağıdaki tablo, çoğu öğenin bir hiyerarşide görüntülendiği Matroska belgesinin yapısını göstermektedir:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| EBML Başlığı | | | |
| Segment | Arama Kafası| ara | Arama Kimliği |
| | | | Pozisyon Ara |
| | bilgi | SegmentUID | |
| | | SegmentDosya Adı | |
| | | ÖncekiUID | |
| | | ÖncekiDosyaadı | |
| | | SonrakiUID | |
| | | SonrakiDosya adı | |
| | | SegmentAilesi | |
| | | BölümÇeviri | |
| | | Zaman Damgası Ölçeği | |
| | | Süre | |
| | | TarihUTC | |
| | | Başlık | |
| | | MuxingUygulaması | |
| | | YazmaUygulaması | |
| | Parçalar | İzleme Girişi | Parça Numarası |
| | | | TrackUID |
| | | | İzleme Türü |
| | | | İsim |
| | | | Dil |
| | | | Codec Kimliği |
| | | | Codec Özel |
| | | | CodecAdı |
| | | | Video | BayrakGeçişmeli |
| | | | | Alan Sırası |
| | | | | StereoMod |
| | | | | Alfa Modu |
| | | | | Piksel Genişliği |
| | | | | Piksel Yüksekliği |
| | | | | Ekran Genişliği |
| | | | | Ekran Yüksekliği |
| | | | | AspectRatioType |
| | | | | Renk |
| | | | Ses | Örnekleme Frekansı |
| | | | | Kanallar |
| | | | | Bit Derinliği |
| | Bölümler | Sürüm Girişi | EditionUID |
| | | | EditionFlagGizli |
| | | | EditionFlagDefault |
| | | | EditionFlagOrdered |
| | | | BölümAtom | Bölüm Kullanıcı Kimliği |
| | | | | ChapterStringUID |
| | | | | BölümZamanıBaşlangıç |
| | | | | BölümZamanSonu |
| | | | | BölümFlagGizli |
| | | | | Bölüm Gösterimi | Bölüm Dizisi |
| | | | | | Bölüm Dili |
| | Küme | Zaman Damgası |
| | | SilentTracks |
| | | pozisyon |
| | | ÖncekiBoyut |
| | | Basit Blok |
| | | Blok Grubu |
| | | ŞifreliBlok |
| | ipuçları | İşaret Noktası | İşaret Zamanı |
| | | | CueTrackPozisyonlar |
| | Ekler | EkliDosya | Dosya Açıklaması |
| | | | DosyaAdı |
| | | | DosyaMimeTürü |
| | | | Dosya Kullanıcı Kimliği |
| | | | Dosya Yönlendirmesi |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Etiketler | Etiket | hedefler | HedefTürüDeğeri |
| | | | | HedefTürü |
| | | | | TagTrackUID |
| | | | | Etiket Sürümü Kullanıcı Kimliği |
| | | | | EtiketBölümüUID |
| | | | | EtiketEklentisiUID |
| | | | BasitEtiket | EtiketAdı |
| | | | | Etiket Dili |
| | | | | Varsayılan Etiket |
| | | | | etiket dizisi |
| | | | | EtiketBinary |
| | | | | BasitEtiket |


### Codec'leri Kullanma ###

Yeni bir medya oynatıcı istemiyor ve mevcut oynatıcınızı kullanmayı tercih ediyorsanız, bazı codec bileşenleri (sıkıştırma/açma kısaltması) yüklemeniz gerekecektir. Codec'leri indirmek geçerli bir seçenek olsa da, kaynak konusunda dikkatli olmalısınız ve bunlar kötü amaçlı yazılım içerebilir.

## Referanslar ##

- [Wikipedia'dan Matroska](https://en.wikipedia.org/wiki/Matroska)

