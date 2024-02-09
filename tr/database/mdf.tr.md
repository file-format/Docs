{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MDF dosya formatı ve MDF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"MDF Dosya Biçimi - SQL Server Ana Veritabanı Dosyası",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## MDF dosyası nedir?

.mdf uzantılı bir dosya, kullanıcı verilerini depolamak için [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) tarafından kullanılan bir Ana Veritabanı Dosyasıdır. Tüm veriler bu dosyada saklandığı için birincil öneme sahiptir. MDF dosyası, kullanıcı verilerini ilişkisel veritabanlarında form sütunlarında, satırlarda, alanlarda, dizinlerde, görünümlerde ve tablolarda depolar. SQL Server, veritabanının performansı üzerinde olumlu bir etkiye sahip olmak için otomatik büyütme ve otomatik küçültme ayarlarının yapılmasına izin verir. MDF dosyaları, Microsoft SQL Server kullanılarak bir veritabanına yüklenebilir ve eklenebilir. MDF dosyalarının Uygulama/octet-stream mime türü vardır.

## MDF Dosya Biçimi

SQL Server'daki temel veri depolama birimi bir sayfadır. Veritabanına atanan bir depolama sayfası, 0'dan n'ye kadar numaralandırılmış mantıksal sayfalara bölünmüştür. Tek bir sayfa, Sayfa Kimliği, sayfanın ait olduğu yapı türü, sayfadaki kayıt sayısı ve önceki ve sonraki sayfalara işaretçilerden oluşan 96 baytlık bir başlık ile başlar.

### Dosya Yapısı

Bir MDF dosyası aşağıdaki veri yapısına sahiptir.

* Sayfa 0: Başlık
* Sayfa 1: İlk PFS
* Sayfa 2: İlk GAM
* Sayfa 3: İlk SGAM
* Sayfa 4: Kullanılmamış
* Sayfa 5: Kullanılmamış
* Sayfa 6: İlk DCM
* Sayfa 7: İlk BCM

#### Dosya Başlığı

Tüm dosyaların sayfa numarası 0, dosyayla ilgili meta verileri depolayan bir başlık içerir.

#### Sayfa Boş Alanı (PFS)
PFS, ayırma durumunu tanımlar ve boş alan miktarını belirler.

* Bit 1: Sayfanın tahsis edilip edilmediğini gösterir.
* Bit 2: Sayfanın karma ölçüde olup olmadığını gösterir.
* Bit 3: Bu sayfanın bir IAM sayfası olduğunu belirtir.
* Bit 4: Bu sayfanın hayalet kayıtlar içerdiğini belirtir
* Bit 5 ila 7: Sayfa doluluğunu aşağıdaki gibi gösteren birleşik üç bitlik bir değer:
* 0: Sayfa boş
* 1: Sayfa %1–50 dolu
* 2: Sayfa %51–80 dolu
* 3: Sayfanın %81–95'i dolu
* 4: Sayfa %96–100 dolu

## Referanslar

* [Veritabanı Dosyaları ve Dosya Grupları](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Veritabanı Ayır ve Ekle - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [SQL Server Veri Dosyası Anatomisini Analiz Etme](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

