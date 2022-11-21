{
  "date" : "2019-12-10",
  "keywords" :[ "XLTX", "dosya", "uzantı", "dosya formatı", "Excel Açık XML", "Elektronik Tablo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XLTX dosyasının ne olduğunu ve bunları oluşturabilen ve açabilen API'leri öğrenmek için dosya biçimi kılavuzunuz.",
  "title" :"XLTX dosyası nedir?",
  "linktitle" : "XLTX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## XLTX dosyası nedir?

.xltx uzantılı dosyalar, Office OpenXML dosya biçimi belirtimlerini temel alan Microsoft Excel Şablonu dosyalarını temsil eder. XLTX dosyasında belirtilen ayarların aynısını sergileyen [XLSX](/tr/spreadsheet/xlsx/) dosyaları oluşturmak için kullanılabilecek standart bir şablon dosyası oluşturmak için kullanılır.

## Kısa Tarihçe

Microsoft, **Office Açık XML** standardına uymak için değişikliğe gitmeye karar verdiğinde 2000 yılının başlarındaydı. Bu yeni Standart kapsamındaki farklı türdeki belgeler, uzantılarına "X" eklenerek tanımlandı; burada "X" XML içindir. 2007 yılına gelindiğinde, bu yeni dosya biçimi Office 2007'nin bir parçası oldu ve Microsoft Office'in yeni sürümlerinde de sürdürülüyor. Yeni dosya türü, küçük dosya boyutları, daha az bozulma değişikliği ve iyi biçimlendirilmiş görüntülerin temsili gibi avantajlar ekledi.

## XLTX Dosya Biçimi Özellikleri

XLTX dosyaları, Office OpenXML dosya biçimini temel alır ve dosya boyutunu küçültmek için XML ve [ZIP](/tr/compression/zip/) kullanır. İkili XLT dosya biçimini değiştirmek için Microsoft Office 2007'nin piyasaya sürülmesiyle oluşturuldu. XLTX'e benzer şekilde, XLT dosya formatı, Microsoft Excel 2003 ve 2007 kullanılarak [XLS](/tr/spreadsheet/xls/) dosyaları oluşturmak için kullanılabilir. Bunlar, dosyaya çift tıklanarak Microsoft Excel ile açılabilir. Bir XLTX dosya biçimindeki dosya organizasyonu, dosyayı ZIP olarak yeniden adlandırarak ve ardından içeriğini diske çıkararak gözlemlenebilir.

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

* [[MS-XLSX] - .Xlsx Dosya Biçimi](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

