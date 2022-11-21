{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "dosya", "uzantı", "dosya formatı", "Visual Basic", "Programlama Kılavuzu"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Visual Basic Kod Dosyası",
  "description":"VB dosya biçimi ve VB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## .vb dosyası nedir?

VB dosyası, Microsoft tarafından .NET uygulamalarının geliştirilmesi için oluşturulmuş, Visual Basic dilinde oluşturulmuş bir kaynak kod dosyasıdır. Farklı sözdizimine sahip bir başka benzer dil, dosyaları [.CS](/tr/programming/cs/) dosya uzantısıyla kaydedilen C#'dır. Dosya formatı, EXE veya DLL biçiminde nihai çıktı dosyasını oluşturmak için derlenen kod yazmak için düşük seviyeli programlama dili sağlar. Bunlar Microsoft Visual Studio ile oluşturulabilir ve derlenebilir. Microsoft Visual Studio Express, ücretsiz bir IDE olan bu tür dosyaları oluşturmak ve güncellemek için de kullanılabilir. VB diliyle oluşturulan basit bir Visual Studio projesi [çözüm](/tr/programming/sln/), bu tür bir veya daha fazla dosyadan oluşabilir. Derlemeye dahil edilmek üzere işaretlenen dosyalar, projenin parçası olan ve derleyiciye işaretli dosyaları kullanmasını söyleyen [CSPROJ](/tr/programming/csproj/) dosyasında listelenir.

## VB Dosya Biçimi - Daha Fazla Bilgi

VB dosyaları, düzenleme için herhangi bir metin düzenleyicide açılabilen metin tabanlı dosya biçimleridir. Bununla birlikte, uygun sözdizimi vurgulama ile desteklenen bir IDE'de açıldığında, kodun okunması ve düzenlenmesi kolaydır. Basit bir VB dosyası şunları içerir:

* Ad alanları bildirimi - Belirli bir ad alanı tarafından tanımlanan belirli bir işlevselliğe atıfta bulunmak için
* Değişken bildirimi - Belirli bir uygulama için sınıf düzeyinde değişkenleri bildirmek için
* Yöntem Bildirimi - Belirli işlevsellik için yöntem bildirimi bildirmek için

## VB Dosya Biçimi Örneği

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



