{
  "date" : "2019-12-09",
  "keywords" :[ "zip dosyası", "zip dosyası biçimi", "zip dosyası nedir", "dosya", "zip örneği", "zip dosyası uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIP",
  "description":"ZIP dosyası nedir ve ZIP dosyalarını oluşturabilen ve açabilen API'ler.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## ZIP dosyası nedir? ##

.zip uzantılı bir dosya, bir veya daha fazla dosya veya dizini tutabilen bir arşivdir. ZIP dosyasının boyutunu azaltmak için arşiv, dahil edilen dosyalara sıkıştırma uygulayabilir. ZIP dosya biçimi, dosya ve klasörlerin arşivlenmesini sağlamak için Şubat 1989'da Phil Katz tarafından halka açıldı. Biçim, PKWARE, Inc. tarafından oluşturulan [PKZIP](https://www.pkware.com/pkzip) yardımcı programının bir parçası haline getirildi. [mevcut spesifikasyonların](https://pkware.cachefly.net/) kullanıma sunulmasından hemen sonra webdocs/casestudies/APPNOTE.TXT), Microsoft (Windows 7'den beri), Apple (Mac OS X ) ve diğerleri de dahil olmak üzere birçok şirket ZIP dosya biçimini yazılım yardımcı programlarının bir parçası haline getirdi.

## ZIP Dosya Biçiminin Kısa Tarihi

ZIP dosya biçiminin geçmişi, System Enhancement Associates (SEA) tarafından PKWARE'e ARC yardımcı programını kendi ticari markası ve ürünün görünümü ve kullanıcı arabiriminin telif hakları için izinsiz kullanmaktan dolayı açtığı dava olayına kadar uzanır. Bundan önce Phil Katz, SEA'nın kaynak kodunu yeniden yazmış ve bir ARC çıkarıcı olan PKXARC'yi ve bir dosya sıkıştırıcı olan PKARC'yi MS-DOS tabanlı sistemler için ücretsiz yazılım olarak yayınlamıştı. Davayı kaybeden PKWARE, artık ARC ile ilgili hiçbir şeyi kullanamadı. Burası, PKWARE, Inc.'de PKZIP yardımcı programının bir parçası haline getirilen ZIP adlı yeni bir dosya sıkıştırmasının oluşturulmasının ortaya çıktığı yerdir.

Katz, ZIP dosya formatı belirtimlerini kamuya açık hale getirirken, kendi sıkıştırma ve çıkarma yardımcı programı olan PKZIP üzerindeki mülkiyet haklarını elinde tuttu. ZIP sıkıştırma sistemi, dosyayı sıkıştırmak için 32 bit döngüsel artıklık denetimi ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) algoritması aracılığıyla bir klasördeki dosyaları arşivleyebildi (ve yapabiliyor). boyutlar. ARC'den farklı olarak, .ZIP klasörleri, sıkıştırılmış dosyaları işlemek için gerekli bilgileri tutan, bir kriptografın kod kitabı rolünü oynayan bir dizin dosyası içerir.

## ZIP'de Desteklenen Sıkıştırma Yöntemleri

.ZIP Dosya Biçimi belirtimlerine göre, aşağıdaki sıkıştırma yöntemleri desteklenir.

* Mağaza - sıkıştırma olmadığı anlamına gelir
* Çekmek
* Azaltma (Bu, 1. seviyeden 4. seviyeye kadar değişen sıkıştırma faktörlerini ifade eder)
* Patlama
* Söndür
* Söndür64
* BZIP2
* LZMA (EFS)
* WavPack
* PPMd sürüm I, Rev 1

