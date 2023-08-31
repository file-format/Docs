{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MDF dosya formatı ve NDF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"NDF Dosya Biçimi - SQL Server Ana Veritabanı Dosyası",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .df dosyası nedir?

.ndf uzantılı bir dosya, kullanıcı verilerini depolamak için [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) tarafından kullanılan ikincil bir veritabanı dosyasıdır. NDF, ikincil depolama dosyasıdır çünkü SQL sunucusu, kullanıcı tarafından belirtilen verileri [MDF](/tr/database/mdf/) olarak bilinen birincil depolama dosyasında depolar. NDF veri dosyası isteğe bağlıdır ve birincil MDF dosyasının tahsis edilen tüm alanı kullanması durumunda veri depolamayı yönetmek için kullanıcı tanımlıdır. Genellikle ayrı bir diskte depolanır ve birden çok depolama aygıtına yayılabilir. NDF dosyalarının açılabilmesi için MDF dosyalarının varlığı gereklidir.

## NDF Dosya Biçimi

NDF dosya formatı [MDF](/tr/database/mdf/)'den farklı değildir ve veri depolamanın temel birimi olarak sayfaları kullanır. her sayfa, aşağıdakileri içeren 96 baytlık bir başlıkla başlar:

* Sayfa Kimliği
* Yapı Tipi
* Sayfalardaki kayıt sayısı
* Önceki ve sonraki sayfalara işaretçiler

### NDF Dosya Yapısı

Bir MDF dosyası aşağıdaki veri yapısına sahiptir.

* Sayfa 0: Başlık
* Sayfa 1: İlk PFS
* Sayfa 2: İlk GAM
* Sayfa 3: İlk SGAM
* Sayfa 4: Kullanılmamış
* Sayfa 5: Kullanılmamış
* Sayfa 6: İlk DCM
* Sayfa 7: İlk BCM

#### NDF Dosya Başlığı

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

## Veri Dosyası Sayfası

Bir SQL Server veri dosyasındaki sayfalar sıfırdan (0) başlar ve sırayla artar. Her dosya, benzersiz bir dosya kimlik numarası ile tanınır. Dosya kimliği ve sayfa numarası çifti, bir veritabanındaki bir sayfayı benzersiz şekilde tanımlar. Veritabanındaki sayfa numaralarını gösteren bir örnek aşağıdaki görseldeki gibidir.

{{< figure src="../ndf.png" alt="NDF Veritabanı Dosya Biçimi" >}}

Bu örnek, 4 MB birincil veri dosyası ve 1 MB ikincil veri dosyası içeren bir veritabanındaki sayfa numaralarını gösterir.

## Referanslar

* [Veritabanı Dosyaları ve Dosya Grupları](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver16)
* [Veritabanı Ayır ve Ekle - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [SQL Server Veri Dosyası Anatomisini Analiz Etme](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

