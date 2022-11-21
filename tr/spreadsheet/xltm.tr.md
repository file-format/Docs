{
  "date" : "2019-12-10",
  "keywords" :[ "XLTM", "dosya", "uzantı", "dosya formatı", "Excel Açık XML Makrosu", "Elektronik Tablo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XLTM dosyasının ne olduğunu ve bunları oluşturabilen ve açabilen API'leri öğrenmek için dosya biçimi kılavuzunuz.",
  "title" :"XLTM dosyası nedir?",
  "linktitle" : "XLTM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## XLTM dosyası nedir?

XLTM dosya uzantısı, Microsoft Excel tarafından Makro özellikli şablon dosyaları olarak oluşturulan dosyaları temsil eder. XLTM dosyaları, yapı olarak [XLTX](/tr/spreadsheet/xltx/) dosyasına benzer, ancak sonraki sürüm makrolarla şablon dosyaları oluşturmayı desteklemez. Bu tür şablon dosyaları, daha sonra benzer XLSX dosyalarının oluşturulmasını kolaylaştırmak için makrolarla birlikte düzen, biçimlendirme ve diğer ayarları oluşturmak ve ayarlamak için kullanılır.

## Kısa Tarih ##

Microsoft, **Office Açık XML** standardına uymak için değişikliğe gitmeye karar verdiğinde 2000 yılının başlarındaydı. Bu yeni Standart kapsamındaki farklı türdeki belgeler, uzantılarına "X" eklenerek tanımlandı; burada "X" XML içindir. 2007 yılına gelindiğinde, bu yeni dosya biçimi Office 2007'nin bir parçası oldu ve Microsoft Office'in yeni sürümlerinde de sürdürülüyor. Yeni dosya türü, küçük dosya boyutları, daha az bozulma değişikliği ve iyi biçimlendirilmiş görüntülerin temsili gibi avantajlar ekledi.

## XLTM Dosya Biçimi Özellikleri ##

XLTM dosyaları, Office OpenXML dosya biçimini temel alır ve dosya boyutunu küçültmek için XML ve [ZIP](/tr/Compression/ZIP/) kullanır. Bunlar, dosyaya çift tıklanarak Microsoft Excel ile açılabilir. Bir XLTM dosya biçimindeki dosya organizasyonu, dosyayı ZIP olarak yeniden adlandırarak ve ardından içeriğini diske çıkararak gözlemlenebilir.

### [Content_Types].xml ###

Bu, zip çıkarıldığında temel düzeyde bulunan tek dosyadır. Paket içindeki parçalar için içerik türlerini listeler. Pakete dahil edilen XML dosyalarına yapılan tüm referanslara bu XML dosyasında atıfta bulunulur.

### \_rels (Klasör) ###

Bu, paket düzeyindeki ilişkileri depolayan tek bir XML dosyası içeren İlişkiler klasörüdür. Xltx dosyalarının önemli bölümlerine bağlantılar bu dosyada URI'ler olarak bulunur. Bu URI'ler, her bir anahtar parçanın paketle olan ilişkisinin türünü tanımlar. Bu, xl/workbook.xml olarak bulunan birincil ofis belgesiyle ve temel ve genişletilmiş özellikler olarak docProps içindeki diğer parçalarla olan ilişkiyi içerir.

### docProps ###

Bu klasör, genel belge özelliklerini içerir. Bunlar, bir dizi temel özellik, bir dizi genişletilmiş veya uygulamaya özel özellik ve belgenin küçük resim önizlemesini içerir. Boş bir çalışma kitabının bu klasörde app.xml ve core.xml olmak üzere iki dosyası vardır. core.xml, yazar, oluşturulma ve kaydedilme tarihi ve değiştirilme tarihi gibi bilgileri içerir. App.xml, dosyanın içeriği hakkında bilgi içerir.

### xl (Klasör) ###

Bu, çalışma kitabının içeriğiyle ilgili tüm ayrıntıları içeren ana klasördür. Varsayılan olarak, aşağıdaki klasörlere sahiptir:

* \_rels
* tema
* çalışma sayfaları

ve aşağıdaki xml dosyaları:

* stiller.xml
* çalışma kitabı.xml

## Referanslar ##

* [MS-XLSX Dosya Biçimi](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

