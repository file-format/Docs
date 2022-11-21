{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc","arsc dosyası nedir","arsc dosyası nasıl açılır", "uzantı", "dosya", "arsc dosyası","arsc dosya biçimi", "arsc dosya uzantısı" ,"arsc Dosya Örneği"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - Android Paketi Kaynak Tablosu Dosyası",
  "description":"ARSC dosya formatı ve ARSC dosyasını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## ARSC dosyası nedir?

ARSC dosyası, uygulamanın kaynak listesini tablo biçiminde içeren bir Android Kaynak tablo dosyasıdır. Bu, Kaynak adları, özellikler ve kimlikler gibi bilgileri içerir. ARSC dosyaları, bu Android uygulamalarını yüklemek için kullanılan APK paketlerinin bir parçasıdır. Bir android uygulamasındaki resimler, düzenler, stiller ve dizeler gibi tüm kaynaklar, APK dosyası oluşturulduğunda ikili dosyalara dönüştürülür. ARSC dosyası da, programın derlenmiş tüm kaynaklarının ve kimliklerinin listesini içeren aynı şekilde oluşturulur.

## ARSC Dosya Biçimi

.arsc uzantılı dosyalar, ANT (Eclipse) veya Gradle (AS) gibi bir derleyicinin [APK](/tr/compression/apk/) dosyasını oluşturmak için Android uygulama kodunu derlemesinden sonra oluşturulan ikili dosyalardır. APK dosyasını, derlenmiş java sınıfı dosyaları olan (classs.dex) içeriğini görüntülemek için WinZip gibi herhangi bir arşivleme yardımcı programını kullanarak ayıklayabilirsiniz. Bunlara ek olarak, aşağıdakiler hakkında meta-bilgi içeren bu ARSC dosyasını da içerir:

* XML düğümleri
* Nitelikler
* Kaynak Kimlikleri

Öznitelikler çalışma zamanında bir değere çözümlenirken, bir APK dosyasındaki kaynaklara Kaynak Kimlikleri tarafından başvurulur. Android aapt aracı, oluşturma zamanında dosyalarda tanımlanan tüm kaynakları toplar ve bunlara kaynak kimlikleri atar. Derlenmiş kaynaklara tanımlayıcılar atandıktan sonra, kaynak kodun yanı sıra resources.arsc'den bir R.java dosyası oluşturulur.

## Referanslar

* [İkili Kaynak Tablosu Yapısı](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

