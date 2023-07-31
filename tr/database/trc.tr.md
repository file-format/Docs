{
  "date" : "2021-08-24",
  "keywords" :[ "trc dosyası", "trc dosya biçimi", "trc dosyası nedir", "dosya", "trc örneği", "trc dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"TRC dosya formatı ve TRC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"TRC - SQL Server İzleme Dosyası",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## .tr dosyası nedir?
.trc uzantılı bir dosya, bir Miscrosoft SQL sunucusu veritabanının etkinliğinin izleme sonuçlarını içerir. Bu dosyalar bir SQL Server Profiler yazılımı tarafından oluşturulur; genellikle Microsoft SQL Server yazılımı ile paketlenmiştir. Veritabanı yöneticileri, bir dizi veritabanı ifadesini analiz edebilir ve bir tür hata veya uyarıdan şüpheleniliyorsa izleme günlüğünü gözden geçirebilir. Bu dosyalar genellikle bir Windows işletim sistemindeki Program Dosyaları dizini içindeki MSSQL'in tipik LOG klasöründe bulunur.

## TRC dosya formatı
TRC dosya formatı, SQL Server Profiler tarafından, MS SQL sunucusu tarafından son zamanlarda yürütülen ifadelerin yeni bir izini otomatik olarak oluşturmak için kullanılır. SQL Server Profiler, herhangi bir yeni izleme için varsayılan şablonu kullanır. Bununla birlikte, yazılım, belirli olay türlerini izlemek için birkaç önceden tanımlanmış şablon içerir. Ayrıca SQL Server Profiler, izlemelere dahil edilecek olay sınıflarını ve veri sütunlarını tanımlayan şablonlar oluşturmak için kullanılabilir.

### Önceden Tanımlanmış Şablonlar
SQL Server Profiler'da bulunan önceden tanımlanmış bazı şablonların listesi aşağıdadır:
- **SP_Counts**: Zaman içinde saklı yordam yürütme davranışını yakalar.
- **Standart**: Bir iz oluşturmak için genel başlangıç noktası.
- **TSQL**: İstemciler tarafından SQL Server'a gönderilen tüm Transact-SQL ifadelerini ve verilen zamanı yakalar.
- **TSQL_Duration**: İstemciler tarafından SQL Server'a gönderilen tüm Transact-SQL ifadelerini, yürütme sürelerini yakalar ve süreye göre gruplandırır.
- **TSQL_Grouped**: Belirli bir müşteriden veya kullanıcıdan gelen sorguları araştırmak için kullanın.
- **TSQL_Locks**: Kilitlenme sorunlarını gidermek, zaman aşımını kilitlemek ve yükseltme olaylarını kilitlemek için kullanın.
- **TSQL_Replay**: Kıyaslama testi gibi yinelemeli ayarlama yapmak için kullanın.
- **TSQL_SPs**: Saklı yordamların bileşen adımlarını analiz etmek için kullanın.
- **Ayarlama**: Database Engine Tuning Advisor'ın veritabanlarını ayarlamak için bir iş yükü olarak kullanabileceği izleme çıktısı üretmek için kullanın.
### Bir izlemeyi Windows Performans Günlüğü verileriyle ilişkilendirin
SQL Server Profiler, bir Microsoft Windows performans günlüğünü açmak, bir izleme ile ilişkilendirilecek sayaçları seçmek ve MS SQL Server Profiler GUI'sinde izlemenin yanında seçilen performans sayaçlarını görüntülemek için kullanılabilir. Seçili izleme olayıyla ilişkili performans günlüğü verilerini belirtmek için, SQL Server Profiler'ın Sistem Monitörü veri penceresi bölmesinde dikey bir kırmızı çubuk.


## Referanslar ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

