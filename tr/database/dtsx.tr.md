{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DTSX dosya formatı ve DTSX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"DTSX Dosya Biçimi - SQL Server DTS Ayarları Dosyası",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## DTSX dosyası nedir?

.dtsx (Veri Dönüştürme Hizmetleri Paketi XML) uzantılı bir dosya, Microsoft SQL tarafından verilerin bir veritabanından diğerine aktarılması için veri taşıma adımlarına/kurallarına atıfta bulunmak için kullanılan bir Veri Dönüştürme Hizmetleri (DTS) dosyasıdır. Bu, başlangıç ve varış noktaları arasındaki veri aktarımı sırasında gerekli olabilecek dönüştürmeleri ve isteğe bağlı işleme adımlarını içerir. Microsoft SQL Server'ın bir bileşeni olan SQL Server Integration Services (SSIS), veritabanı sunucuları arasında veri işleme adımlarını belirlemek için DTSX dosyalarını kullanır. DTSX dosyaları Microsoft SQL Server 2019 ile açılabilir.

## DTSX Dosya Biçimi

Veritabanı sunucuları arasındaki veri hareketi, bu işlem sırasında verilerin bütünlüğünü sağlamak için kurallar ve işlem adımları gerektirir. SSIS, bir kuruluştaki farklı kaynaklardan verileri taşımak ve uyumlu hale getirmek için tüm bu faaliyetlerin uygun bir şekilde gerçekleşmesini sağlar. DTSX'in geldiği yer burasıdır ve bu adımlar boyunca takip ettiği gibi verilerin işlenebileceği adımları oluşturmak için SSIS tarafından kullanılacak yapıları tanımlar.

DTSX tarafından açıklanan veri akışı aşağıdaki görüntüde gösterildiği gibidir.

{{< figure src="../DataFlowDTSX.png" alt="Veri Akışı DTSX" >}}

DTSX, [XML](/tr/web/xml/) tabanlıdır ve [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd) içinde belgelenmiştir. DTSX XML'in geliştirilmiş yeniden düzenlemesi, yapılara yeni öznitelikler, adlandırılmış özelliklerin üst XML öznitelikleri olarak değiştirilmesini, çoğu öznitelik değeri için varsayılanları belirlemeyi ve bir üst öğe içine yinelenen öğelerin yerleştirilmesini içeren DTSX 2.0'dır. DTSX yapıları, bu [XML Şemaları](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc) kullanılarak açıklanır ve yapısal biçim şöyledir: kiler-metin XML.

## Referanslar

* [DTSX Formatı - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [DTSX 2 Biçimi - Microsoft Tarafından](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

