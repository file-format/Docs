{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "uzantı", "dosya", "biçim", "sistem", "Dynamic Link Library", "ayarlar", "programlar", "bilgisayar", "uygulama"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - Dinamik Bağlantı Kitaplığı",
  "description":"DLL dosya formatı ve DLL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## DLL dosyası nedir? ##

Bir DLL dosyası veya Dinamik Bağlantı Kitaplığı, bir yürütülebilir dosya türüdür. Cihazınızda en sık bulunan uzantı dosyalarından biridir ve genellikle Windows'unuzdaki System32 klasöründe depolanır. DLL uzantı dosyası Microsoft tarafından geliştirilmiştir ve onlar tarafından yaygın olarak kullanılmaktadır. Yüksek bir popülerlik kullanıcı derecelendirmesine sahiptir. DLL, windows sunucusu tarafından bir program/uygulama için tasarlanan ve uygulanan *sürücüler/prosedürler/işlevler/özellikler* içeren bir raf gibi çalışır. Tek bir DLL dosyası, çeşitli Windows programları arasında da paylaşılabilir. Bu uzantı dosyaları, programda dosya yazma ve okuma, kurulumunuzun dışındaki diğer cihazlara bağlanma gibi çeşitli işlevleri etkinleştirmek ve çalıştırmaktan sorumlu olduklarından, Windows programlarının cihazınızda sorunsuz çalışması için hayati önem taşır.
Ancak bu Dosyalar yalnızca herhangi bir Windows sürümünü (Windows 7/Windows 10/vb.) destekleyen bir cihazda açılabilir ve bu nedenle doğrudan Mac OS'yi destekleyen bir cihazda açılamaz. (Mac OS'de bir DLL dosyası açmak isterseniz, çeşitli harici uygulamalar bunları açmanıza yardımcı olabilir.)


## DLL Dosya Biçimi ##

DLL dosyası Microsoft tarafından geliştirilmiştir ve türü temsil eden ".dll" uzantısına sahiptir. Windows 1.0 sunucusunun ve ötesinin ayrılmaz bir parçası olmuştur. İkili bir dosya türüdür ve Microsoft Windows'un tüm sürümleri tarafından desteklenir. Bu dosya türü, programları yeniden bağlamaya gerek kalmadan program kitaplıklarında ayrı ve bağımsız düzenlemelere veya değişikliklere izin vermek için Windows programları içinde paylaşılan bir kitaplık sistemi oluşturmak amacıyla oluşturulmuştur.


## DLL Örneği ##

Bir DLL giriş noktası için örnek kod aşağıda bulunabilir:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## Referans ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
