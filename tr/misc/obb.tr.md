{
  "date" : "2022-02-16",
  "keywords" :[ "obb dosyası", "obb dosya biçimi", "obb dosyası nedir", "dosya", "obb örneği", "obb dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBB Dosya Biçimi - Android Opak İkili Blob Dosyası",
  "description":"OBB dosya formatı ve OBB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## OBB dosyası nedir?

OBB dosyası, Android [APK](/tr/compression/apk/) dosyasına ek olarak ek veriler içeren bir genişletme dosyasıdır. Google Play mağazası, boyutu 100 MB'tan büyük bir Android APK dosyasına izin vermez. Ancak bazı uygulamalar, APK dosyalarına ek olarak yüksek tanımlı grafikler, medya dosyaları veya diğer büyük varlıkların barındırılmasını gerektirebilir. OBB dosya türlerinin devreye girdiği yer burasıdır. Google Play, bu genişletme dosyalarının APK dosyasına ek olarak eklenmesine izin verir.

## OBB Dosya Biçimi

OBB dosyaları, APK dosyalarıyla birlikte ikili dosyalar olarak kaydedilir. OBB dosyalarına bir APK eşlik ettiğinde, Google Play genişletme dosyalarını kendi sunucusunda barındırır ve geliştiriciden herhangi bir ek ücret alınmaz. Bu ek dosyalar, uygulama kurulum için indirildiğinde cihazın paylaşılan depolama alanında SD kartta veya USB'ye monte edilebilir bölümde depolanır.

OBB dosyaları indirilir ve indirildikten sonra kurulur. Ancak bazı durumlarda, uygulama ilk kez çalıştırıldığında bunlar kurulum için indirilir.

### OBB Maksimum Dosya Boyutu

Google Play Store, boyutu 2 GB'a kadar olan OBB genişletme dosyalarını yüklemenizi sağlar. İnternet üzerinden verimli yükleme için büyük boyutlu dosyaların sıkıştırılmış [ZIP](/tr/compression/zip/) dosyaları olarak yüklenmesi önerilir.

Bu genişletme dosyaları, uygulamanın gerektirdiği ek kaynaklar için **ana** birincil genişletme dosyası olarak veya ana genişletme dosyasındaki küçük güncellemeler için tasarlanmış isteğe bağlı bir yama genişletme dosyası olarak barındırılabilir.

## Referanslar

* [Android Geliştiricileri - Genişletme Dosyaları](https://developer.android.com/google/play/expansion-files)

