{
  "date" : "2019-10-11",
  "keywords" :[ "wmz dosyası", "wmz dosya biçimi", "wmz dosyası nedir", "dosya", "wmz örneği", "wmz dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMZ Dosya Biçimi - Sıkıştırılmış Windows Meta Dosyası",
  "description":"WMZ dosya formatı ve WMZ dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## WMZ dosyası nedir?

.wmz uzantılı bir dosya, [WMF](/tr/image/wmf/) dosyasının sıkıştırılmış bir sürümüdür ve meta dosyalarını depolamak için kullanılır. Microsoft Office uygulamalarının eski sürümleri tarafından oluşturulan orta düzey bir dosyadır ve çok popüler olarak kullanılmamaktadır. WMZ dosyaları, belgeler [HTML](/tr/web/html/) biçiminde kaydedilirken oluşturulur. Bunlar, gömülü küçük resimler, denklemler vb. içeren belgeleri e-postayla gönderirken de oluşturulabilir. WMZ dosyalarını açabilen uygulamalar Corel Winzip ve Apple Archive Utility'yi içerir (ancak bunlarla sınırlı değildir).

## WMZ Dosya Biçimi

WMZ dosyaları [Gzip](/tr/compression/gz/) sıkıştırılmıştır ve içinde [WMF](/tr/image/wmf/) içerir. Gzip, arşivin sıkıştırılması için DEFLATE algoritmasını kullanır. GZIP, tek tek dosyalar yerine arşivi tamamlamak için sıkıştırma algoritması uyguladığı için [ZIP](/tr/compression/zip/) arşiv biçiminden farklıdır. Dosya formatı şunlardan oluşur:

* Dosya Başlığı
* İsteğe Bağlı Başlıklar
* Sıkıştırılmış Veri
* Dosya Altbilgisi

Internet Engineering Task Force (IETF) tarafından yayınlanan GZIP dosya biçimi [özellikler sürüm 4.3](https://datatracker.ietf.org/doc/html/rfc1952), dosya biçimi hakkında ayrıntılı bilgiler içerir.

## Referanslar

* [RFC1952: GZIP dosya biçimi belirtimi](https://datatracker.ietf.org/doc/html/rfc1952), [IETF](https://www.ietf.org) tarafından
* [Windows Meta Dosyası - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

