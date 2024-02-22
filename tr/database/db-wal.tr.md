{
  "date" : "2023-01-16",
  "keywords" : [ "DB-WAL", "what is a DB-WAL file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "DB-WAL dosya formatı ve DB-WAL dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "title" : "DB-WAL Dosya Formatı - SQLite Veritabanı Yazma Öncesi Günlük Dosyası",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal-tr",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## DB-WAL dosyası nedir?

.db-wal dosya uzantısı, popüler bir açık kaynaklı ilişkisel veritabanı yönetim sistemi olan SQLite ile ilişkilidir. WAL dosya formatı (Önceden Yazma Günlüğü'nün kısaltması), SQLite tarafından kullanılan geleneksel geri alma günlüğüne bir alternatiftir. Daha fazla eşzamanlılık kontrolü sağlayarak, birden fazla işlemin aynı anda veritabanını okumasına olanak tanırken, aynı zamanda çökme kurtarma yeteneklerini de sağlar. .db-wal dosyası, henüz ana veritabanı dosyasına (.db uzantılı) kaydedilmemiş, veritabanında yapılan değişiklikleri depolamak için kullanılır.

## Genel WAL Formatı

WAL (Önceden Yazma Günlüğü) dosya formatında, veritabanında yapılan değişiklikler, ana veritabanı dosyasına kaydedilmeden önce ilk olarak WAL dosyasına yazılır. Bu, değişiklikler yapılırken birden fazla işlemin veritabanından okuyabilmesi nedeniyle veritabanına daha eşzamanlı erişime olanak tanır. Ayrıca WAL dosya formatı, beklenmedik bir kapanma durumunda veritabanının önceki bir duruma geri alınmasına olanak tanıyan kilitlenme kurtarma yetenekleri sağlar.

## DB-WAL ve WAL formatı arasındaki fark

Hem .db-wal hem de WAL dosya formatları, popüler bir açık kaynaklı ilişkisel veritabanı yönetim sistemi olan SQLite ile ilişkilidir. Ancak ikisi arasında ince bir fark var.

.db-wal dosyası aslında bir WAL dosyasıdır ancak farklı bir dosya uzantısına sahiptir. .db-wal dosyası, henüz ana veritabanı dosyasına kaydedilmemiş (.db uzantılı) veritabanında yapılan değişiklikleri depolamak için kullanılırken, WAL dosya formatı, veritabanı değişikliklerinin yazma öncesi günlüğünü depolamak için kullanılır. .

Başka bir deyişle, .db-wal dosyası, SQLite veritabanları tarafından, henüz ana veritabanı dosyasına kaydedilmemiş veritabanında yapılan değişiklikleri depolamak için kullanılan belirli bir WAL dosyası türüdür. WAL dosya formatı bu tür dosya formatı için genel terimdir.

Dolayısıyla WAL, dosya formatı için genel terimdir, .db-wal ise SQLite veritabanları tarafından kullanılan WAL dosya formatının özel bir uygulamasıdır.

## Referanslar
* [WAL Modu Dosya Formatı](https://www.sqlite.org/walformat.html)

* [Önceden Yazma Günlüğü](https://www.sqlite.org/wal.html)


