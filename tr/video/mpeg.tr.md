{
"tarih": "2023-07-12",
  "keywords": [
"mpeg",
"mpeg dosyası",
"mpeg dosyası nedir",
"mpeg dosyası nasıl açılır",
"dosya",
"mpeg dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "MPEG Dosya Formatı - MPEG Video",
  "description":"MPEG formatı ve MPEG dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle" : "MPEG",
  "menu": {
    "docs": {
      "identifier": "video-mpeg",
      "parent": "video"
}
},
"sonmod": "2023-07-12"
}

## MPEG dosyası nedir?

MPEG video dosyası olarak da bilinen MPEG dosyası, video sıkıştırma için Hareketli Resim Uzmanları Grubu (MPEG) standartlarını kullanan bir dijital video dosyası formatıdır. MPEG, video verilerinin saklanması ve iletilmesi için yaygın olarak kullanılan bir formattır.

MPEG formatı kayıplı sıkıştırma kullanır; bu, dosya boyutunu küçültmek için bazı bilgilerin atıldığı anlamına gelir. Bu sıkıştırma tekniği, makul video kalitesini korurken, video içeriğinin verimli bir şekilde depolanmasına ve akışına olanak tanır. MPEG standardının, MPEG-1, MPEG-2, MPEG-4 ve MPEG-7 dahil olmak üzere her biri farklı sıkıştırma ve kalite düzeylerine sahip çeşitli sürümleri vardır.

MPEG dosyaları genellikle ".mpeg" veya ".mpg" dosya uzantısına sahiptir. Genellikle tek bir dosyada birleştirilen hem video hem de ses verilerini içerebilirler. MPEG dosyaları çok çeşitli medya oynatıcılar ve video düzenleme yazılımlarıyla uyumludur, bu da onları video içeriği paylaşımı ve dağıtımı için popüler bir seçim haline getirir.

## MPEG dosyası nasıl açılır?

MPEG dosyalarını açabilen ve oynatabilen çok sayıda yazılım uygulaması bulunmaktadır. İşte bazı popüler seçenekler:

- VLC medya oynatıcı
- Windows Medya Oynatıcısı
- QuickTime Oynatıcı
-MPC-HC
- GOM Oyuncusu
- MP oynatıcı
- PotPlayer
- Kodi

## MPEG dosyası nasıl dönüştürülür?

VideoLAN VLC medya oynatıcısı, HandBrake ve Apple QuickTime Player dahil olmak üzere MPEG dosyalarını diğer formatlara dönüştürebilen çok sayıda video uygulaması vardır. Örneğin VLC, MPEG dosyalarını bu formatlara dönüştürebilir

- MP4
-AVI
-MKV
- MOV
-WMV
-FLV

## MPEG Dosyalarının İç Yapısına Genel Bakış

MPEG dosyalarının iç yapısı, video, ses ve diğer ilgili bilgileri düzenleyen ve saklayan farklı bileşenlerden ve veri yapılarından oluşur. MPEG dosyalarının iç yapısındaki temel unsurlara genel bir bakış aşağıda verilmiştir:

- **Sistem Katmanı:**

Sistemler katmanı MPEG dosyasının genel yapısını tanımlar. Kod çözme ve oynatma için gerekli olan başlıkları, program akışlarını ve sistemle ilgili diğer verileri içerir. Sistemler katmanı, temel akışların senkronizasyonunu ve çoğullanmasını yönetmekten sorumludur.

- **Temel Akışlar:**

MPEG dosyaları video, ses ve diğer veri türleri için ayrı temel akışlar içerir. Her temel akış, türüne özgü sıkıştırılmış verileri taşır. Örneğin, video temel akışı sıkıştırılmış video kareleri içerir ve ses temel akışı sıkıştırılmış ses örnekleri içerir.

- **Video sıkıştırma:**

Kare içi ve kareler arası sıkıştırma gibi MPEG video sıkıştırma teknikleri, video kalitesini korurken dosya boyutunu küçültmek için kullanılır. Sıkıştırılmış video kareleri, dahili kodlanmış (I), tahmin edilen (P) ve çift yönlü (B) karelerden oluşan resim grupları (GOP'ler) halinde düzenlenir.

- **Ses Sıkıştırma:**

MPEG dosyaları MP3, AAC veya MPEG-1 Audio Layer II gibi çeşitli ses sıkıştırma codec bileşenlerini destekler. Ses örnekleri bu codec'ler kullanılarak sıkıştırılarak ses verilerinin verimli bir şekilde depolanmasına ve iletilmesine olanak sağlanır.

- **Senkronizasyon ve Zamanlama:**

MPEG dosyaları, oynatma sırasında video ve ses akışları arasında uygun hizalamayı sağlamak için zaman damgalarını ve senkronizasyon bilgilerini kullanır. Bu zaman damgaları senkronizasyonun korunmasına yardımcı olur ve ses ve video karelerinin kodunun çözülmesi ve işlenmesi için doğru zamanlama sağlar.

- **Meta veriler:**

MPEG dosyaları, video ve ses içeriği hakkında ek bilgi sağlayan meta veriler içerebilir. Bu meta veriler başlık, yazar, oluşturulma tarihi gibi ayrıntıları ve diğer açıklayıcı bilgileri içerebilir.

- **Paketler ve Paket Başlıkları:**

MPEG dosyaları verileri paketler halinde düzenler. Her paket, akış türü, paket boyutu ve zamanlama bilgileri gibi paketin içeriği hakkında bilgi sağlayan bir paket başlığı içerir.

- **Programa Özel Bilgiler (PSI):**

PSI, MPEG dosyalarında program ve akış tanımlayıcıları, akış türü ve tanımlayıcılar gibi program akışları hakkında ek bilgiler taşıyan bir bölümdür. PSI, dosya içindeki temel akışların kodunun çözülmesine ve çoğullamasının çözülmesine yardımcı olur.

- **Ulaşım Akışı:**

MPEG-2'de video içeriğini yayınlamak ve iletmek için kullanılan özel bir aktarım akışı formatı vardır. Taşıma akışı, birden fazla programı tek bir akışta çoğaltarak ses, video ve diğer verilerin ağlar üzerinden verimli bir şekilde iletilmesine ve senkronize edilmesine olanak tanır.

## MPEG Dosya Formatı - Daha Fazla Bilgi

MPEG dosya formatı hakkında bilmeniz gereken bazı önemli noktalar şunlardır:

- **Sıkıştırma:**

MPEG dosyaları, makul video kalitesini korurken dosya boyutunu küçültmek için kayıplı sıkıştırma teknikleri kullanır. Sıkıştırma miktarı, kullanılan MPEG sürümüne ve ayarlara bağlı olarak değişebilir.

- **Video ve Ses:**

MPEG dosyaları hem video hem de ses verilerini içerebilir. Video verileri MPEG standartları kullanılarak sıkıştırılırken ses, MP3 veya AAC gibi çeşitli ses codec bileşenleri kullanılarak sıkıştırılabilir.

- **MPEG Sürümleri:**

MPEG standardının MPEG-1, MPEG-2, MPEG-4 ve MPEG-7 dahil olmak üzere farklı versiyonları vardır. Her sürümün kendine özgü özellikleri, yetenekleri ve sıkıştırma düzeyleri vardır. MPEG-1 yaygın olarak VCD'ler (Video CD'ler) için kullanılırken, MPEG-2 DVD'ler ve televizyon yayını için kullanılır. MPEG-4, çevrimiçi video akışı için yaygın olarak kullanılır ve MPEG-7, multimedya içerik açıklamasına ve meta verilere odaklanır.

- **Dosya uzantıları:**

MPEG dosyaları genellikle ".mpeg" veya ".mpg" dosya uzantılarına sahiptir. Ancak MPEG-4 dosyaları için ".mp4" veya MPEG-1 Ses Katmanı 3 dosyaları için ".mp3" gibi farklı varyasyonlar ve uzantılar mevcut olabilir.

- **Platformlar arası uyumluluk:**

MPEG dosyaları çeşitli medya oynatıcılar, işletim sistemleri ve cihazlar tarafından yaygın olarak desteklenir. Windows, Mac ve Linux sistemlerinin yanı sıra akıllı telefonlarda, tabletlerde ve akıllı TV'lerde oynatılabilirler.

- **Düzenleme:**

MPEG dosyaları video düzenleme yazılımı kullanılarak düzenlenebilir. Ancak MPEG kayıplı sıkıştırma kullandığından, dosyanın tekrar tekrar düzenlenmesi ve yeniden kodlanması kalitenin düşmesine neden olabilir. Kapsamlı düzenleme öncesinde genellikle kayıpsız formatlarla çalışmanız veya yedek kopyalar almanız önerilir.

- **Yayın Akışı:**

MPEG dosyaları genellikle internet üzerinden video içeriği akışı için kullanılır. Özellikle MPEG-4, verimli sıkıştırması ve iyi kalite-boyut oranı nedeniyle çevrimiçi video platformları ve video paylaşım web siteleri için popülerdir.

- **Gelişen Standartlar:**

MPEG standartları teknolojik gelişmelere ayak uydurmak için gelişmeye devam ediyor. MPEG-4 Bölüm 10 (H.264 veya AVC olarak da bilinir) ve MPEG-4 Bölüm 14 (MP4) gibi daha yeni sürümler ve varyasyonlar, gelişmiş sıkıştırma verimliliği ve yüksek çözünürlüklü video ve 3D içerik gibi gelişmiş özellikler için destek sunar.

- **Multimedya Uygulamaları:**

MPEG dosyaları, dijital televizyon, yayın hizmetleri, video konferans, video gözetimi, multimedya sunumları ve daha fazlası dahil olmak üzere çeşitli alanlarda uygulama bulur.

## MPEG ve Diğer Formatlar

MPEG dosya formatını diğer video formatlarıyla karşılaştırırken sıkıştırma verimliliği, uyumluluk, özellikler ve destek gibi çeşitli faktörler devreye girer. İşte MPEG'in bazı popüler video formatlarıyla karşılaştırması:

### MPEG ve AVI (Ses Video Araya Ekleme)

- **Sıkıştırma:**
   

MPEG dosyaları genellikle AVI'ye kıyasla daha yüksek sıkıştırma verimliliği sunar ve bu da dosya boyutlarının daha küçük olmasını sağlar.

- **Uyumluluk:**

AVI dosyaları çeşitli medya oynatıcılar tarafından geniş çapta desteklenir, ancak MPEG dosyalarının cihazlar ve platformlar arasında daha geniş uyumluluğu vardır.

- **Özellikler:**

MPEG dosyaları genellikle birden fazla ses parçası, altyazı ve bölüm gibi daha gelişmiş özellikleri desteklerken AVI'nin bu tür özellikler için sınırlı desteği vardır.

- **Video kalitesi:**

Sıkıştırma ayarlarına bağlı olarak MPEG ve AVI benzer video kalitesi elde edebilir ancak MPEG, gelişmiş sıkıştırma teknikleri nedeniyle genellikle daha düşük bit hızlarında daha iyi kalite sağlar.

### MPEG ve WMV (Windows Media Video):

- **Sıkıştırma:**

WMV dosyaları genellikle MPEG'ye kıyasla daha iyi sıkıştırma verimliliği sunar, bu da iyi video kalitesini korurken dosya boyutlarının daha küçük olmasını sağlar.

- **Uyumluluk:**

MPEG dosyaları farklı cihazlar ve platformlar arasında daha geniş bir uyumluluğa sahipken WMV dosyaları öncelikle Windows tabanlı sistemlerle ilişkilendirilir.

- **Özellikler:**

Her iki format da birden fazla ses parçası ve altyazı da dahil olmak üzere bir dizi özelliği destekler, ancak MPEG genellikle gelişmiş özellikler için daha fazla çok yönlülük ve daha geniş destek sağlar.

- **Video kalitesi:**

Benzer sıkıştırma ayarlarıyla MPEG ve WMV karşılaştırılabilir video kalitesi elde edebilir ancak WMV, gelişmiş sıkıştırma teknikleri nedeniyle belirli senaryolarda daha iyi performans gösterebilir.

### MPEG ve MP4 (MPEG-4 Bölüm 14):

- **Sıkıştırma:**

Hem MPEG hem de MP4 benzer sıkıştırma teknikleri kullanır ve sıkıştırma verimliliği karşılaştırılabilir. Ancak MP4 içindeki MPEG-4 Bölüm 10 (H.264/AVC), genellikle eski MPEG formatlarından daha iyi sıkıştırma sağlar.

- **Uyumluluk:**

Hem MPEG hem de MP4, cihazlar ve platformlar arasında yaygın bir uyumluluğa sahiptir. MP4, geniş desteği ve benimsenmesi nedeniyle son yıllarda önemli bir popülerlik kazanmıştır.

- **Özellikler:**

MP4, altyazılar, bölümler, etkileşimli menüler ve H.264 ve HEVC (H.265) gibi gelişmiş video codec bileşenleri desteği dahil olmak üzere daha gelişmiş özellikler ve yetenekler sunar. MP4 içindeki MPEG-4 Bölüm 2 (DivX, Xvid) de gelişmiş özellikleri destekler.

- **Video kalitesi:**

MPEG ve MP4, karşılaştırılabilir sıkıştırma ayarları kullanıldığında benzer video kalitesi elde edebilir. Ancak MP4'ün daha gelişmiş video codec'lerini desteklemesi, daha düşük bit hızlarında daha iyi kalite sağlar.

## Referanslar
* [MPEG-1](https://en.wikipedia.org/wiki/MPEG-1)

