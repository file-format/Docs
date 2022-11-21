{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MDMP Dosyası - Windows Minidump Dosya Biçimi",
  "description":"MDMP dosya formatı ve MDMP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## MDMP dosyası nedir?

Bir MDMP dosyası, Microsoft Windows'taki bir uygulamanın, uygulama anormal şekilde kapandığında veya çöktüğünde oluşturulan bir bellek dökümüdür. Çökmenin nedenini ayıklamak için kullanılabilecek bilgileri ve veri dökümlerini içerir. MDMP dosyaları, Java, C++, .NET ve diğerleri gibi herhangi bir platform tarafından oluşturulan uygulamalara uygulanabilir. MDMP'ye ek olarak,

MDMP dosyalarını açabilen uygulamalar, Microsoft Visual Studio Debugger'ı içerir.

## MDMP Dosya Biçimi

MDMP dosyaları diske ikili dosyalar olarak kaydedilir ve Microsoft Visual Studio hata ayıklayıcı ile açılabilir. Kilitlenmenin nedenini belirlemeye yardımcı olmak için aşağıdaki bilgileri içerir.

* Dur mesajının, parametrelerinin ve diğer verilerin ayrıntıları
* Yüklü sürücülerin listesi
* Çalışmayı durduran işlemci için işlemci bağlamı (PRCB)
* Durdurulan işlem için işlem bilgisi ve çekirdek içeriği (EPROCESS)
* Durdurulan iş parçacığı için işlem bilgileri ve çekirdek içeriği (ETHREAD)
* Duran iş parçacığı için çekirdek modu çağrı yığını

Bu bilgi, ne olduğunu bulmaya, sorunu çözmeye ve tekrar olmasını önlemeye yardımcı olur.

### Mini dökümü analiz et

Windows, bir bellek dökümü dosyası oluşturmak için önyükleme biriminde bir disk belleği dosyası gerektirir. Disk belleği dosyası önyükleme biriminde oluşturulur ve boyutu en az 2 megabayt (MB) olmalıdır. Döküm dosyası, bir uygulama çöktüğünde oluşturulur. İkinci bir sorun olması durumunda, bir önceki korunurken ikinci bir küçük bellek dökümü dosyası oluşturulur. Üzerine yazmayı önlemek için döküm dosyasının adı farklıdır.

Windows, %SystemRoot%\Minidump klasöründeki tüm bellek dökümü dosyalarının bir listesini tutar. MDMP dosyalarını aşağıdaki adımlarda listelendiği gibi Visual Studio Debugger'da çalıştırarak analiz edebilirsiniz.

## Visual Studio'da bir MDMP dosyasını nasıl açarım?

Bir MDMP dosyasını Visual Studio'da açmak için aşağıdaki adımlar kullanılabilir.

* Visual Studio'da Dosya menüsünden Aç | Kilitlenme Dökümü.
* Açmak istediğiniz döküm dosyasına gidin.
* Aç'ı seçin.

## Referans

* [Bir çökme meydana geldiğinde Windows tarafından oluşturulan küçük bellek dökümü dosyası nasıl okunur](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -dosya)

