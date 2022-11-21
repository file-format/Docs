{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "dosya", "uzantı", "dosya formatı", "ICI uygulaması", "Programlama Kılavuzu", "ici örneği", "ICI programlama dili", "ICI modülleri", "ICI veri modeli ", "ICI belgeleri", "ICI dili" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - Programlama Dili Dosyası",
  "description":"ICI dosya formatı ve ICI dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## ICI dosyası nedir?

Esnek veri türlerinin yanı sıra dinamik yazım gibi çeşitli özellikleri içeren ve yorumlanan genel amaçlı bir programlama dili, ICI (kısaltma değil) programlama dili olarak bilinir. [Perl](/tr/programming/pl/) diline benzer olduğu düşünülmektedir. Bu ICI dili, akış kontrol yapılarını içerir ve ayrıca C dilinin bazı operatörlerini içerir. Nesne yönelimli bir dil değildir, ancak OOP'nin bazı özellikleri, üst yapılar olarak bilinen belirli bir kalıtım yöntemiyle elde edilebilir. [C](/tr/programming/c) ile benzer şekilde, bu ICI programlama dili aynı sistem arabirimine ve yerleşik işlevler için standart bir kitaplığa sahiptir.


## Kısa Tarih ##

1980'lerin sonunda, Tim Long tarafından genel amaçlı yorumlanmış bir programlama dili olarak geliştirildi. Bu dilin özelliklerinin çoğu C'ye benzer ve bazı özellikleri bazı özel yöntemler uygulayarak da elde edebilir. Bu dilin mülkiyeti kamuya aittir ve yeniden satılabilir bir dil olarak mevcuttur ve hiç kimse kaynak kodunu nereden aldığını belirtmek zorunda değildir. ICI belgelerinin telif hakkı Canon Information System Research Australia'nın altındadır.

## Teknik Şartname ##

Bu dilde kullanılan iki farklı veri türü vardır. Bu ikisi İlkel ve Toplu veri türleridir. Bunların her ikisi de dilde önceden tanımlanmış yapılarına göre farklı ifadeler içerir. Yuvalanmış ve alt programlar gibi farklı modüller bu dil tarafından desteklenir. Bazı özellikleri Perl'e benzediğinden, düzenli ifadelerle katı bir entegrasyona sahiptir.

Kümeler heterojen ve iç içe olacak şekilde sınırlandırılmıştır. Bu kümeler, Birleştirme ve Kesişme vb. gibi yaygın olarak kullanılan küme işlemleri için destek sağlar. Çoğunlukla çok uluslu kuruluşların sahip olduğu uygulamalar için çekirdek uygulama adına bir dil olarak kullanılır.

Bu dilde neredeyse tüm program türleri yazılabilir ve çoğunlukla karmaşık veri yapılarını içeren belirli programlar ICI programlama dilinde yazılır. Uygulamalar, ICI uygulamasını, içinde yazılması gereken bir şekilde içerebilir. Uygulamanın işlevsel bölümleri, ICI modülleri tarafından uygulanabilir. ICI'nin dili biraz C diline benzer, ancak ICI'nin veri modeli sözlükler (yapı), kümeler, dinamik diziler, düzenli ifadeler ve (gerçek) dizeler gibi türlerle oldukça yüksek düzeyde ve farklıdır.


## ICI Dosya Biçimi Örneği ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Referans ##

* [ICI Programlama Dili](http://atrn.org/ici/doc/ici.html)



