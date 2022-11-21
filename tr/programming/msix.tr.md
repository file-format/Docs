{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - MSIX dosyası nedir?",
  "description":"MSIX dosyası ve MSIX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## MSIX dosyası nedir?

MSIX dosyası, Windows 10'da uygulama oluşturmak ve dağıtmak için kullanılan bir Windows uygulama paketleme biçimidir. Bu, sonunda aşamalı olarak kaldırılacak olan [APPX](/tr/programming/appx/) ve MSI ile karşılaştırıldığında modern paket dosyası biçimidir. bu yeni dosya formatına. Win32, WPF ve Windows Forms uygulamalarının dağıtımı için kullanılabilir. MSIX dosyaları güvenilirdir ve ağ ve disk alanı optimizasyonunu hedefler. Geliştiriciler, programları Microsoft Mağazası (önceden Windows Mağazası olarak biliniyordu) aracılığıyla son kullanıcılara dağıtmak için bunları kullanır.

## MSIX Dosya Biçimi - Daha Fazla Bilgi

MSIX dosyaları [ZIP](/tr/compression/zip/) ile sıkıştırılmıştır ve tüm dosyalar paketlenmiş dosyanın içindedir. Uygulamayla ilgili dosyalara ek olarak, MSIX dosyası, uygulama yüklemesiyle ilgili bilgileri içeren [.xml](/tr/web/xml/) yapılandırma dosyalarını içerir.

## Bir MSIX paketinin içinde neler var?

Bir MSIX paketi aşağıdaki dosyalardan oluşur.

* `AppxBlockMap.xml` - Paket blok eşleme dosyası olarak bilinir ve pakette depolanan her veri bloğu için dizinler ve kriptografik karmalar içeren uygulama dosyalarının bir listesini içeren bir XML belgesidir.
* `AppxManifest.xml` - Bir MSIX uygulamasının konuşlandırılması, görüntülenmesi ve güncellenmesi için gerekli bilgileri içeren bir XML belgesi. Bu bilgiler, paket kimliği, paket bağımlılıkları, gerekli yetenekler, görsel öğeler ve genişletilebilirlik noktalarını içerir.
* `AppxSignature.p7x` - Paket imzalandığında oluşturulan bir dosya. Tüm MSIX paketlerinin kurulumdan önce imzalanması gerekir. AppxBlockmap.xml ile platform paketi kurabilir ve doğrulanabilir.

## Referanslar

* [MSIX'e Genel Bakış](https://docs.microsoft.com/en-us/windows/msix/overview)
* [Microsoft Visual Studio kullanarak APPX dosyaları oluşturun](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

