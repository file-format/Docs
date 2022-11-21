{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c","ac dosyası nedir","c dosyası nasıl açılır", "uzantı", "dosya", "c dosyası","c dosya biçimi", "c dosya uzantısı"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"C - C Dili Programlama Dosyası",
  "description":"C dosya formatı ve C dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## .c dosyası nedir?

c dosya uzantısıyla kaydedilen bir dosya, C programlama dilinde yazılmış bir kaynak kod dosyasıdır. **C dosyası**, uygulamanın işlevselliğinin tüm uygulamalarını kaynak kodu biçiminde içerir. Kaynak kodun bildirimi [.h](/tr/programming/h/) uzantılı kaydedilen başlık dosyalarına yazılır. C++, C dilinin modern biçimidir ve günümüzde yazılımların çoğunu geliştirmek için kullanılmaktadır.

## Kısa Tarihçe

C dili, UNIX işletim sistemi için farklı yardımcı programlar oluşturmanın bir sonucu olarak ortaya çıkmıştır. Bu programlama dilinin yaratılmasının arkasındaki adam olan Denis Ritchie, çalışma ilk olarak 1960'larda ve 1970'lerin başında başladı.

## C Dosya Biçimi

C dosyaları, programlama dili sözdizimine göre düz metin dosyası biçiminde yazılır. Tipik bir C dosyasında şunlar bulunur:

* herhangi bir başlık Dosyasını içe aktarmak için dosyanın üst kısmındaki import ifadesi
* istenen işlevselliği uygulamak için bir veya daha fazla yöntem

### Başlıkları İçe Aktarma

.h uzantılı başlık dosyaları, projedeki diğer işlevsellik dosyalarını dahil etmek için gerekli içerme ifadelerini içerir. Ayrıca bunlar, uygulama dosyasında tanımlanan yöntemlerin bildirimlerini içerir. Başlık dosyaları, aşağıda gösterildiği gibi include deyimi kullanılarak dahil edilir.

```
#include <filename.h>
```

### Kaynak Kodu Uygulaması

İşlevsel gereksinimlerin gerçek uygulaması, C dosyasında yöntemler olarak kodlanmıştır. Bir C dosyasındaki her yöntemin bir dönüş türü, yöntem adı vardır ve bazı giriş parametreleri olabilir. Dönüş türü geçersiz değilse, yöntem bir miktar değer döndürüyor olabilir.

### C Kodu Örneği
İşte ac örnek program:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Referanslar** ##

* [Sınıf Uygulaması - Wikipedia Tarafından](https://en.wikipedia.org/wiki/Class_implementation_file)

