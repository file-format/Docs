{
  "date" : "2021-08-11",
  "keywords" :[ "wim dosyası", "wim dosya biçimi", "wim dosyası nedir", "dosya", "wim örneği", "wim dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"WIM dosya formatı ve WIM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"WIM - Windows Görüntüleme Formatı Dosyası",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## WIM dosyası nedir?
.wim uzantılı dosyalar ilk kez Windows Vista'da görüldü. WIM, tipik olarak Microsoft Windows Vista'da tanıtılan dosya tabanlı bir görüntüleme formatına aittir. Tek bir disk görüntüsünün çeşitli bilgisayar platformlarına dağıtılmasını sağlar. WIM dosyaları, işletim sistemi görüntüsünü yeniden başlatmadan güncellemeler, sürücüler ve bileşenler gibi dosyaları yönetmek için kullanılır. AQ WIM dosyası, diğer disk dosyası formatlarına çok benzeyen bir dizi dosya ve ilişkili meta verileri içerir.

## WIM dosya biçimleri
WIM dosya biçimi, VHD veya IS gibi sektör tabanlı biçimler gibi değildir, aslında dosya tabanlıdır, yani bir WIM'deki temel bilgi birimi bir dosyadır. Dosya tabanlı olmanın temel yararı, dosya sistemi ağacında birden çok kez başvurulan bir dosyanın tek eşgörünümlü depolanması ve donanım bağımsızlığıdır. dosya. WIM dosyaları, benzersiz adlarıyla veya sayısal dizinleriyle başvurulan birden çok disk görüntüsünü depolayabilir.
### Sıkıştırma algoritmaları için destek
WIM, azalan hız ve artan oranda aşağıdaki sıkıştırma algoritması ailelerini destekler:
- XPRESS
- LZX
- LZMS
- Katı sıkıştırma.
İlk üç aile LZ77 tabanlıyken Katı sıkıştırma, WIMGAPI Windows 8 ve DISM Windows 8.1'de LZMS ile birlikte tanıtıldı.
### WIM dosya formatı için araçlar
Aşağıdaki araçlar genellikle WIM dosya biçimini destekler:

- **ImageX**: Windows Görüntüleme Biçiminde Windows disk görüntülerini düzenlemek, oluşturmak ve dağıtmak için kullanılan bir komut satırı aracı. İlgili WIMGAPI ile birlikte, ücretsiz Windows Otomatik Kurulum Kitinin bir parçası olarak dağıtılır. Windows Vista'dan başlayarak, Windows Kurulumu, Windows'u yüklemek için WAIK API'sini kullanır.
- **DISM**: Windows 7 ve Windows Server 2008 R2'de tanıtılan ve ister çevrimiçi bir görüntü, ister bir klasör veya WIM dosyası içindeki çevrimdışı bir görüntü olsun, bir Windows yükleme görüntüsü üzerinde hizmetle ilgili görevleri gerçekleştirebilen bir araç. bu araç, görüntüleri takma ve çıkarma, çevrimdışı bir görüntüye bir aygıt sürücüsü ekleme ve çevrimdışı bir görüntüde yüklü aygıt sürücülerini sorgulama yeteneğine sahipti.
 




## Referanslar


* [Windows Görüntüleme Biçimi - Wikipedia'dan](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


