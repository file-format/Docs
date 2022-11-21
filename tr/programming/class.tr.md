{
  "date" : "2019-10-11",
  "keywords" :[ "class", ".class","class dosyası nedir","class dosyası nasıl açılır", "uzantı", "dosya", "class file","class file format", ".class extension ", "java'da sınıf dosyası"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Sınıf - Java Sınıfı Dosya Biçimi",
  "description":"Class dosya formatı ve Class dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Sınıf dosyası nedir?

**Java'daki bir Sınıf dosyası**, aslında bir Java Sanal Makinesi (JVM) tarafından yürütülen [.java](/tr/programming/java/) sınıfının derlenmiş çıktısıdır. Sınıf dosyaları ayrı ayrı çalıştırılabileceği gibi, diğer paket dosyalarıyla birlikte bir [JAR](/tr/programming/jar/) dosyasının bir parçası olabilir. Bunlar, komut satırı arabiriminden **`javac`** komutu kullanılarak oluşturulabilir. [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/Eclipse-ide-java-developers) ve NetBeans gibi bazı Java IDE'leri, projenin Java'sından .class çıktı dosyaları oluşturmayı sağlar Dosyalar.

## Sınıf Dosya Biçimi

Bir Java sınıf dosyası, JVM tarafından çalıştırılacak ara kod olan bayt kodundan oluşur. Bir sınıf dosyası, 8 bitlik bir bayt akışından oluşur ve çok baytlı veri öğeleri her zaman büyük-endian düzeninde depolanır.

### ClassFile Yapısı

Sınıf dosya yapısı aşağıda gösterildiği gibidir.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
nerede:

* u1 = işaretsiz bir baytlık miktar
* u2 = işaretsiz iki baytlık miktar
* u4 = işaretsiz dört baytlık miktar

.class dosya yapısının ayrıntıları, Oracle [sınıf dosya biçimi](https://docs.Oracle.com/javase/specs/jvms/se7/html/jvms-4.html)'de açıklandığı gibi ve tarafından başvurulabilir. referans için geliştiriciler. Bu alanların özeti aşağıdaki gibidir.

* `sihir' - Sihirli öğe, sınıf dosyası biçimini tanımlayan sihirli sayıyı sağlar; 0xCAFEBABE değerine sahiptir.
* `minor_version`, `major_version` - minor_version ve major_version öğelerinin değerleri, bu sınıf dosyasının alt ve ana sürüm numaralarıdır.
* `constant_pool_count` - Constant_pool_count öğesinin değeri, Constant_pool tablosundaki giriş sayısı artı bire eşittir. Bir sabit_havuz dizini, uzun ve çift türündeki sabitler dışında, sıfırdan büyük ve sabit_havuz_sayımından küçükse geçerli kabul edilir.
* `constant_pool[]` - Constant_pool, çeşitli dizi sabitlerini, sınıf ve arabirim adlarını, alan adlarını ve ClassFile yapısı ve alt yapılarında atıfta bulunulan diğer sabitleri temsil eden bir yapı tablosudur (§4.4). Her bir sabit_havuz tablosu girişinin formatı, ilk "etiket" baytı ile belirtilir.
* `access_flags` - access_flags öğesinin değeri, bu sınıf veya arayüzün erişim izinlerini ve özelliklerini belirtmek için kullanılan bir bayrak maskesidir.
* `this_class` - this_class öğesinin değeri, Constant_pool tablosunda geçerli bir dizin olmalıdır.
* `süper_sınıf` - Bir sınıf için, süper_sınıf öğesinin değeri sıfır olmalı veya sabit_havuz tablosunda geçerli bir dizin olmalıdır.
* `interfaces_count` - interfaces_count öğesinin değeri, bu sınıf veya arabirim türündeki doğrudan süper arabirimlerin sayısını verir.
* `interfaces[]` - interfaces dizisindeki her değer, Constant_pool tablosunda geçerli bir dizin olmalıdır.
* `fields_count` - fields_count öğesinin değeri, field tablosundaki field_info yapılarının sayısını verir.
* `fields[]` - Fields tablosundaki her değer, bu sınıf veya arabirimdeki bir alanın tam açıklamasını veren bir field_info yapısı olmalıdır.
* `methods_count` - method_count öğesinin değeri, method tablosundaki method_info yapılarının sayısını verir.
* `methods[]` - Method tablosundaki her değer, bu sınıf veya arabirimdeki bir yöntemin tam açıklamasını veren bir method_info yapısı olmalıdır. Bir method_info yapısının erişim_flags öğesinde ACC_NATIVE ve ACC_ABSTRACT işaretlerinden hiçbiri ayarlanmamışsa, yöntemi uygulayan Java Sanal Makinesi yönergeleri de sağlanır.
* `attributes_count` - nitelikler_sayım öğesinin değeri, bu sınıfın nitelikler tablosundaki özniteliklerin sayısını (§4.7) verir.
* `attributes[]` - Nitelikler tablosunun her değeri bir feature_info yapısı olmalıdır.




## Referanslar

* [Sınıf Dosya Biçimi](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

