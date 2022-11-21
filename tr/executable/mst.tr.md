{
  "date" : "2021-06-30",
  "keywords" :[ "mst dosyası", "mst dosya biçimi", "mst dosyası nedir", "dosya", "mst örneği", "mst dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"MST dosya formatı ve MST dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"MST - Windows Yükleyici Paket Dosyası",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## MST dosyası nedir?
.mst uzantılı dosyalar, bir MSI paketinin içeriğini dönüştürmek için kullanılır. Özel ayarları mevcut bir MSI dosyasına uygulamak için genellikle sistem yöneticileri tarafından kullanılırlar. MST dosyaları, grup ilkeleri gibi yazılım dağıtım sistemlerinde orijinal MSI paketi ile birlikte kullanılır. MST dosyaları genellikle yazılım geliştirmede ve yazılımın geliştirme sürümlerini yapılandırmak için test etmede kullanılır.

## MST dosya formatı
Bir dosyada Microsoft Windows Installer kullanan programların yükleme seçeneklerini toplamak için bir MST veya Transform dosyası kullanılır. Bu dosyalar genellikle Yükleyici (MSIEXEC.EXE) komut satırında veya yazılım yüklemesinin Grup İlkesi'nde kullanılır; bir Microsoft Active Directory etki alanında. MST dosyaları, sarılmış yürütülebilir yükleyicilerle de kullanılabilir. Genel bir durum, birisinin komut satırı parametrelerini sarılmış yükleyiciye iletmek istemesidir. Bunu yapmak için WRAPPED_ARGUMENTS özelliğini özellik tablosuna ekleyen bir MST dosyasına ihtiyacınız var. Bu dosyalar genel düzenleyiciler kullanılarak oluşturulamaz veya düzenlenemez. Bu amaç için özel araçlar mevcuttur.

### MST dosyaları nasıl kullanılır?
MST dosyaları çeşitli araçlar kullanılarak oluşturulabilir ve Ocra genellikle bir MST dosyası oluşturmak için kullanılır. Ardından ayarlar ihtiyaca göre özelleştirilebilir ve bunları belirli bir konuma kaydedebilir. Bundan sonra MST dosyaları, MSI dosyalarıyla birlikte kullanılabilir. Bu dosyaları test etmek isterseniz; komut satırında aşağıdaki sözdizimini kullanın

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMS özelliği

Ayrıca, paketi yüklerken yükleyicinin uyguladığı dönüşümlerin bir listesi olan Windows yükleyicinin **TRANSFORMS** özelliğini de kullanabilirsiniz. Yükleyici, dönüştürmeleri TRANSFORM özelliğinde listelendikleri sırayla yürütür. Dönüşümler, .mst uzantılı dosya adına veya tam yola göre belirtilebilir. Birden fazla dönüştürme belirtmek için, aşağıdaki örnekte olduğu gibi her bir dosya adını veya noktalı virgülü ayırın.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Referanslar

* [MST Dönüşüm Dosyaları](https://www.exemsi.com/documentation/mst-transformation-files/)
* [TRANSFORMS özelliği](https://docs.microsoft.com/en-us/windows/win32/msi/transforms)


