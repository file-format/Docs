{
  "date" : "2021-08-13",
  "keywords" :[ "sdi dosyası", "sdi dosya biçimi", "sdi dosyası nedir", "dosya", "sdi örneği", "sdi dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"SDI dosya formatı ve SDI dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"SDI - Windows Sistem Dağıtım Görüntü Dosyası",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## SDI dosyası nedir?
.sdi uzantılı dosya bir yükleme blobu, önyükleme blobu ve parça blobu içerir; Windows Embedded Studio tarafından Windows yüklemek ve yüklemek için RAM diskleri veya önyükleme diskleri oluşturmak için yaygın olarak kullanılır. SDI, Sistem Dağıtım Görüntüsü için kısaltılmıştır. Windows Embedded Studio, Windows için disk görüntüleri oluşturmak için kullanılan bir programdır. Aslında bu program, SDI Dosya Yöneticisi programını ve **sdimgr.exe** adlı bir komut satırı aracını içerir, her ikisi de SDI görüntülerini derlemek, oluşturmak ve düzenlemek için kullanılabilir.

## SDI dosya formatı
SDI dosya formatı, bir sistemi başlatmak için bir sanal diskin kullanılmasını sağlamak için yaygın olarak kullanılır. Microsoft Windows'un bazı sürümleri, bir SDI dosyasını belleğe yüklemek ve ardından ondan önyükleme yapmak için önemli olan **RAM önyüklemesini** etkinleştirir. SDI dosya formatı ayrıca PXE'yi (Önyükleme Öncesi Yürütme Ortamı) kullanarak ağ önyüklemesi için kendisini etkinleştirir. Ayrıca sabit disk görüntüleme için kullanılıyor.
### SDI dosya bölümleri
SDI dosyasının kendisi aşağıdaki bölümlere ayrılabilir:
- **Boot BLOB**: Bu, gerçek önyükleme programı olan STARTROM.COM'u içerir. Bu, bir sabit diskin önyükleme sektörüne benzer.
- **BLOB'u Yükle**: Bu genellikle NTLDR içerir ve önyükleme BLOB'u tarafından başlatılır.
- **Parça BLOB**: Bu, gerçek önyükleme çalışma zamanını içerir; çalışma zamanının kök dizininde bulunması gereken boot.ini ve ntdetect.com dosyalarını da içerir.
- **Disk BLOB**: Bu, bir MBR ile başlayan düz HDD görüntüsüdür. Önyükleme yerine sabit sürücü görüntüleme için kullanılır. Ayrıca, Microsoft'un yardımcı programlarıyla yalnızca Disk BLOB'ları monte edilebilir.


## Referanslar

* [Sistem Dağıtım Görüntüsü - Wikipedia'dan](https://en.wikipedia.org/wiki/System_Deployment_Image)


