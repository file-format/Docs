{
  "date" : "2019-10-11",
  "keywords" :[ "osm dosyası", "osm dosyası nedir", "dosya", "osm örneği", "osm dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM - OpenStreetMap Dosya Biçimi",
  "description":"OSM dosya formatı ve OSM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## OSM dosyası nedir?

OpenStreetMap (OSM), bu verileri bit ve baytlara dönüştürmek için farklı kodlama şemaları kullanan, farklı dosya türlerinde büyük bir gönüllü coğrafi bilgi depoları koleksiyonudur. OSM, dünyanın ücretsiz düzenlenebilir bir haritasının oluşturulmasına yönelik ortak bir çabadır. Bu işbirlikçi çabanın birincil çıktısı, haritanın kendisinden ziyade coğrafi verilerdir. Dünyanın birçok yerinde coğrafi bilginin kullanımı veya mevcudiyeti üzerindeki kısıtlamalar, bir OSM oluşturma ihtiyacını tetikler. OSM'den elde edilen veriler, klasik uygulamalar (Facebook, Craigslist vb.) için Google Haritalar'ın ve GPS alıcısının uygulamaları için varsayılan verilerin yerini almaya hazırdır.^^ ^^Veri kalitesi dünya çapında çeşitlilik gösterse de, OpenStreetMap verileri rahatlıkla patentle karşılaştırılabilir veri kaynakları.

## Kısa Tarih ##

Wikipedia'nın başarısından ilham alan İngiliz girişimci Steve Coast, 2004 yılında Birleşik Krallık'ta bu topluluk temelli dünya haritalama projesini yarattı. Başlangıçta Birleşik Krallık'ın haritasını çıkarmaya odaklandı. OpenStreetMap Foundation, ilk olarak Nisan 2006'da herkes için ücretsiz jeo-uzaysalın gelişimini, genişlemesini ve dolaşımını desteklemek için kuruldu. Aralık 2006'da Yahoo, harita üretimi için hava fotoğrafçılığında OpenStreetMap'e yardım etti. Hollanda için eksiksiz yol verileri ve Hindistan ve Çin için ana yol verileri, Otomotiv Navigasyon Verileri (AND) tarafından Nisan 2007'de OSM'ye katkıda bulunulmuştur. Aralık 2007'de Oxford Üniversitesi, OpenStreetMap verilerini ana web sitesine entegre eden en önde gelen kuruluştu. O zamandan beri, 2 milyonun üzerinde kayıtlı kullanıcı, GPS cihazları, hava fotoğrafları ve manuel anketler kullanarak bu projeye veri sağlıyor. Topluluğun katkıda bulunduğu bu veriler, Açık Veritabanı Lisansı altında kullanıma sunulur. İngiltere'de tescilli, kar amacı gütmeyen bir kuruluş olan OpenStreetMap Foundation, OSM sitesinin bakımını yaptı.

## OSM Dosya Biçimi ##

Coğrafi verileri saklamanın birçok yolu ve dosya formatı vardır ancak **OSM** dosya formatı OpenStreetMap ile sınırlıdır. OSM, internet üzerinden kolayca taşınması amaçlanan özel olarak tasarlanmış standart bir formattır. XML'de kodlanmış, yapılandırılmış sıralı bir biçim, .osm dosyasını oluşturur. OpenStreetMap'te topolojik veri yapısını depolamak için dört pivot öğe vardır:

{{< figure src="../OSM.png" alt="OSM Dosya Biçimi" >}}


|Düğümler|Yollar|İlişkiler|Etiketler
---|---|---|---|
|<ul><li> Enlem ve boylam çiftleri olarak saklanan coğrafi konumu temsil eder.</li><li> Dağ zirveleri gibi bir boyutu olmayan harita özelliklerini temsil etmek için kullanılır.</li></ul> |<ul><li> Bir çoklu çizgiyi veya bir çokgeni gösteren sıralanmış düğüm listeleri</li><li> Yollar ve nehirler gibi doğrusal özellikleri ve park alanları, ormanlar ve parklar gibi bölgeleri temsil eder.</li></ul> |<ul><li> Düğümlerin ve yolların sıralanmış listeleri, yollardaki engeller ve u dönüşleri gibi ilişkilerini temsil eder, otoyollar farklı mevcut yolları ve delikli alanları kapsar.</li></ul> |<ul><li> Harita nesneleri hakkında meta verileri depolayın.* Her zaman herhangi bir düğüme, yola veya ilişkiye bağlı</li></ul>


Etiketler, OpenStreetMap'te yerdeki fiziksel özellikleri (binalar ve yollar vb.) karakterize etmek için kullanılır. Her etiket, söz konusu belirli düğüm veya ilişki tarafından temsil edilen özelliğin bir coğrafi özelliğini ilişkilendirir. Bu ücretsiz etiketleme sisteminde, bir özelliği tanımlamak için, bir haritaya sınırsız sayıda özellik dahil edilebilir. Kayıtlı kullanıcılar tarafından onaylanan belirli anahtar ve değer kombinasyonları, sık kullanılan etiketler için resmi olmayan standartlar görevi görür. Bununla birlikte, özelliklerin daha önce eşlenmemiş özniteliklerini analiz etmek için yeni yönler gerektiğinde yeni etiketler oluşturulabilir. Çoğu özellik, açıklama için yalnızca az sayıda etiket kullanır.

OSM tarafından ana verilerini depolamak için üç tür dosya kullanılır.

OSM, tüm bu dosyaları biçimlendirme ayrıntılarıyla ilgili bilgilerle işler. Ancak aynı dahili nesneler bu dosyalar tarafından üretilir. Veri dosyaları için, OSM nesnelerindeki görünür bayrak her zaman doğrudur, geçmiş ve değişiklik dosyaları için durum böyle değildir.

Yaygın kullanımda, OSM dosya formatlarında bir çeşitlilik vardır. Dosya formatları, disk veya kablo üzerindeki içerik kodlamasını bit ve bayt cinsinden tanımlar. OSM, bu formatlardan maksimum okuma ve yazma yeteneğine sahiptir.

**XML**

Orijinal OSM formatı XML tabanlıdır. Ana OSM veri tabanı API'sinin dönüş verileri XML formatındadır.

**PBF**

Protokol Arabellekleri kodlaması, ikili formatta ve en kompakt formatlardan birinde durur.

**O5M/O5C**

İkili biçim tabanlı daha basit biçim ancak nispeten daha az kullanılır. OSM bu formatı okuyabilir ancak yazamaz.

**OPL**

Standart UNIX komut satırı araçlarıyla kullanılması önerilen basit bir biçim. CSV dosyalarına yakın, bir satırda bir OSM varlığına izin verir.

**HATA AYIKLAMA**

Hata ayıklama için oluşturulması amaçlanan metin tabanlı bir biçim. OSM bu formatı yazabilir ancak okuyamaz.

**KARA DELİK**

Tüm verileri ortadan kaldıran sahte bir biçim. OSM bu formatı yazabilir ancak okuyamaz.

## OSM Veri Depolama ##

OSM'nin ana **PostgreSQL** veritabanı, PostGIS uzantılı OSM verilerinin ana kopyasını tutar. Her veri ilkel için, ana veritabanı, satırları ayrı ayrı nesneleri depolayan bir tablo tutar. Tüm düzenlemeler bu veritabanını günceller ve diğer tüm formatlar bu veritabanı kullanılarak oluşturulur. Verileri bir yerden diğerine aktarmak için çok sayıda indirilebilir veritabanı havuzu oluşturulur. Biri XML kullanan ve diğeri Protocol Buffer Binary Format (PBF) kullanan iki format bu havuzları tanımlar. Tüm veriler, planet.osm adlı bir dosyada saklanır.

## OSM Dosyalarında Sıkıştırma ##

Metin tabanlı biçimler (XML, OPL ve Debug) isteğe bağlı olarak gzip veya bzip2 sıkıştırmasını kullanır.

## Referanslar ##

* [OSM dosya Biçimleri Kılavuzu](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [OSM'yi Öğrenin](https://learnosm.org/en/osm-data/getting-data/)

