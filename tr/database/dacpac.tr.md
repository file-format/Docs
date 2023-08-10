{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Veri Katmanı Uygulama Paketi" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DACPAC dosya formatı ve DACPAC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"DACPAC - Veri Katmanı Uygulama Paketi",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## DACPAC dosyası nedir?

.dacpac (Veri Katmanı Uygulama Paketi anlamına gelir) uzantılı bir dosya, Microsoft SQL Server veri katmanı uygulamasıyla oluşturulan ve veritabanı nesnelerinin temsili için veritabanı modelini içeren bir veritabanı dosyasıdır. Veritabanının tüm modelini içerdiğinden, modelde bulunan ayrıntılardan bir veritabanını geri yüklemek için kullanılır. DACPAC dosyaları, veritabanını geri yüklemek için genellikle müşterinin tesislerinde kurulum için dağıtım ekiplerine teslim edilir. Bunlar ile açılabilir
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## DACPAC Dosya Biçimi - Daha Fazla Bilgi

DACPAC veri paketi dosyaları, bir veritabanını geri yüklemek için kullanılan tablolar ve görünümler gibi veritabanı modeli hakkında bilgiler içeren birkaç [XML](/tr/web/xml/) dosyası içeren sıkıştırılmış ZIP dosyalarıdır. DACPAC dosyalarının içeriğini görüntülemek için, dosyaları .dacpac'tan [.zip](/tr/compression/zip/) olarak yeniden adlandırın ve herhangi bir açma yardımcı programını kullanarak zip arşivini çıkarın.

Aşağıda, bir DACPAC dosyası içinde bulunan birkaç dosya bulunmaktadır.

* [İçerik_Türleri].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Kaynak.xml

* model.xml

DACPAC'ın DATA ve diğer sunucu düzeyinde nesneleri içermediğine dikkat edilmelidir. Dosya, SSDT projesinde tutulabilecek tüm nesne türlerini içerebilir.

## Referanslar

* [Veri Katmanı Uygulamaları - Avantajlar](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications?view=sql-server-ver15)
* [Veri Katmanı Uygulamasını Dağıtma - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [DACPAC Dosyası nasıl oluşturulur?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

