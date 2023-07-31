{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - Rapor Tanımlama Dili İstemci Tarafı",
  "keywords" :[ "rdlc", "rapor tanımlama dili", "mkv formatı", "XSD", "rapor tanımlama dili istemci tarafı"],
  "description":"SQL Server Reporting Services rapor tanımının XML temsili olan RDLC dosya biçimi hakkında bilgi edinin.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## RDLC dosyası nedir? ##

RDLC, Rapor Tanımlama Dili İstemci tarafı anlamına gelir. Aslında Microsoft raporlama teknolojisi kullanılarak oluşturulan rapor dosyasının bir uzantısıdır. Bu dosyaları oluşturmak için Rapor Tasarımcısı'nın SQL Server 2005 sürümü kullanılır. İstemci tarafındaki **ReportViewer** denetimi, RDLC raporlarını doğrudan yürütebilir.

## RDL ve RDLC Dosyaları
|.rdl Dosyaları |.rdlc dosyaları|
---|---|
|RDL dosyaları, Rapor Tasarımcısının SQL Server 2005 sürümü tarafından oluşturulur|RDLC dosyaları, Rapor Tasarımcısının Visual Studio 2005 sürümü tarafından oluşturulur|
|SQL Server Raporlama Servislerinde kullanılır|Visual Studio'da kullanılır|
|Uzak bir rapordur|Yerel bir rapordur|
|Çalıştırmak için bir Raporlama Hizmetleri örneğine ihtiyacınız var|Raporlama Hizmetleri örneğine gerek yok|

## Müşteri Raporu Tanımı (.rdlc) Dosyaları Oluşturma
ReportViewer kontrolü, kontrolün yerleşik işleme yeteneğini kullanarak müşteri rapor tanımı (.rdlc) dosyalarını çalıştırmak için kullanılır. Yerel işleme modunda çalıştırdığınız istemci raporları, uygulama projenizde kolayca oluşturulabilir. Raporun oluşturulmasına yönelik yaklaşımlar şunlardır:

- Yeni bir müşteri raporu tanımı (.rdlc) oluşturmak için **Rapor Sihirbazı**'nı kullanın.

- Visual Studio'yu kullanarak yeni bir müşteri raporu tanımı (.rdlc) dosyası oluşturun.

- Programlı olarak bir rapor tanımı oluşturun.


Bir raporu yalnızca bir **ReportViewer** denetiminde çalıştırarak önizleyebilirsiniz. Lütfen rapor tanımını istediğiniz zaman açıp düzenleyebileceğinizi ve ardından sonuçları kontrol etmek için uygulamayı oluşturabileceğinizi veya dağıtabileceğinizi unutmayın.

## Referanslar ##

- [İstemci Raporu Tanımı (.rdlc) Dosyaları Oluşturma](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

