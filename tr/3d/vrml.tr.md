{
  "date" : "2019-10-11",
  "keywords" :[ "vrml dosyası", "vrml dosya formatı", "vrml dosyası nedir", "dosya", "vrml örneği", "vrml dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VRML Dosya Biçimi",
  "description":"VRML dosya formatı ve VRML dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VRML",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## VRML dosyası nedir?
Sanal Gerçeklik Modelleme Dili (VRML), World Wide Web (www) üzerinde etkileşimli [3D](/tr/3d/) dünya nesnelerinin temsili için bir dosya formatıdır. Kullanımını, illüstrasyonlar, tanım ve sanal gerçeklik sunumları gibi karmaşık sahnelerin üç boyutlu temsillerini oluştururken bulur. Biçimin yerini [X3D](/tr/3d/x3d/) almıştır. Birçok 3D modelleme uygulaması, nesneleri ve sahneleri VRML formatında kaydedebilir.

## VRML Dosya Biçimi

VRML, bir 3B çokgenin köşeleri ve kenarları gibi bilgilerin yanı sıra yüzey rengi, UV eşlenmiş dokular, parlaklık, saydamlık vb. bilgileri belirten bir metin dosyası biçimidir. Ses, film ve görüntüler gibi diğer ortamlara köprülere sahip olmanın yanı sıra statik ve hareketli nesneleri temsil etme yeteneğine sahiptir. Bu, kullanıcı bu nesneleri tıkladığında hiper bağlantılı öğelerin açılmasına izin verir.

Yaygın terminolojide TVRML dosyaları "dünyalar" olarak adlandırılır ve .wrl uzantısına sahiptir. Bu dosyaların metinsel doğası, gzip gibi sıkıştırma formatlarını kullanarak dosya boyutunu küçültmeyi mümkün kılar ve bu da onları internet üzerinden hızlı bir şekilde aktarım için daha uygun hale getirir. [VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html) için dosya biçimi belirtimleri, bu dosyaları okumak/yazmak için uyumlu uygulamalar oluşturmak için geliştiricinin referansı olarak işlev görür.

## Tasarım Kriteri ##

VRML'nin amacı ve tasarımı aşağıdaki gereksinimler etrafında döner.

* **Yetkilendirilebilirlik** - Uygulama oluşturucular ve düzenleyiciler geliştirmeyi ve diğer endüstriyel formatlardan veri içe aktarmayı mümkün kılar
* **Tamlık** - Uygulama için gerekli tüm bilgileri sağlar ve geniş endüstri kabulü için eksiksiz bir özellik setini ele alır
* **Birleştirilebilirlik** - VRML öğelerini bir arada kullanma ve böylece yeniden kullanılabilirliğe izin verme yeteneği.
* **Genişletilebilirlik** - Yeni öğeler ekleyebilme.
* **Uygulanabilirlik** -Geniş bir sistem yelpazesinde uygulanabilme özelliği.
* **Çoklu kullanıcı potansiyeli** - Çok kullanıcılı ortamların uygulanmasını engellememelidir.
* **Ortogonallik** - VRML'nin öğeleri birbirinden bağımsız olmalı veya bağımlılıklar yapılandırılmalı ve iyi tanımlanmalıdır.
* **Performans** - Öğeler, çeşitli bilgi işlem platformlarında etkileşimli performansa önem verilerek tasarlanmalıdır.
* **Ölçeklenebilirlik** - VRML'nin öğeleri, sonsuz büyüklükteki kompozisyonlar için tasarlanmalıdır.
* **Standart uygulama** - Yalnızca mevcut uygulamayı yansıtan, mevcut uygulamayı desteklemek için gerekli olan veya önerilen standartları desteklemek için gerekli olan unsurlar standartlaştırılmalıdır.
* **İyi yapılandırılmış** - Bir öğe, iyi tanımlanmış bir arayüze ve basit bir şekilde ifade edilmiş koşulsuz bir amaca sahip olmalıdır. Çok amaçlı elemanlardan ve yan etkilerden kaçınılmalıdır.

## Referanslar ##

* [VRML - Wikipedia'dan](https://en.wikipedia.org/wiki/VRML)
* [VRML v 2.0 Dosya Biçimi Özellikleri](http://gun.teipir.gr/VRML-amgem/spec/index.html)

