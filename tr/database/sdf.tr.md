{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "sdf dosyası","sdf dosyası nedir","sdf dosyası nasıl açılır", "uzantı", "dosya", "sdf dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi ", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"SDF dosya formatı ve SDF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"SDF - SQL Server Kompakt Veritabanı Dosyası",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## SDF dosyası nedir?
.sdf uzantılı bir dosya, kompakt ilişkisel veritabanı olarak da bilinen Microsoft SQL Server Compact (SQL CE) veritabanını içerir; mobil cihazlar ve masaüstleri için yapılan uygulamalar için Microsoft tarafından üretilmiştir. Hem 32 hem de 64 bit işletim sistemini destekler ve veritabanının tüm içeriği tek bir SDF dosyasına dahildir ve 4 GB'tan fazla disk alanı kaplayabilir. Güvenlik amacıyla, bir .sdf dosyası 128 bit şifreleme ile şifrelenebilir. SQL CE çalışma zamanı, .sdf dosyasına paralel çok kullanıcılı erişimi ayarlar. SDF dosyası **QuickOnce** aracılığıyla kopyalanabilir veya yalnızca sistem dağıtımı için hedefe kopyalanabilir.

## SDF Dosya Biçimi
Bir SDF dosyası, genellikle kompakt ilişkisel veritabanı olarak adlandırılan bir veritabanı içerir. Bir SDF dosyası, veritabanıyla ilgili tüm bilgileri içerir ve SQL Server Compact, .sdf dosyalarını yönetmek için kullanılan hafif ve ücretsiz bir veritabanı motorudur. .sdf dosya boyutu 4 GB boyut sınırını aşmamalıdır. SDF dosyaları saklı yordamlar, tetikleyiciler veya görünümler hakkındaki bilgileri saklamaz. Bir SQL CE veritabanı kullanan uygulamaların ADO.NET bağlantı dizesinde bir SDF dosyasının yolunu belirtmesi gerekmez, bunun yerine uygulama için derleme bildiriminde tanımlanmakta olan veri dizinini tanımlayan |DataDirectory|\database_name.sdf olarak belirtilebilir.
.sdf adlandırma kuralı isteğe bağlıdır ve dosyayı kaydetmek için herhangi bir uzantı kullanılabilir. Veritabanı dosyası için parola ayarlamak isteğe bağlı bir adımdır. Veritabanını sıkıştırmak veya onarmak için dosya **sıkıştırılmış/onarılmış veritabanı** seçeneğiyle kaydedilmelidir.

## Referanslar

* [SQL Server Kompakt - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [ASP.NET Web Uygulamaları için SQL Server Compact Kullanımı](https://learn.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


