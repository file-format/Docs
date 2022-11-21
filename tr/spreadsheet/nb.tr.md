{
  "date" : "2019-12-16",
  "keywords" :[ "NB", "dosya", "uzantı", "dosya formatı", "Mathematica", "Elektronik Tablo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"NB dosyalarını oluşturabilen ve açabilen NB dosyası API'lerinin ne olduğu hakkında bilgi edinin.",
  "title" :"NB - Mathematica Defter Dosya Biçimi",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## .NB dosyası nedir?

.nb uzantılı bir dosya, matematiksel yönergeler için yönergeleri bir metin dosyasına kaydeden bir Wolfram not defteri dosya biçimidir. Canlı hesaplama, isteğe bağlı dinamik arabirimler, tam dizgi girişi, görüntü girişi, otomatik kod açıklaması, tam bir üst düzey programatik arabirim ve özenle düzenlenmiş binlerce işlev ve seçenek gibi birçok farklı türde veri içerebilir. Metinsel talimatlar, girdi ifadeleri dosyaya konulduğu için oluşturulan ve güncellenen Mathematica girdi ve çıktılarıdır.

## Wolfram Notebook NB Dosya Biçimi - Daha Fazla Bilgi

Wolfram Notebook NB dosyaları, insan tarafından okunabilen bir dosya biçimi olan düz metin biçiminde kaydedilir. Not defterinin içeriği, elektronik tabloya benzer şekilde, her birinin hücre gruplarıyla temsil edildiği düz metin olarak bölümler halinde düzenlenir. Bu grupların aralığı, her hücrenin sonuna doğru bir parantez ile tanımlanır. Bir hücreye atanan stil, not defteri içindeki rolünü aşağıda ayrıntılı olarak belirler.

### Wolfram Dili Olarak Defterler

Wolfram Language Kernal tarafından yürütülecek matematiksel talimatlardan oluşan Not Defterini kaydetmek istendiğinde, belgedeki hücrelere otomatik olarak "Giriş" metin stili atanır. Bu, çekirdeğe bunları, kullanıcı 'Shift+Return' tuşlarının bir kombinasyonunu verdiğinde yürütülen talimatlar olarak kabul etmesini söyler. Bir Mathematica Defter aşağıdaki örnekte gösterildiği gibidir.

{{< figure src="../Wolfram Notebook.jpeg" alt="Wolfram Defter Dosya Biçimi" >}}

### Belge Olarak Defterler

Mathematica Not Defterleri, ne gördüğünüze ne elde ettiğinize dair bir görünüm vermek için belge biçiminde olabilir (WYSIWYG). Bu belgeler, ekranda veya basılı bir kağıtta görüntülenenlerle aynıdır ve etkileşimlidir. Bunun için, Çekirdek tarafından ifadeleri yürütmeden içeriği görüntülemek için hücreye 'Metin Stili' atanır.

## Mathematica Defterlerini Dışa Aktar

Mathematica Not Defterleri, PDF, grafik, GIS, Sıkıştırılmış ve Elektronik Tablolar gibi birçok farklı dosya biçimine aktarılabilir.

## Referanslar

* [Mathematica Notebook Basics](https://reference.wolfram.com/language/guide/NotebookBasics.html)

