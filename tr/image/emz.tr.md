{
  "date" : "2019-10-11",
  "keywords" :[ "emz dosyası", "emz dosya biçimi", "emz dosyası nedir", "dosya", "emz örneği", "emz dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMZ Dosya Biçimi - Bir Windows Sıkıştırılmış Gelişmiş Meta dosyası",
  "description":"EMZ dosya formatı ve EMZ dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## EMZ dosyası nedir?

.emz uzantılı bir dosya, Gelişmiş Meta Dosyasının ([EMF](/tr/image/emf/) dosyası) sıkıştırılmış bir kapsayıcısıdır. Bunlar, UNIX ve LINUX işletim sistemlerinde yaygın olarak kullanılan sıkıştırma yöntemi olan [GZIP](/tr/compression/gz/) sıkıştırma tekniği kullanılarak sıkıştırılır. ZIP bağlantısını kaldır (/tr/compression/zip/), GZIP, tek tek dosyaları sıkıştırmak yerine arşivi bir bütün olarak sıkıştırır. EMZ dosyaları, EMF dosyalarına kıyasla boyut olarak daha küçüktür ve çevrimiçi dosya paylaşımı sırasında hızlı aktarıma yardımcı olur. EMZ dosyalarını açabilen uygulamalardan bazıları Microsoft Visio 2019, Microsoft Office 2019, XnView MP ve File Viewer Plus'ı içerir.

## EMZ Dosya Biçimi

EMZ dosyaları [Gzip](/tr/compression/gz/) sıkıştırılmıştır ve içinde [EMF](/tr/image/emf/) içerir. Gzip, arşivin sıkıştırılması için DEFLATE algoritmasını kullanır ve sıkıştırma uygulamasında farklıdır. Bir EMZ dosyasının sıkıştırılmış hali, GNU Zip gibi GZip sıkıştırma yardımcı programları kullanılarak açılabilir. Dosya formatı şunlardan oluşur:

* Dosya Başlığı
* İsteğe Bağlı Başlıklar
* Sıkıştırılmış Veri
* Dosya Altbilgisi

Internet Engineering Task Force (IETF) tarafından yayınlanan GZIP dosya biçimi [özellikler sürüm 4.3](https://datatracker.ietf.org/doc/html/rfc1952), dosya biçimi hakkında ayrıntılı bilgiler içerir.

## Referanslar

* [RFC1952: GZIP dosya biçimi belirtimi](https://datatracker.ietf.org/doc/html/rfc1952), [IETF](https://www.ietf.org/) tarafından
* [Windows Meta Dosyası - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

