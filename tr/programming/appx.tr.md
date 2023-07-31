{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - APPX dosyası nedir?",
  "description":"APPX dosya formatı ve APPX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## APPX dosyası nedir?

Bir APPX dosyası, bir uygulamanın dağıtımı ve kurulumu için kullanılan dağıtılabilir bir paket dosyası biçimidir. Microsoft Windows Store'da yayınlanmak üzere Windows 8 ile tanıtıldı. Bir Windows uygulamasını yüklemek için gereken tüm dosyaları içerir. Bunlar meta verileri, dosyaları ve kimlik bilgilerini içerir. Daha modern bir paketleme dosyası formatı, şu anda APPX'e kıyasla daha yaygın olarak kullanılan MSIX'tir.

## APPX Dosya Biçimi - Daha Fazla Bilgi

APPX dosyaları, [ZIP](/tr/compression/zip/) dosya biçiminde sıkıştırılmış dosyalar olarak kaydedilir. Bu, paketin tamamını, Microsoft Store'a yüklenmesi kolay, küçültülmüş dosya boyutuna sahip bir arşiv dosyası haline getirir.

## Bir APPX dosyasındaki dosyalar nasıl görüntülenir?

Bir APPX dosyası içindeki içerikleri veya dosyaları görüntülemek için aşağıdaki adımlar izlenmelidir.

1. APPX dosyaları sıkıştırılmış ZIP dosyaları olarak saklandığından, dosyayı .zip uzantısına yeniden adlandırın
1. APPX dosyasında bulunan dosyaları çıkarmak için 7-Zip, WinZip veya WinRAR gibi herhangi bir açma aracını kullanın.

## APPX dosyası nasıl oluşturulur?

APPX dosyaları oluşturmak için kullanılabilecek iki yöntem vardır.

1. MakeApp.exe'yi kullanma - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) her ikisini de oluşturmak için kullanılır uygulama paketleri (.msix veya .appx) ve uygulama paketi paket dosyaları .msixbundle veya .appxbundle). Ayrıca, bir uygulama paketinden dosya ayıklayabilir. MakeApp.exe, Windows 10 SDK ile birlikte sunulur ve komut isteminden kullanılabilir.
1. Microsoft Visual Studio'yu kullanma - Geliştiriciler genellikle Microsoft Visual Studio'yu kullanarak [APX dosyaları oluşturur](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview). Uygulama geliştirme tamamlandıktan ve uygulama yayınlanmaya hazır hale geldiğinde, Visual Studio içinden yayınlanarak APPX paket dosyası oluşturulabilir.

## Referanslar

* [MakeAppx.exe ile bir MSIX paketi veya paketi oluşturun](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Microsoft Visual Studio kullanarak APPX dosyaları oluşturun](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

