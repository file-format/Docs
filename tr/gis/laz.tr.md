{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ - Sıkıştırılmış LIDAR Veri Değişim Dosyası",
  "description":"LAZ dosya formatı ve LAZ dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## LAZ Dosyası Nedir?

LAZ dosya formatı, özellikle lidar nokta bulutu verilerini depolamak için tasarlanmış LAS (Lidar LASer) dosya formatının sıkıştırılmış bir versiyonudur. LAZ dosyaları, LAS dosyalarıyla aynı verileri ve yapıyı korur ancak orijinal veri doğruluğunu korurken dosya boyutunu küçültmek için kayıpsız sıkıştırma teknikleri kullanır.

## LAZ Dosya Formatı - Kısa Tarihçe

LAZ dosya formatı, büyük lidar veri kümelerinin verimli bir şekilde depolanması ve iletilmesi için artan talebi karşılamak üzere geliştirildi. LAS dosyalarını sıkıştırarak, LAZ dosyalarının boyutları önemli ölçüde küçültülür ve yönetilmeleri ve aktarılmaları daha kolay hale gelir. Sıkıştırma, Lidar noktası niteliklerini daha kompakt bir biçimde temsil etmek için entropi kodlaması ve değişken uzunluklu kodlama gibi farklı algoritmaların bir kombinasyonu kullanılarak elde edilir.

## LAZ Dosya Formatı

Sıkıştırmaya rağmen LAZ dosyaları, herhangi bir bilgi kaybı olmadan orijinal LAS verilerini tamamen geri yükleme yeteneğini korur. Bu, bir LAZ dosyasının sıkıştırması açıldığında, sıkıştırılmamış bir LAS dosyasıyla aynı şekilde işlenebileceği ve analiz edilebileceği anlamına gelir. Sıkıştırma ve açma işlemi genellikle LAZ formatını destekleyen özel yazılım veya kitaplıklar kullanılarak gerçekleştirilir.

LAZ dosya formatı, LAS dosyalarıyla uyumluluğu koruyarak lidar yazılımı ve işleme araçları arasında birlikte çalışabilirliği sağlar. Bu, LAS dosyalarını okuyabilen ve işleyebilen uygulamaların genellikle LAZ dosyalarını herhangi bir değişiklik yapmadan işleyebileceği anlamına gelir. Ayrıca LAZ dosyaları, LAS dosyalarıyla aynı yapıyı koruyarak dosya başlığını, değişken uzunluklu kayıtları (VLR'ler) ve nokta veri kayıtlarını içerir.

## LAZ Dosya Formatının Avantajları

**Küçültülmüş Dosya Boyutu:** LAZ sıkıştırması, lidar veri kümelerinin dosya boyutunu önemli ölçüde azaltır, böylece onları daha yönetilebilir ve saklanması ve aktarılması daha kolay hale getirir.

**Veri Bütünlüğü:** LAZ sıkıştırması kayıpsızdır; bu, sıkıştırılmamış verilerin orijinal LAS verilerinin tam bir kopyası olduğu ve bilgi veya hassasiyet kaybı olmadığı anlamına gelir.

**Birlikte çalışabilirlik:** LAZ dosyaları LAS dosyalarıyla uyumludur ve mevcut lidar yazılımı ve iş akışlarıyla kusursuz entegrasyona olanak tanır.

**Verimli İşleme:** Küçültülmüş boyutları nedeniyle, LAZ dosyaları daha hızlı yüklenip işlenebilir, böylece genel işlem ve analiz süreleri iyileşir.

LAZ dosya formatı, sıkıştırılmış lidar veri depolama ve alışverişi için bir standart olarak lidar topluluğunda yaygın olarak benimsenmiştir. Verimli veri sıkıştırma ile veri bütünlüğü arasında bir denge sunarak büyük lidar veri kümelerinin daha kolay işlenmesini sağlarken orijinal verilerin doğruluğunu ve kalitesini korur.

## Referanslar

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
