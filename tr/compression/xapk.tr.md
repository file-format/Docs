{
  "date" : "2021-04-11",
  "keywords" :[ "xapk dosyası", "xapk dosya biçimi", "xapk dosyası nedir", "dosya", "xapk örneği", "xapk dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAPK - Meta Paket Dosya Biçimi",
  "description":"XAPK dosya formatı ve XAPK dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XAPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-11"
}

## XAPK dosyası nedir?

.xapk uzantılı bir dosya, Android uygulamalarını mobil cihazlara yüklemek için kullanılan sıkıştırılmış bir paket dosyasıdır. APK'yi ve kurulum için gereken ek ilişkili dosyaları içeren bir kapsayıcı dosya biçimidir. İlişkili diğer dosya, uygulamanın çalışır durumda kalması için gerekli olan grafikler, medya dosyaları ve uygulama verileri gibi ek dosyaları depolayan bir OBB dosyasıdır. XAPK dosyaları Google Play tarafından desteklenmez ve yalnızca üçüncü taraf Android uygulama indirme web sitelerinde dağıtılmak için kullanılır. Bunlar, XAPK Installer kullanılarak bir Android cihaza kurulabilir.

## XAPK Dosya Biçimi

XAPK dosyaları, standart [ZIP](/tr/compression/zip/) dosya biçimi kullanılarak sıkıştırılır. Bunlar, WinZIP gibi standart bir sıkıştırma/açma yazılımı kullanılarak çıkarılabilir. XAPK dosyası diske çıkarıldıktan sonra, klasörde aşağıdaki dosyaları içerir.

* APK - Uygulamayı Android cihazlara yüklemek için standart kurulum dosyası
* OBB - İlgili kaynak dosyalarını içeren ek dosya

## Referanslar

* [Android Paket Dosyası](https://en.wikipedia.org/wiki/Android_application_package)

