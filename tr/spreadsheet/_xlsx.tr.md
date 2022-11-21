{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Bir _XLSX dosyasının ne olduğunu ve _XLSX dosyalarını oluşturabilen ve açabilen API'leri öğrenmek için dosya biçimi kılavuzunuz.",
  "title" :"_XLSX dosyası nedir?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## _XLSX dosyası nedir?

.\_xlsx uzantılı bir dosya aslında başka bir uygulama tarafından yeniden adlandırılan bir [XLSX](/tr/spreadsheet/xlsx/) dosyasıdır. Bu, dosya adı bir . dosya adının sonunda. \_XLSX dosyaları Microsoft Excel'de XLSX dosyalarına benzer şekilde tekrar .xlsx uzantılı olarak yeniden adlandırılarak açılabilir.

## _XLSX Dosya Biçimi - Daha fazla bilgi

_XLSX dosyaları, XLSX dosyalarından farklı değildir ve Microsoft tarafından 2000 yılında kabul edilen Açık XML standardını kullanır. XLSX'ten önce, [XLS](/tr/spreadsheet/xls/), belgeleri kaydetmek için Excel elektronik tablolarıyla çalışmak için kullanılan birincil dosya biçimiydi. ikili biçimde. Bu yeni XML tabanlı dosya biçimi, küçük dosya boyutları, dosya bozulmasına karşı direnç ve iyi biçimlendirilmiş görüntülerin temsili gibi avantajlarla birlikte geldi. Bu yeni XML tabanlı dosya biçimi, Office 2007'nin bir parçası oldu ve Microsoft'un yeni sürümlerinde de yürütülüyor.

## \_XLSX Dosya Biçimi Özellikleri

\_XLSX dosyası, yeniden adlandırılmış bir XLSX dosyası olduğundan, orijinal dosyayla aynı özelliklere sahiptir. Bu yalnızca [ZIP](/tr/compression/zip/) arşiv dosyası biçimini temel alan bir arşiv dosyasıdır. Bu arşivin içeriğini görmek istiyorsanız, dosyayı .zip uzantılı olarak yeniden adlandırın ve bu Excel çalışma kitabını oluşturan dosyaları görüntülemek için ayıklayın. Boş bir çalışma kitabı, dosyalarına ayıklandığında aşağıdaki kurucu dosya ve klasörlere sahiptir.

### [İçerik_Türleri].xml

Bu, zip çıkarıldığında temel düzeyde bulunan tek dosyadır. Paket içindeki parçalar için içerik türlerini listeler. Pakete dahil edilen XML dosyalarına yapılan tüm referanslara bu XML dosyasında atıfta bulunulur.

### \_rels (Klasör)

Bu, paket düzeyindeki ilişkileri depolayan tek bir XML dosyası içeren İlişkiler klasörüdür. Xlsx dosyalarının önemli bölümlerine bağlantılar bu dosyada URI'ler olarak bulunur. Bu URI'ler, her bir anahtar parçanın paketle olan ilişkisinin türünü tanımlar. Bu, xl/workbook.xml olarak bulunan birincil ofis belgesiyle ve çekirdek ve genişletilmiş özellikler olarak docProps içindeki diğer parçalarla olan ilişkiyi içerir.

### docProps

Bu klasör, genel belge özelliklerini içerir. Bunlar, bir dizi temel özellik, bir dizi genişletilmiş veya uygulamaya özel özellik ve belgenin küçük resim önizlemesini içerir. Boş bir çalışma kitabının bu klasörde app.xml ve core.xml olmak üzere iki dosyası vardır. core.xml, yazar, oluşturulma ve kaydedilme tarihi ve değiştirilme tarihi gibi bilgileri içerir. App.xml, dosyanın içeriği hakkında bilgi içerir.

### xl (Klasör)

Bu, çalışma kitabının içeriğiyle ilgili tüm ayrıntıları içeren ana klasördür. Varsayılan olarak, aşağıdaki klasörlere sahiptir:

* \_rels
* tema
* çalışma sayfaları

ve aşağıdaki xml dosyaları:

* stiller.xml
* çalışma kitabı.xml

## Referanslar

* [MS-XLSX - .xlsx Dosya Biçimi](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

