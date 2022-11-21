{
  "date" : "2019-10-11",
  "keywords" :[ "apk dosyası", "apk dosya biçimi", "apk dosyası nedir", "dosya", "apk örneği", "apk dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - APK dosyası nedir?",
  "description":"APK dosyasının ne olduğunu ve APK dosyalarını oluşturabilen ve açabilen API'leri öğrenin.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## APK dosyası nedir?

.apk uzantılı bir dosya, Android cihazlara uygulamaları (uygulamaları) yüklemek için kullanılan bir Google Android uygulama dosyasıdır. Resmi IDE Google Android Studio kullanılarak yürütülebilir bir dosya olarak oluşturulur ve son kullanıcılar tarafından indirilip kurulmak üzere Google Play mağazasına yüklenir. APK dosyaları, Google Play Store'da yayınlanmadan önce oluşturulabilir ve manuel kurulum için kullanılabilir hale getirilebilir. Bu, oluşturulan APK paket dosyasının işlevselliğini ve davranışını test etmeye yardımcı olur. Bu nedenle, APK dosyasının güvenilir bir kaynaktan geldiğinden ve herhangi bir kötü amaçlı yazılım içermediğinden emin olunmalıdır.

## APK Dosya Biçimi

APK dosyaları, herhangi bir ZIP dosya açma yazılımı ile açılabilen [ZIP](/tr/compression/zip/) dosya biçiminde sıkıştırılmış olarak paketlenir. Böyle bir dosyanın .apk uzantısı .zip olarak yeniden adlandırılabilir ve dosyayı herhangi bir ZIP uygulamasında açabilir veya içeriğini çıkartabilirsiniz.

## APK Paket İçeriği

Tek bir APK dosyası, kurulumu ve yürütülmesi için gerekli olan tüm gerekli dosyaları içerir. Bir APK dosyası, bir ZIP uygulamasıyla çıkarıldığında aşağıdaki dosya ve klasörleri içerir.

* `META-INF/`: Bildiri dosyasını, imzayı ve arşivdeki kaynakların listesini içeren dizin
* `lib/`: armeabi-v7a, x86, arm64-v8a, vb. gibi belirli platformlarla ilgili derlenmiş kodu içeren dizin.
* `res/`: Görüntüler gibi derlenmemiş kaynakları içeren dizin
* `assets/`: AssetManager tarafından alınabilen uygulama varlıklarını içeren dizin.
* `androidManifest.xml`: APK dosyasının adını, sürüm bilgilerini ve içeriğini içerir
* `classes.dex`: Bunlar, Dalvik sanal makinesinde ve Android Runtime tarafından çalıştırılabilen derlenmiş Java sınıflarıdır.
* `resources.arsc`: Dizeler gibi derlenmiş kaynaklar dosyası

## APK dosyası Android Cihaza nasıl kurulur?

Android cihazlarınıza APK dosyası yüklemek için aşağıdaki adımlar kullanılabilir.

1. Web tarayıcısını kullanarak APK'yı indirin
2. Ona dokunun - daha sonra cihazınızın üst çubuğunda indirildiğini görebilmeniz gerekir.
3. İndirildikten sonra İndirilenler'i açın, APK dosyasına dokunun ve istendiğinde Evet'e dokunun.

Bu adımların ardından, uygulamanın cihazınıza yüklenmesi başlayacaktır.

## Referanslar

* [APK Dosya Biçimi](https://en.wikipedia.org/wiki/Android_application_package)

