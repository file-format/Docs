{
  "date" : "2023-01-16",
  "keywords" : [ "DLIS", "what is a DLIS file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "DLIS dosya formatı ve DLIS dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "title" : "DLIS Dosya Formatı - Kuyu Günlüğü Veri Dosyası",
  "linktitle" : "DLIS",
  "menu" : {
    "docs" : {
      "identifier":"database-dlis-tr",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## DLIS dosyası nedir?

.dlis dosya formatı, petrol ve gaz endüstrisinde kuyu günlüğü verilerinin depolanması ve değişimi için standart bir dosya formatıdır. Format, Günlük Endüstrisi Veri Standardı (LIDS) komitesi tarafından geliştirilmiştir ve Dijital Günlük Bilgi Standardı anlamına gelir. Format, iyi günlük verilerini farklı sistemler arasında okunması, yazılması ve değiş tokuş edilmesi kolay bir şekilde depolamak için tasarlanmıştır.

DLIS dosyaları, kuyu günlüğü verilerini ve günlük verilerinin türü (örn. direnç, gama ışını), ölçüm birimleri ve verilerin kuyudaki konumu gibi özelliklerini tanımlayan bir dizi mantıksal kayıt içerir. Gerçek günlük verileri ayrı ikili dosyalarda saklanır ve DLIS dosyasındaki mantıksal kayıtlar tarafından referans alınır.

## Kuyu Log Verileri Hakkında Kısa Bilgi

Kuyu günlüğü verileri, genellikle sondaj işlemi sırasında veya kuyu açıldıktan sonra, bir kuyunun farklı derinliklerinde alınan ölçümlerin bir kaydıdır. Bu ölçümler kuyudaki kaya ve sıvıların çeşitli fiziksel, kimyasal ve/veya jeofizik özelliklerini içerebilir. Kuyu günlüğü verilerinin bazı örnekleri şunları içerir:

- Elektriksel direnç: kayanın elektrik akımı akışına direnme yeteneğinin bir ölçüsü
- Gama ışını: kayanın doğal radyoaktivitesinin bir ölçüsü
- Gözeneklilik: kayadaki açık alanların veya gözeneklerin miktarının ölçüsü
- Sonik: bir ses dalgasının kaya boyunca ilerlemesi için geçen sürenin ölçüsü
- Yoğunluk: Bir kayanın birim hacim başına kütlesinin ölçüsü
- Litoloji: kaya türü veya oluşumunun ölçüsü

Kuyu günlüğü verileri, petrol ve gaz endüstrisinde aşağıdakiler gibi çeşitli amaçlar için kullanılır:

- Hidrokarbon içeren oluşumların yerinin ve kalitesinin belirlenmesi
- Bir kuyunun üretim potansiyelinin değerlendirilmesi
- Bir kuyunun tamamlanması ve uyarılmasının planlanması ve izlenmesi
- Zaman içindeki kuyu davranışının izlenmesi

## PPDM ile İlişki

PPDM (Profesyonel Petrol Veri Yönetimi), kuyu ve üretim verilerini yönetmek için ortak bir veri modeli sağlayan bir petrol ve gaz endüstrisi veri yönetimi standardıdır. PPDM veri modeli, DLIS verileri de dahil olmak üzere kuyu günlüğü verilerini düzenlemek ve yönetmek için kullanılabilecek bir dizi standart veri nesnesini ve ilişkiyi tanımlar.

PPDM veri modeli kuyu ve üretim verileri için kuyular, kuyu başlıkları, kuyu günlükleri ve üretim verileri gibi veri nesnelerini içerir. Aynı zamanda, bir kuyu ile onunla ilişkili kuyu günlükleri arasındaki ilişki gibi, bu veri nesneleri arasındaki ilişkileri de içerir.

PPDM veri modeli, DLIS verileri de dahil olmak üzere kuyu günlüğü verilerini düzenlemek ve yönetmek için tutarlı, endüstri standardında bir yol sağlar. Farklı kuruluşların ortak bir veri modeli kullanarak veri paylaşmasına ve alışverişine olanak tanır, verilerin birlikte çalışabilirliğini artırır ve veri entegrasyon maliyetlerini azaltır.

PPDM veri modeli ve DLIS verilerinin birlikte kullanılması, iyi log verilerinin endüstri standartlarıyla tutarlı ve diğer sistem ve uygulamalar tarafından kolayca erişilebilecek şekilde saklanmasını ve yönetilmesini mümkün kılar.


