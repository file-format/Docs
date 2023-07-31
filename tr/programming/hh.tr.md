{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh",".hh dosyası nedir",".hh dosyası nasıl açılır", "uzantı", "dosya", ".hh dosyası",".hh dosya formatı", " .hh dosya uzantısı",".HH Dosya Örneği"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - C++ Başlık Dosyası Biçimi",
  "description":"HH dosya formatı ve HH dosyası oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## .hh dosyası nedir?

.hh uzantılı bir dosya, değişkenlerin, sabitlerin ve işlevlerin bildirimini içeren bir C++ başlık dosyasıdır. Bu bildirimler, genellikle kullanıcı mantığının gerçek uygulamasını içeren [.cpp](/tr/programming/cpp/) dosyaları olarak kaydedilen ilgili C++ uygulama dosyaları tarafından kullanılır. .hh başlık dosyalarına, uygulama CPP dosyalarında '#include' yönergesi kullanılarak başvurulur. Proje düzeyi bildirimlerini dahil etmek için C++ projenize mümkün olduğu kadar çok başlık dosyası ekleyebilirsiniz.

## .HH Dosya Biçimi

Bir .hh dosyası, başlık dosyası tanımlama kuralları göz önünde bulundurularak oluşturulan bir düz metin dosyasıdır. Bir .hh dosyasında bildirilen en yaygın bilgiler aşağıdakileri içerir.

**`Değişkenler`** - Nesne Yönelimli Programlama (OOP) durumunda, bir sınıf başlık dosyası, uygulama kaynak kodu dosyalarından erişilebilen tüm sınıf düzeyindeki değişkenlerin tanımlarını içerir
**`Metot Bildirimi`** - Tüm yöntem bildirimleri, birden çok uygulama dosyasında erişilebilmesi için .h başlık dosyalarına dahil edilmiştir.
**`Satır İçi Olmayan İşlev Tanımları`** - Başlık dosyaları, satır içi olmayan yöntemlerin tanımlarını da içerebilir.
**`Message Maps`** - Bir başlık dosyası, bir MFC kaynak kodu uygulaması durumunda mesaj haritaları da içerebilir. Bu durumda, mesaj haritaları, düğme, onay kutusu, radyo düğmeleri vb. gibi UI öğelerine bağlı olan işlevsellik uygulamasına bağlıdır.

## .H ve .HH Dosyaları Arasındaki Fark

Görünüşe göre, .h ve .hh başlık dosyaları arasında, [C](/tr/programming/c/) veya C++ gibi ilgili diller için önerilen kullanım şekli dışında böyle bir fark yoktur. Başlık dosyalarınızı bu dillere göre adlandırmak, C ve C++ uygulamalarının bir karışımı olabilen büyük bir projede bunları ayırt etmenize yardımcı olur.

Ek olarak, başlıklar uzantıya göre ayrılmışsa, editörünüz sırasıyla uygun biçimlendirmeyi otomatik olarak uygulayabilir.

Genel olarak, bu iki dosya biçiminin farklılaştırılması herhangi bir zarar vermeyecek, ancak avantajlı olacaktır ve C ve C++ ayrımı için takip edilmesi teşvik edilir.

### Başlık Muhafızları

Başlık dosyaları, diğer başlık dosyalarının eklenmesinin bir sonucu olarak aynı dosyaya birden çok bildirimin dahil edildiği karmaşık hatalara neden olabilir. Bu yinelenen tanımlar, derleyici hatalarına neden olur. Bu problemli durum, aşağıda gösterildiği gibi koşullu derleme direktifleri olan başlık koruması adı verilen bir mekanizma ile önlenebilir.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Bu üst bilgi ile ön işlemci, "ANY_UNIQUE_NAME_HERE_HPP" öğesinin zaten tanımlanıp tanımlanmadığını kontrol eder. Başlık aynı dosyaya tekrar tekrar dahil edilirse, başlığın içeriği göz ardı edilir.

## Referanslar

* [Başlık Dosyalayıcıları - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [.h ve .hh dosya biçimleri arasındaki fark](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

