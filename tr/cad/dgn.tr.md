{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "Dosya", "Format", "Aç", "Oku", "API", "MicroStation", "Intergraph Etkileşimli Grafik Tasarım Sistemi" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - MicroStation CAD Tasarım Dosyası Formatı",
  "description" :"DGN dosya formatı ve DGN dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## .dgn dosyası nedir?

.dgn (Tasarım) uzantılı bir dosya, MicroStation ve Intergraph Interactive Graphics Design System gibi CAD uygulamaları tarafından oluşturulan ve desteklenen bir çizim dosyasıdır. Otoyol, köprü, bina gibi inşaat projelerinde tasarım oluşturmak ve kaydetmek için kullanılır. Biçim, Autodesk'in [DWG](/tr/cad/dwg/) dosya biçimine benzer ve rakibi olarak kabul edilir. DNG dosyaları, Intergraph Standart Dosya Biçimi veya V8 DGN olarak kaydedilebilir. DGN, DWG, [BMP](/tr/image/bmp/), [JPEG](/tr/image/jpeg/), [PDF](/tr/pdf/), [GIF](/tr/image/) gibi birçok farklı formata dönüştürülebilir. gif/) ve diğerleri. Corel PaintShop Photo Pro ve IMSI TurboCAD Deluxe sürümleri gibi diğer yazılım uygulamalarının yanı sıra Autodesk AutoCAD, Bentley View ve Bentley Systems MicroStation ile açılabilir.

## V8 DGN Dosya Biçimi

Bir MicroStation V8 DGN dosyası, bir veya daha fazla modelden oluşur. Model, öğeler için bir kapsayıcıdır. V8 DGN, MicroStation'ın önceki sürümlerinde bulunan tüm dosya formatı tabanlı kısıtlamaları kaldırır. DGN dosya biçimindeki iyileştirmelerin bir listesi aşağıdadır.

* Bir DGN dosyasındaki seviye sayısındaki sınır kaldırıldı ve her seviye bir öğe olarak adlandırıldı ve saklandı.
* DGN dosyasının maksimum fiziksel boyutunun herhangi bir sınırlaması yoktur ve sadece işletim sistemi ile sınırlıdır (NT limiti 4 GB gibi)
* Tek bir öğenin maksimum boyutu 128 KB'dir.
* Bir hücrenin maksimum boyutunda herhangi bir sınır yoktur.
* Hücre adları yaklaşık 500 karakterle sınırlıdır.
* Bir DGN dosyasına eklenebilecek referans sayısında bir sınırlama yoktur.
* Bir çizgi dizisi, şekli veya nokta eğrisi en fazla 5000 köşeye sahip olabilir.
* Karmaşık bir zincir veya karmaşık şekildeki bileşenlerin sayısında bir sınır yoktur.
* Bir DGN dosyasındaki grafik gruplarının sayısında bir sınır yoktur.
* Çit yerleştirildiği görünüme paraleldir.
* Tek bir metin satırı 65.535 karakter içerebilir.
* Bir metin düğümünün maksimum boyutunda bir sınır yoktur.
* Bir DGN dosyasındaki metin düğümlerinin sayısında bir sınır yoktur.
* Her öğe, öğenin yaşam döngüsü boyunca değişmeyen benzersiz bir 64 bit tanımlayıcıya sahiptir.
* Her öğe, en son değişikliğin zamanını gösteren bir zaman damgasına sahiptir.

## Referanslar

* [DNG - Wikipedia Tarafından](https://en.wikipedia.org/wiki/DGN)
* [MicroStation V8 DGN Dosya Biçimi](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

