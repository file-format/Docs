{
  "date" : "2019-10-11",
  "keywords" :[ "mov dosyası", "mov dosya biçimi", "mov dosyası nedir", "dosya", "mov örneği", "mov dosya uzantısı","uzantı", "biçim", "QuickTime", "MPEG- 4"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MOV Dosyası - Apple QuickTime Film Dosyası Formatı",
  "description":"MOV dosya formatı ve MOV dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## MOV dosyası nedir?

MOV dosyası, Apple Inc. tarafından geliştirilen ve bir veya daha fazla parça içeren bir video dosyası türüdür. Her parça bir film, ses, film klipleri ve altyazıları saklar. Farklı türde medya öğelerini depolayabilen bir multimedya kabıdır. MOV video formatı hem Windows hem de Macintosh sistemleriyle uyumludur. Sıkıştırma için MPEG-4 kodlu kullanır ve izler, hiyerarşik bir veri yapısına yerleştirilmiş atom adı verilen nesnelerde tutulur.

## MOV Dosya Formatının Kısa Tarihi

MPEG-4 dosya formatı, 2001'de QuickTime Dosya Formatı (**QTFF**) spesifikasyonundan geliştirilmiştir. Uluslararası Standardizasyon Örgütü formatı onayladı ve MPEG-4 Bölüm 1 sistem spesifikasyonları 1999'da yayınlandı. 2001'de bir revizyon dosyası [MP4](/tr/video/mp4/) biçimi yayınlandı.

MP4'ün ilk versiyonu 2003 yılında MPEG-4 Part 14 (ISO/IEC 14496-14:2003) olarak revize edilmiştir. 2004 yılında MP4, tüm zamana dayalı medya dosyaları için genel bir yapı tanımlamak üzere genelleştirildi. Bu nedenle, şimdi diğer çeşitli multimedya dosya biçimleri için bir temel olarak kullanılmaktadır.

## QuickTime Dosya Biçimi (QTFF) - Daha Fazla Bilgi

Dijital multimedya ile çalışmak için QTFF birçok türde veriyi tutabilir. Format, her türlü medya yapısını tanımlama standartlarını tanımladığından, dijital medya alışverişi için bir fikir formatıdır. Dosya biçimi, nesne yönelimli nesnelerin esnek bir koleksiyonundan oluşur. QuickTime, filmlerin disklerde depolanması için iki yapı kullanır, yani "atomlar" ve "QT atomları".

### atomlar

Atom, QuickTime dosyasının temel birimidir. Herhangi bir atomda diğer alanlardan önce iki ana alan vardır: Boyut ve Tür alanları. Size alanı atomun boyutunu gösterirken type alanı atomda depolanan verinin türünü gösterir. Doğaları gereği, atomlar hiyerarşiktir, bu da bir atomun başka atomları içerebilen diğer atomları içerebileceği anlamına gelir. Örnek bir atomun düzeni aşağıdaki resimde gösterilmektedir.

Her atomun "başlık" ve "veri" olmak üzere iki bölümü vardır. Başlık, boyut ve tür alanlarını içerir ve veri kısmı, gerçek verileri içerir. Ayrıca, her alan aşağıda açıklanmıştır:

### Atom Boyutu

Atomun başlığı ve içeriği, atomun boyutu olarak bilinen 32 bitlik bir tamsayı ile gösterilir. Boyut alanı, atomun boyutunu 32 bitlik işaretsiz bir tamsayı olarak ifade edilen bayt cinsinden içerir.

### Atom Türü

Atomun türü ayrıca, bir film atomu için 'moov' (0x6D6F6F76) veya 'trak' (0x7472616B) gibi, çoğunlukla knemonik değeri olan dört karakterli bir alan olarak ele alınan 32 bitlik bir tamsayı ile gösterilir. bir iz atomu. Atom tipi bilindiğinde, verilerinin yorumlanmasına izin verir.

### QT Atomları ve Atom Konteynerleri

QT atomları, genel amaçlı bir depolama biçimi sağlar ve Boyut, Tür, Atom Kimliği ve Alt atom sayısı alanlarından oluşan genişletilmiş bir başlığa sahiptir. QT atomları, kilit sayısına sahip bir başlığa sahip benzersiz bir veri yapısı olan bir atom kabına sarılır. QT atomu olan her atom kabında bir kök atom vardır. QT atomunun düzeni aşağıdaki şekilde gösterilmektedir.

QT atom konteyner başlığı aşağıdaki verilere sahiptir:

Ayrılmış: 0 değerine sahip 10 baytlık bir öğe.

Kilit Sayısı: 0 değerine sahip 16 bitlik tamsayı.

QT atom başlıkları aşağıdaki verilere sahiptir:

**Boyut -** QT atom başlığı ve içeriği, 32 bitlik bir tamsayı ile bayt cinsinden belirtilir. Bir yaprak atomu söz konusu olduğunda, bu alan tek bir atomun boyutunu içerir.

**Tip -** Atomun türü 32 bitlik bir tamsayı ile gösterilir. Kök atom olması durumunda, değer 'sean' olarak ayarlanır.

**Atom Kimliği -** Atom kimliğini gösteren ve tüm kardeşler için benzersiz olması gereken 32 bitlik bir tam sayıdır. Kök atom her zaman atom kimliğinin değeri 1'dir.

**Ayrılmış -** 0 olarak ayarlanması gereken 16 bitlik bir tamsayı.

**Çocuk sayısı -** Bir atomun alt atomlarının sayısını gösteren 16 bitlik bir tam sayı.

**Ayrılmış -** 0 olarak ayarlanması gereken 32 bitlik bir tam sayı.

## MOV Dosyalarının Dosya Yapısı

MOV dosyaları ardışık parçalardan oluşur. Her parçanın 8 baytlık bir başlığı vardır: 4 baytlık yığın boyutu (önce big-endian, yüksek bayt) ve 4 baytlık yığın türü - önceden tanımlanmış imzalardan biri: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "ücretsiz", "atla", "jP2", "geniş", "yük", "ctab", "imap", "mat", "kmat", "klip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". İlk öbek "ftype" türündedir ve 8 uzaklığında bir alt türü vardır. MOV, "qt " olması gereken alt tür tarafından tanımlanır. MOV dosyasını oluşturmak için, bilinmeyen tür algılanana kadar parçaların yinelenmesi gerekir.

İşte bir "örnek örnek": Örnek bir MOV dosyasının ikili verilerini incelerken, QuickTime Kapsayıcı Dosya Türünü tanımlayan 4. ofsette **ftyp** (hex: 66 74 79 70) imzasıyla başladığı açıktır. Dosya alt tipi **qt~_~_** (hex: 71 74 20 20) şeklindedir ve MOV dosya tipine işaret eder. İlk blok boyutu 32'dir (hex: 00 00 00 20, big-endian, high byte first), boyut ofset 0'da yer alır. Offset 32'de (hex: 20), 8 boyutuna sahip ikinci yığın bulunur ve **mdat** yazın (onaltılı: 6D 64 61 74).

Bir sonraki öbek 32+8#40 (onaltılık: 28) konumunda bulunur ve 3.263.028 (onaltılık: 00 31 CA 34) boyutuna sahiptir ve 44 (onaltılık) konumunda **mdat** (hex: 6D 64 61 74) yazın : 2C). Bir sonraki parça ofset 40 + 3,263,028#3,263,068 (onaltılık: 00 31 CA 5C) konumunda bulunur ve 21,189 (onaltılık: 00 00 52 C5) boyutuna sahiptir ve ofset konumunda **moov** (hex: 6D 6F 6F 76) yazın 1.836.019.574 (onaltılık: 00 31 CA 60). Bu son parçadır, dolayısıyla toplam dosya boyutu 3.263.068+21.189#3.284.257 bayttır.

## MOV Dosyası Nasıl Dönüştürülür?

MOV dosyalarını diğer popüler video dosyası formatlarına dönüştürmek için çok sayıda medya oynatıcı ve yazılım video düzenleyicisi bulunmaktadır. MOV dosyalarını diğer formatlara dönüştürebilen medya oynatıcılardan bazıları şunlardır:

* VideoLAN VLC medya oynatıcı
* Eltima Elma Medya Oynatıcı

VideoLAN VLC medya oynatıcı ve Eltima Elmedia Player dahil olmak üzere birçok medya oynatıcı ve video düzenleyici, MOV dosyalarını diğer biçimlere dönüştürebilir. Bu yazılımlar MOV dosyalarını aşağıdaki video formatlarına dönüştürebilir.

* MPEG-4 Video - [MP4](/tr/video/mp4/)
* WebM Videosu - [WEBM](/tr/video/webm/)
* Video Aktarım Akışı - [TS](/tr/video/ts/)
* Gelişmiş Sistem Formatı - [ASF](/tr/video/ts/)
* Ogg Vorbis Sesi - [OGG](/tr/audio/ogg/)
* MP3 Ses - [MP3](/tr/ses/mp3/)
* Ücretsiz Kayıpsız Ses Codec'i - [FLAC](/tr/audio/flac/)
* WAVE Ses - [WAV](/tr/audio/wav/)

## MOV Dosyaları için Açık Kaynak API'si

* [MOV'u MP4'e dönüştürmek için React Native API](https://github.com/taltultc/react-native-mov-to-mp4)
* [MOV Dosyalarını onarmak için Python API'si](https://github.com/nrosenstein-stuff/movrepair)
* [MOV'u GIF'e dönüştürmek için Ruby API](https://github.com/skygroundmedia/convert-mov-to-gif)

## Referanslar

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

