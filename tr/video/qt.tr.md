{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QT Dosya Biçimi - Hızlı Film Dosyası",
  "keywords" :[ "QT", "QuickTime video", "qt formatı", "qt dosyaları nasıl oynatılır", "Hızlı Film Dosyası", "QTFF", "video", "Apple" ],
  "description":"QT dosya formatı ve QT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## .qt dosyası nedir?

.qt uzantılı bir dosya, QuickTime çerçevesi tarafından multimedya dosya içeriklerini depolamak için kullanılan bir multimedya kapsayıcı dosyasıdır. Apple Inc. tarafından geliştirilen QuickTime Dosya Biçimi (QTFF), daha sonra oynatmak üzere ses, video veya metin içeren bir multimedya kapsayıcı dosyasıdır. Cihazlar, uygulamalar ve işletim sistemleri arasında dijital ortam alışverişi için tercih edilen biçimdir. QT dosyaları ayrıca Apple Inc. tarafından geliştirilen [MOV](/tr/video/mov/) biçiminde kaydedilir. QT dosyalarını açabilen uygulamalardan bazıları arasında Apple QuickTime player, VLC media player ve K- ile Media Player Classic bulunur. Basit Codec Paketi.

## QT Dosya Biçimi

QTFF, ayrıştırma ve genişletme kolaylığı için esnek bir nesne koleksiyonunu ortaya çıkaran nesne yönelimlidir. Bir QT dosyasındaki her iz, dijital olarak kodlanmış bir medya akışı veya başka bir dosyada bulunan medya akışına bir veri referansı içerir. Atom adı verilen nesnelerden oluşan hiyerarşik veri yapısı, izleme kapları görevi görür. [QT dosya formatı](https://developer.apple.com/documentation/quicktime-file-format) için dosya formatı belirtimleri, geliştiricinin referansı için Apple Inc tarafından resmi olarak mevcuttur.

### Medya açıklaması

Bir QuickTime dosyasının ortam açıklaması, ortam verilerinden ayrı olarak depolanır. Parça sayısı, video sıkıştırma formatı ve zamanlama bilgisi gibi bilgiler ortam açıklamasında saklanır (film kaynağı, film atomu veya kısaca film olarak da bilinir). Medya verilerine, bu medya yapısındaki bir dizin tarafından başvurulur. Medya verileri, filmde kullanılan video kareleri ve ses örnekleri gibi gerçek örnek verilerdir.

### atomlar

Atom, QuickTime dosyasının temel birimidir. Herhangi bir atomda diğer alanlardan önce iki ana alan vardır: Boyut ve Tür alanları. Size alanı atomun boyutunu gösterirken type alanı atomda depolanan verinin türünü gösterir. Doğaları gereği, atomlar hiyerarşiktir, bu da bir atomun başka atomları içerebilen diğer atomları içerebileceği anlamına gelir. Örnek bir atomun düzeni aşağıdaki resimde gösterilmektedir.

Her atomun iki bölümü vardır, başlık ve veri. Başlık, boyut ve tür alanlarını içerir ve veri kısmı, gerçek verileri içerir. Ayrıca, her alan aşağıda açıklanmıştır:

#### Atom Boyutu

Atomun başlığı ve içeriği, atomun boyutu olarak bilinen 32 bitlik bir tamsayı ile gösterilir. Boyut alanı, atomun boyutunu 32 bitlik işaretsiz bir tamsayı olarak ifade edilen bayt cinsinden içerir.

#### Atom Türü

Atomun türü ayrıca, bir film atomu için 'moov' (0x6D6F6F76) veya 'trak' (0x7472616B) gibi, çoğunlukla knemonik değeri olan dört karakterli bir alan olarak ele alınan 32 bitlik bir tamsayı ile gösterilir. bir iz atomu. Atom tipi bilindiğinde, verilerinin yorumlanmasına izin verir.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Dosya Yapısı ##

QT/MOV dosyaları ardışık parçalardan oluşur. Her parçanın 8 baytlık bir başlığı vardır: 4 baytlık yığın boyutu (önce big-endian, yüksek bayt) ve 4 baytlık yığın türü - önceden tanımlanmış imzalardan biri: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "ücretsiz", "atla", "jP2", "geniş", "yük", "ctab", "imap", "mat", "kmat", "klip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". İlk öbek "ftype" türündedir ve 8 uzaklığında bir alt türü vardır. MOV, "qt " olması gereken alt tür tarafından tanımlanır. MOV dosyasını oluşturmak için, bilinmeyen tür algılanana kadar parçaların yinelenmesi gerekir.

İşte örnek bir örnek: Örnek bir MOV dosyasının ikili verilerini incelerken, QuickTime Kapsayıcı Dosya Türünü tanımlayan 4. ofsette **ftyp** (hex: 66 74 79 70) imzasıyla başladığı açıktır. Dosya alt tipi **qt~_~_** (hex: 71 74 20 20) şeklindedir ve MOV dosya tipine işaret eder. İlk blok boyutu 32'dir (hex: 00 00 00 20, big-endian, high byte first), boyut ofset 0'da yer alır. Offset 32'de (hex: 20), 8 boyutuna sahip ikinci yığın bulunur ve **mdat** yazın (onaltılık: 6D 64 61 74).

Bir sonraki öbek 32+8#40 (onaltılık: 28) konumunda bulunur ve 3.263.028 (onaltılık: 00 31 CA 34) boyutuna sahiptir ve 44 (onaltılık) konumunda **mdat** (hex: 6D 64 61 74) yazın : 2C). Bir sonraki parça ofset 40 + 3,263,028#3,263,068 (onaltılık: 00 31 CA 5C) konumunda bulunur ve 21,189 (onaltılık: 00 00 52 C5) boyutuna sahiptir ve ofset konumunda **moov** (hex: 6D 6F 6F 76) yazın 1.836.019.574 (onaltılık: 00 31 CA 60). Bu son parçadır, dolayısıyla toplam dosya boyutu 3.263.068+21.189#3.284.257 bayttır.

## Referanslar ##

* [QT Dosya Biçimi - Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)
* [QuickTime Dosya Biçimi - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

