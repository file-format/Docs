{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ADE dosya formatı ve ADE dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"ADE - Proje Uzantı Dosyasına Erişim",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## ADE dosyası nedir?

.ade uzantılı bir dosya, Microsoft Access ADP proje dosyasında yer alan bilgilerin derlenmiş çıktısını içeren bir Microsoft Access Projesi dosyasıdır. Visual Basic for Applications (VBA) dışındaki Access proje dosyasındaki bilgiler, ADE dosyalarında derlenmiş biçimde bulunur. Veriler, dosya boyutunu azaltmak ve Access'te performansı artırmak için bu dosyalarda sıkıştırılmış biçimde depolanır. ADE, Access proje dosyasının derlenmiş çıktısı olduğundan, projenin parçası olan herhangi bir VBA kaynak kodu, çıktının bir parçası olmasına izin vermeyerek korumalı kalır. ADE dosyaları Microsoft Access 365'te açılabilir.

## ADE Dosya Biçimi - Daha Fazla Bilgi

ADE, diskte ikili dosyalar olarak saklanan derlenmiş Access Veritabanı dosyalarıdır. Bu dosyaların dahili dosya yapısı bilinmemektedir.

ADE dosyaları, bu dosyaları oluşturmak için kullanılan Microsoft Access sürümüne bağlı olarak açılışta sorunlar oluşturabilir. Microsoft Access 2010'un 64 bit sürümünü kullanan ve MDE, [ACCDE](/tr/database/accde/) veya ADE dosyaları olarak derlenen Access veritabanlarının Microsoft Access 2021 Service Pack 1'de (SP1) yeniden derlenmesi gerekir. Access 2010 SP1 ile düzgün çalışın. Bu sorun, Access 2010 SP1'in VBE7.dll dosyasının (sürüm 7.00.1619) daha yeni bir sürümünü kullanması nedeniyle oluşur.

## Referanslar

* [Access ADE Dosyalarıyla İlgili Sorun](https://docs.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Hangi Access Dosya Biçimlerinin Kullanılacağı](https://support.microsoft.com/en-us/office/what-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

