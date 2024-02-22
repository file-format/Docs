{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ Dosyası - EAZ dosyası nedir ve nasıl açılır?",
  "description":"EAZ dosya formatı ve EAZ dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-trz"
}
},
  "lastmod" : "2023-12-23"
}

## .EAZ dosyası nedir?

EAZ dosyası, ESRI tarafından harita keşfi, görselleştirme ve paylaşım için geliştirilen ücretsiz bir uygulama olan ArcGIS Explorer tarafından kullanılan bir Eklenti dosyasıdır. Bir [XML file](/web/xml/), derlenmiş kod ve eklenti için gerekli destekleyici dosyaları içeren sıkıştırılmış bir dosya arşivi içerir. Bu dosyalar, yeni düğmeler, takılabilir pencereler ve diğer uzantıları birleştirerek yazılımın temel işlevselliğini genişletmek için kullanılır.

## EAZ Dosya Formatı - Daha Fazla Bilgi

EAZ dosyaları, ArcGIS Explorer'da özel işlevler oluşturmak için tasarlanmış bir geliştirme kiti olan ArcGIS Explorer SDK'nın kullanılmasıyla oluşturulur. Bu dosyalar, içeriklerini verimli bir şekilde paketlemek için [ZIP](/compression/zip/) sıkıştırmasını kullanır. Arşivin merkezinde, **Addins.xml** dosyası kök dizinde bulunur ve EAZ dosyasına gömülü çeşitli özelleştirmelerin ana hatlarını çizen ve ayrıntılarını veren hayati bir bileşen olarak hizmet eder.

Addins.xml dosyası esas olarak bir yol haritası görevi görür ve EAZ dosyasının ArcGIS Explorer'a sunduğu belirli geliştirmeler, değişiklikler ve uzantılara ilişkin bilgiler sunar. Bu kapsamlı yapı sayesinde geliştiriciler yeni özellikleri, düğmeleri ve kenetlenebilir pencereleri kapsayabilir ve sorunsuz bir şekilde entegre edebilir, böylece ArcGIS Explorer uygulamasının genel işlevselliğini ve kullanıcı deneyimini geliştirebilir.

## Referanslar

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