DEFLATE, LZ77 ve Huffman kodlamasının bir kombinasyonunu kullanan ve [RFC 1951](https://tools.ietf.org/html/rfc1951)'de ayrıntılı olarak açıklanan, kayıpsız bir tarih sıkıştırma algoritması olan yaygın olarak kullanılan bir sıkıştırma yöntemidir.

## ZIP Dosya Biçimi Özellikleri

ZIP dosyaları, farklı sıkıştırma teknikleri kullanarak birden çok dosyayı depolama yeteneğine sahipken, aynı zamanda bir dosyayı herhangi bir sıkıştırma olmadan depolamayı da destekler. Her dosya ayrı ayrı depolanır/sıkıştırılır, bu da tüm arşive sıkıştırma veya açma uygulamadan bunları çıkarmaya veya yenilerini eklemeye yardımcı olur.

### Genel ZIP Dosya Biçimi

Her Zip dosyası aşağıdaki şekilde yapılandırılmıştır:


|ZIP Dosya biçimi
---|
|Yerel Dosya Başlığı 1
|Dosya Verileri 1
|Veri Tanımlayıcı 1
|Yerel Dosya Başlığı 2
|Dosya Verileri 2
|Veri Tanımlayıcı 2
| ....
| ....
|Yerel Dosya Başlığı N
|Dosya Verisi N
|Veri Tanımlayıcı N
|Arşiv Şifre Çözme Başlığı
|Arşiv Ekstra Veri Kaydı
|Merkezi Dizin

ZIP dosya biçimi, arşivleme amacıyla 32 bit CRC algoritması kullanır. Sıkıştırılmış dosyaları işlemek için bir ZIP arşivi, içerdiği dosyaların girişini ve arşiv dosyasındaki konumlarını tutan bir dizin tutar. Bu nedenle, sıkıştırılmış dosyaları işlemek için gerekli bilgileri kapsüllemek için kodlama rolünü oynar. ZIP okuyucuları, tüm ZIP arşivini okumadan dosya listesini yüklemek için dizini kullanır. Biçim, veri kaybına karşı daha fazla koruma sağlamak için dizin yapısının ikili kopyalarını tutar.

Bir ZIP arşivindeki her dosya, her girişin bir Yerel Dosya Başlığından ve ardından sıkıştırılmış dosya verilerinden oluştuğu ayrı bir giriş olarak temsil edilir. Arşivin sonundaki Dizin, tüm bu dosya girişlerine yapılan referansları tutar. ZIP dosyası okuyucuları, yerel dosya başlıklarını okumaktan kaçınmalı ve her türlü dosya listesi Dizinden okunmalıdır. Dosyalar arşivin sonuna doğru da eklenebildiğinden, bu Dizin arşivdeki geçerli dosya girişleri için tek kaynaktır. Bu nedenle, bir okuyucu bir ZIP arşivinin yerel başlıklarını baştan okursa, arşivden silinen Dizinin parçası olmayan geçersiz (silinmiş) girişleri de okuyabilir.

Merkezi dizindeki dosya girişlerinin sırasının, arşivdeki dosya girişlerinin sırası ile çakışması gerekmez.

### ZIP Dosya Girişleri

ZIP dosyasındaki girişler birbiri ardına düzenlenir ve her giriş aşağıdakilerden oluşur:

* Yerel Dosya Başlığı
* İsteğe Bağlı Ekstra Veri Alanları
* Kullanıcı verileri (isteğe bağlı olarak sıkıştırılmış/isteğe bağlı olarak şifrelenmiş)

Her girişin Yerel Dosya Başlığı, yorum, dosya boyutu ve dosya adı gibi dosya hakkındaki bilgileri temsil eder. Ekstra veri alanları (isteğe bağlı), ZIP formatının genişletilebilirlik seçenekleri için bilgileri barındırabilir.

#### Yerel Dosya Başlığı

Yerel Dosya Başlığı, çok baytlık değerlerden oluşan özel alan yapısına sahiptir. Tüm değerler, alan uzunluğunun uzunluğu bayt olarak saydığı küçük-endian bayt düzeninde depolanır. Bir ZIP dosyasındaki tüm yapılar, her dosya girişi için 4 baytlık imzalar kullanır. Merkezi dizin imzasının sonu 0x06054b50'dir ve kendi benzersiz imzası kullanılarak ayırt edilebilir. Yerel Dosya Başlığında depolanan bilgilerin sırası aşağıdadır.


|Ofset|Bayt|Açıklama
---|---|---|
|0|4|Yerel dosya başlığı imzası # 0x04034b50 (biraz endian numarası olarak okunur)
|4|2|Çıkarmak için gereken sürüm (minimum)
|6|2|Genel amaçlı bit işareti
|8|2|Sıkıştırma yöntemi
|10|2|Dosyanın son değiştirilme zamanı
|12|2|Dosyanın son değiştirilme tarihi
|14|4|CRC-32
|18|4|Sıkıştırılmış boyut
|22|4|Sıkıştırılmamış boyut
|26|2|Dosya adı uzunluğu (n)
|28|2|Ek alan uzunluğu (m)
|30|n|Dosya Adı
|30+n|m|Ek Alan

#### Merkezi Dizin Dosya Başlığı


|Ofset|Bayt|Açıklama
---|---|---|
|0|4|Merkezi dizin dosya başlığı imzası # 0x02014b50
|4|2|Yapan sürüm
|6|2|Çıkarmak için gereken sürüm (minimum)
|8|2|Genel amaçlı bit işareti
|10|2|Sıkıştırma yöntemi
|12|2|Dosyanın son değiştirilme zamanı
|14|2|Dosyanın son değiştirilme tarihi
|16|4|CRC-32
|20|4|Sıkıştırılmış boyut
|24|4|Sıkıştırılmamış boyut
|28|2|Dosya adı uzunluğu (n)
|30|2|Ek alan uzunluğu (m)
|32|2|Dosya yorum uzunluğu (k)
|34|2|Dosyanın başladığı disk numarası
|36|2|Dahili dosya öznitelikleri
|38|4|Harici dosya öznitelikleri
|42|4|Yerel dosya başlığının göreli uzaklığı. Bu, dosyanın oluştuğu ilk diskin başlangıcı ile yerel dosya başlığının başlangıcı arasındaki bayt sayısıdır. Bu, ZIP dosyası içindeki dosyanın konumunu bulmak için merkezi dizini okuyan yazılımı sağlar.
|46|n|Dosya adı
|46+n|m|Ek alan
|46+n+m|k|Dosya yorumu

#### Merkezi Dizin Kaydının Sonu


|Ofset|Bayt|Açıklama
---|---|---|
|0|4|Merkezi dizin imzasının sonu # 0x06054b50
|4|2|Bu diskin numarası
|6|2|Merkezi dizinin başladığı disk
|8|2|Bu diskteki merkezi dizin kaydı sayısı
|10|2|Merkezi dizin kayıtlarının toplam sayısı
|12|4|Merkez dizinin boyutu (bayt)
|16|4|Arşiv başlangıcına göre merkezi dizin başlangıcının ofseti
|20|2|Yorum uzunluğu (n)
|22|n|Yorum

## Referanslar

* [PKWARE ZIP Dosya Biçimi Özellikleri](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [PKZip Dosyasının Yapısı](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)

