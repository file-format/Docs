{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "dosya", "uzantı", "dosya formatı", "CSharp", "Programlama Dili"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - CSharp Kod Dosyası",
  "description":"CS dosya formatı ve CS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## CS dosyası nedir?

.cs uzantılı dosyalar C# programlama dili için kaynak kod dosyalarıdır. Microsoft tarafından .NET Framework ile kullanılmak üzere sunulan dosya formatı, EXE veya DLL biçiminde nihai çıktı dosyasını oluşturmak için derlenen kod yazmak için düşük seviyeli programlama dili sağlar. Bunlar Microsoft Visual Studio ile oluşturulabilir ve derlenebilir. Microsoft Visual Studio Express, ücretsiz bir IDE olan bu tür dosyaları oluşturmak ve güncellemek için de kullanılabilir. CS dosyaları, basit masaüstü uygulamalarından daha karmaşık programlara kadar değişebilen uygulama geliştirme için kullanılır. C# diliyle oluşturulan basit bir Visual Studio projesi [çözüm](/tr/programming/sln/), bu tür bir veya daha fazla dosyadan oluşabilir. Derlemeye dahil edilmek üzere işaretlenen dosyalar, projenin parçası olan ve derleyiciye işaretli dosyaları kullanmasını söyleyen [CSPROJ](/tr/programming/csproj/) dosyasında listelenir.

## CS Dosya Biçimi ##

CS dosyaları, düzenleme için herhangi bir metin düzenleyicide açılabilen metin tabanlı dosya biçimleridir. Bununla birlikte, uygun sözdizimi vurgulama ile desteklenen bir IDE'de açıldığında, kodun okunması ve düzenlenmesi kolaydır. Basit bir CS dosyası şunları içerir:

* Ad alanları bildirimi - Belirli bir ad alanı tarafından tanımlanan belirli bir işlevselliğe atıfta bulunmak için
* Değişken bildirimi - Belirli bir uygulama için sınıf düzeyinde değişkenleri bildirmek için
* Yöntem Bildirimi - Belirli işlevsellik için yöntem bildirimi bildirmek için

### Sözdizimi ###

* Noktalı virgül, bir ifadenin sonunu belirtmek için kullanılır.
* İfadeleri gruplandırmak için süslü parantezler kullanılır. İfadeler genellikle yöntemler (işlevler), yöntemler sınıflar ve sınıflar ad alanları olarak gruplandırılır.
* Değişkenler eşittir işareti kullanılarak atanır, ancak ardışık iki eşittir işareti kullanılarak karşılaştırılır.
* Köşeli parantezler dizilerle birlikte, hem dizileri bildirmek hem de bunlardan birinde belirli bir dizinde bir değer almak için kullanılır.

### Örnek ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

