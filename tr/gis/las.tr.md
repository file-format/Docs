{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS - Lidar LASer Dosya Formatı",
  "description":"LAS dosyalarını oluşturup açabilen LAS dosya formatı ve API'ler hakkında bilgi edinin.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## LAS Dosyası Nedir?

LAS (Lidar LASer) dosya formatı, özellikle lidar nokta bulutu verilerini depolamak için tasarlanmış bir ikili dosya formatıdır. Lidar veri alışverişi ve birlikte çalışabilirlik için standartlaştırılmış bir format olarak Amerikan Fotogrametri ve Uzaktan Algılama Derneği (ASPRS) tarafından geliştirilmiş ve sürdürülmektedir.

LAS dosyaları, 3B koordinatları (x, y ve z), yoğunluk değerleri, sınıflandırma kodları ve ek nitelikler dahil olmak üzere, bireysel lidar noktaları hakkında ayrıntılı bilgileri saklar. Format, hem ayrık dönüşü hem de tam dalga biçimi lidar verilerini destekleyerek, lazer darbesi başına birden fazla geri dönüşün depolanmasına olanak tanır.

## LAS Dosya Formatı

Bir LAS dosyasının yapısı üç ana bölümden oluşur: dosya başlığı, değişken uzunluklu kayıtlar (VLR'ler) ve nokta veri kayıtları.

1. Dosya Başlığı: Dosya başlığı, veri formatı sürümü, nokta veri formatı, nokta sayısı, sınırlayıcı kutu koordinatları, koordinat referans sistemi (CRS) ve diğer meta veriler gibi LAS dosyası hakkında temel bilgileri içerir. Dosyanın içerdiği lidar verilerinin bir özetini sağlar.

2. Değişken Uzunluklu Kayıtlar (VLR'ler): VLR'ler isteğe bağlıdır ve lidar verileri hakkında ek meta veriler ve özel bilgiler saklayabilir. VLR'ler, formatın belirli kullanıcı gereksinimlerini karşılayacak şekilde genişletilmesinde esneklik sağlar. VLR örnekleri arasında sensör sistemi, veri işleme parametreleri veya sınıflandırma şemaları hakkındaki bilgiler yer alır.

3. Nokta Veri Kayıtları: Nokta veri kayıtları gerçek lidar ölçümlerini saklar. Her nokta veri kaydı, tek bir lidar noktasını temsil eder ve x, y ve z koordinatları, yoğunluk değerleri, sınıflandırma kodları (örneğin zemin, bitki örtüsü, binalar) ve diğer kullanıcı tanımlı nitelikler gibi nitelikleri içerir. Nokta kayıtları aynı zamanda zaman damgalarını, geri dönüş sayımlarını ve tarama açılarını da saklayabilir.

LAS dosyaları, çeşitli lidar verisi türlerini ve ihtiyaç duyulan bilgi düzeyini karşılamak için farklı veri formatlarını (0 ila 10) destekler. Örneğin, format 0, temel bilgileri içeren basit bir nokta formatını temsil ederken, format 1'den 3'e kadar olan formatlar, her dönüş için dalga formu bilgilerini içeren daha kapsamlı veriler sağlar.

LAS dosyaları, lidar yazılımı ve işleme araçları tarafından geniş çapta desteklenir ve bu da onları, lidar veri alışverişi ve analizi için standart bir format haline getirir. Ayrıca LAS dosyaları, orijinal veri doğruluğunu korurken dosya boyutunu küçültmek için kayıpsız sıkıştırma teknikleri kullanılarak sıkıştırılabilir. LAS dosyalarının sıkıştırılmış sürümüne genellikle verimli depolama ve veri aktarma yetenekleri sunan LAZ adı verilir.

## Referanslar

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
