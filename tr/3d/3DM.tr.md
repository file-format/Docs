{
  "date" : "2021-08-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3DM",
  "description":"3DM dosya formatı ve 3DM dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "3DM",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-08-13"
}

## 3DM dosyası nedir?

.3dm uzantılı bir dosya, 3B grafik yazılımı için kullanılan açık kaynaklı bir dosya biçimidir. Yüzey, noktalar ve eğri bilgileri gibi bağımlı öğeleriyle birlikte 3B modelleri içerir. 3DM dosya formatı, 3 boyutlu geometrinin uygulamalar arasında doğru şekilde aktarılması için [openNURBS](https://github.com/mcneel/opennurbs) girişimi tarafından geliştirilmiştir. 3DM dosyaları, Rhinoceros, SAP VEViewer, Moment of Inspiration ve Right Hemisphere Deep View gibi uygulamalarla açılıp dönüştürülebilir.

## 3DM Dosya Biçimi

Açık kaynaklı bir araç seti olan [openNURBS](https://github.com/mcneel/opennurbs), dosya formatını okumak ve yazmak için 3DM dosya formatı belirtimlerini, belgeleri, C++ kaynak kodu kitaplıklarını ve .NET 2.0 derlemelerini içerir.

### 3DM Örnek Dosyaları

Bazı örnek 3DM dosyaları openNURBS [examples](https://github.com/mcneel/opennurbs/tree/7.x/example_files) bölümünden indirilebilir. Bunlar, openNURBS araç takımı kullanılarak yüklenebilir ve görüntülenebilir.

## 3DM dosyaları nasıl okunur veya yazılır?

[openNURBS](https://github.com/mcneel/opennurbs) kitaplıkları, herkesin Rhino'ya ihtiyaç duymadan 3DM dosya biçimini okumasına ve yazmasına olanak tanır. OpenNURBS dosya biçimini kullanarak 3B modelleri okuyup yazacak bir kitaplık için C++ kaynak kodu sağlar. Bu araç seti ayrıca NURBS değerlendirme araçları ve temel geometrik ve 3B görünüm işleme araçlarının yanı sıra birkaç örnek program için kaynak kodu da sağlar. [Rhinoceros](https://discourse.mcneel.com/c/opennurbs/6) destek forumları, 3DM topluluğunun karşılaştığı sorunları paylaşmak ve çözüm bulmak için zengin bir içerik ve tartışma yeridir.

## Referanslar ##

* [Gergedan](https://www.rhino3d.com/download/openNURBS)
* [Gergedan - Vikipedi](https://en.wikipedia.org/wiki/Rhinoceros_3D)
* [GitHub'da openNURBS](https://github.com/mcneel/opennurbs)

