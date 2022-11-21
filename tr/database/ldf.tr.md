{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"LDF dosya formatı ve LDF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"LDF - SQL Server Ana Veritabanı Dosya Biçimi",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .LDF dosyası nedir?

.ldf uzantılı bir dosya, ilişkisel bir veritabanı yönetim sistemi (RDBMS) olan Microsoft SQL Server tarafından tutulan bir günlük dosyasıdır. Birincil veritabanı dosyalarında ([MDF](/tr/database/mdf/))(ekleme, güncelleme, silme gibi) yapılan tüm işlemler LDF dosyasına kaydedilir. LDF dosyaları, herhangi bir veritabanının kritik bileşenleridir. Bir sistem arızası durumunda, veritabanını tutarlı bir duruma geri yüklemek için günlük dosyası kullanılır. İşlemler tam olarak taahhüt edilmezse, işlemler günlük dosyasının boyutu artabilir. LDF dosyaları, Microsoft SQL Server yazılım uygulamasıyla açılabilir.

## LDF Dosyasına Kayıtlı İşlemler

Bir SQL günlük dosyası aşağıdaki işlemleri kaydeder:

* Her işlemin başlangıcı ve bitişi.

* Her veri veri değişikliği (ekleme, güncelleme veya silme). Bu ayrıca, sistem tabloları da dahil olmak üzere herhangi bir tabloya sistem saklı yordamlar veya veri tanımlama dili (DDL) ifadeleri tarafından yapılan değişiklikleri de içerir.

* Her ölçüde ve sayfa ayırma veya ayırma.

* Bir tablo veya dizin oluşturma veya bırakma.

## LDF Dosya Biçimi

LDF dosyası, günlük kayıtları dizisi olarak düzenlenmiş SQL Server işlem kayıtlarından oluşur. Her günlük kaydı, önceki kaydın LSN'sinden daha yüksek bir günlük sıra numarasına (LSN) sahiptir. Dizeler, dosyada birbiri ardına birleştirilir. Modern yüksek hızlı bilgisayarlar sayesinde, LSN1'den önceki günlük dosyasında LSN2'nin bulunduğu yerlere kayıtlar eklenebilir. İşlemler bir seri halinde kaydedildiğinden, LSN2 tarafından açıklanan değişiklik, LSN1 günlük kaydından sonra gerçekleştirildi. Belirli bir işlem için kayıtlar, kullanılan işaretçiler kullanılarak geriye doğru bağlanır ve işlemin geri alınmasını hızlandırır.
 

## Referanslar

* [Veritabanı Dosyaları ve Dosya Grupları](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [İşlem Günlüğü Mimarisi ve Yönetim Kılavuzu](https://docs.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql- sunucu-ver15)

