{
  "date" : "2020-11-11",
  "keywords" :[ "BAK", "uzantı", "dosya", "dosya formatı", "BAK Dosya Tipi", "BAK Dosya Uzantısı", "Veritabanı Dosya Tipi", "Veritabanı Dosya Formatı", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"BAK dosya formatı ve BAK dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"BAK Dosya Formatı - Veritabanı Yedekleme Dosyası",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## BAK dosyası nedir?

.bak uzantılı bir dosya, genellikle farklı yazılım araçları tarafından verilerin yedeklerini depolamak için kullanılan bir yedekleme dosyasıdır. Veritabanı açısından bakıldığında, Microsoft SQL Server tarafından bir veritabanının içeriğini depolamak için bir BAK dosyası kullanılır. Veritabanıyla ilişkili tüm veriler ve dosyalar, veritabanının herhangi bir nedenle bozulması veya geçersiz hale gelmesi durumunda geri alınmak üzere bu dosya biçiminde saklanır. Yedekleme dosyaları, güvenlik amacıyla diğer sunucularda saklanabilir ve dizine eklenebilir. SQL Server Management Studio, Transact-SQL ve Windows PowerShell gibi çeşitli uygulamalar BAK dosyaları oluşturabilir.

## BAK Dosya Biçimi

Bir BAK dosyasının dahili detayları bilinmemekle birlikte, Microsoft Teyp Formatına (MTF) dayalı olduğu yaygın olarak varsayılmaktadır. MTF belirtimleri mevcuttur ve dosyanın yapısını anlamak için başvurulabilir. Belge, depolama yönetimi işlemleri, teyp sürücüleri ve dosya sistemleri hakkında genel bilgisi olan herkes için MTF depolaması hakkında ayrıntılar sağlar.

### Veri Kümeleri

Veri seti, veri yedekleme veya geri yükleme sırasında bir depolama ortamına (bant, optik disk vb.) yazılan nesneler topluluğudur. Veri kümeleri, büyük miktarda veri olması durumunda birden çok ortamdan oluşur.

### MTF'nin Temel Unsurları

Bir MTF dosyası, yapı taşlarını oluşturan bazı temel öğelerden oluşur. Bu unsurlar:

#### Tanımlayıcı Bloklar

Tanımlayıcı bloklar (DBLK), format kontrolü için kullanılır ve bir MTF dosyasının birincil temellerini oluşturur. Tek bir MTF dosyası, her benzersiz rol için birden çok DBLK tanımlar. Her DBLK, aşağıdaki dört bölüme ayrılan değişken uzunluklu bir veri bloğudur:

* `Ortak Blok Başlığı` - Tüm DBLK'lerde ortak olan sabit uzunlukta yapı. Bu, gerekli olan tek Blok Başlığıdır.
* `DBLK Tip Bilgisi` - Tanımlanmakta olan DBLK tipine özel Sabit Uzunluk bloğu
* "İşletim Sistemi Verileri" - DBLK türüne ve İşletim sistemlerine göre tanımlanan belirli veriler
* `DBLK Bilgisi` - Sabit Uzunluk DBLK bilgisi ile kaydedilemeyen değişken uzunluklu DBLK'ye özgü bilgi.

 {{< figure src="../bak.png" alt="Microsoft SQL Yedek Dosya Biçimi" >}}

#### Veri akışı

Bir MTF dosyasındaki veri akışları, veri kapsülleme ve hizalama için kullanılır. Bir Akış Başlığından ve ardından Akış Verilerinden oluşur. Bir akış başlığı, yalnızca tek bir Akış Verisi türünü kapsülleyebilir.

{{< figure src="../bak_datastream.png" alt="Microsoft SQL Yedek Dosya Biçimi" >}}

#### Dosya İşaretleri

Dosya işareti, bir ortam içinde mantıksal ayırma ve hızlı erişim için kullanılır. Dosya işaretleri, kullanılan aygıtın dosya işaretleri sağlamaması durumunda, aygıt sürücüsü tarafından veya Soft Filemark Descriptor bloğu kullanılarak öykünülür.

## Referanslar ##

* [[MS-BCP]: Toplu Kopya Biçimi](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

