{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "dosya", "uzantı", "dosya formatı", "Excel", "Elektronik Tablo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XLSX dosyasının ne olduğu ve XLSX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"XLSX Dosya Formatı - XLSX dosyası nedir?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## XLSX dosyası nedir?

**XLSX**, Microsoft tarafından Microsoft Office 2007'nin piyasaya sürülmesiyle kullanıma sunulan Microsoft Excel belgeleri için iyi bilinen bir biçimdir. [Bölüm 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm), OOXML standardı ECMA-376'nın yeni biçimi, bir dizi XML dosyası içeren bir zip paketidir. Altta yatan yapı ve dosyalar, yalnızca .xlsx dosyasını açarak incelenebilir.

## XLSX Dosya Biçiminin Kısa Tarihi

XLSX dosya formatı 2007'de tanıtıldı ve Microsoft tarafından 2000'de uyarlanan Açık XML standardını kullanıyor. XLSX'ten önce, kullanılan yaygın dosya formatı, saf ikili dosya formatı olan [XLS](/tr/spreadsheet/xls/) idi. Yeni dosya türü, küçük dosya boyutları, daha az bozulma değişikliği ve iyi biçimlendirilmiş görüntülerin temsili gibi avantajlar ekledi. Microsoft, **Office Açık XML** standardına uymak için değişikliğe gitmeye karar verdiğinde 2000 yılının başlarındaydı. 2007 yılına gelindiğinde, bu yeni dosya biçimi Office 2007'nin bir parçası oldu ve Microsoft Office'in yeni sürümlerinde de sürdürülüyor.

## XLSX Dosya Biçimi Özellikleri

Resmi [XLSX dosya biçimi belirtimleri](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) Microsoft'tan çevrimiçi olarak edinilebilir. XLSX dosyasının içinde ne olduğunu görmek için, uzantısını değiştirerek onu [ZIP](/tr/compression/zip/) dosyası olarak yeniden adlandırın ve ardından bu Excel çalışma kitabının kurucu dosyalarını görüntülemek için ayıklayın. Boş bir çalışma kitabı, dosyalarına ayıklandığında aşağıdaki kurucu dosya ve klasörlere sahiptir.

### [Content_Types].xml ###

Bu, zip çıkarıldığında temel düzeyde bulunan tek dosyadır. Paket içindeki parçalar için içerik türlerini listeler. Pakete dahil edilen XML dosyalarına yapılan tüm referanslara bu XML dosyasında atıfta bulunulur.

### \_rels (Klasör) ###

Bu, paket düzeyindeki ilişkileri depolayan tek bir XML dosyası içeren İlişkiler klasörüdür. Xlsx dosyalarının önemli bölümlerine bağlantılar bu dosyada URI'ler olarak bulunur. Bu URI'ler, her bir anahtar parçanın paketle olan ilişkisinin türünü tanımlar. Bu, xl/workbook.xml olarak bulunan birincil ofis belgesiyle ve çekirdek ve genişletilmiş özellikler olarak docProps içindeki diğer parçalarla olan ilişkiyi içerir.

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

## XLSX Biçim Örneği ##


Bir çalışma kitabında bulunan her Excel çalışma sayfası için bir XML dosyası vardır. Bu XML dosyalarını xl/worksheets klasöründe bulabilirsiniz. Bir çalışma sayfasında yer alan tüm bilgiler, XML dosyasındaki farklı bölümlerde düzenlenmiştir. Aşağıdaki görseldeki çalışma kitabından örnek bir çalışma sayfasını inceleyelim.

{{< figure src="../XLSX file format.png" alt="XLSX Dosya Biçimi" >}}

Görülebileceği gibi, bu çalışma sayfası A1'den B2'ye kadar olan hücrelerin içeriğini ve bir görüntüyü içermektedir. Ek olarak, G13 hücresi şu anda çalışma sayfasındaki etkin hücredir. Şimdi bu bilgilerin XML dosyasında nasıl temsil edildiğini görmek için xl/worksheets/sheet1.xml dosyasını inceleyelim. Bu XML dosyasının içeriği aşağıda gösterildiği gibidir.

{{< figure src="../XLSX File Format Details.png" alt="XPS Dosya Biçimi" >}}

1. Sekmeye tema rengi uygulanmış. Etiketli XML dosyasında bahsedilmiştir.<tabColor> tema kimliğinin ardından.
1. tabSelected değeri, bunun seçilen sayfa olduğunu gösteren 1'e ayarlanır.
1. Yukarıdaki ilk görselde görüldüğü gibi çalışma sayfasındaki G13 hücresi XML dosyasında da bahsedilen aktif hücredir.
1. SheetData sekmesi, çalışma sayfasında bulunan verileri temsil eder. Ancak, çalışma sayfasının orijinal içeriğinin bu bölümde hiçbir yerde olmadığını görebilirsiniz. Bunun nedeni, metnin dolaylı olarak "sharedStrings" XML sayfasından yönlendirilmesidir. Bu bağlantı, her metnin yalnızca bir kez kaydedilmesini ve yerden tasarruf etmek için tekrar referans alınabilmesini sağlar.
1. Görüldüğü şekliyle görüntü, "rId2" referans kimliği ile referanslandırılmıştır.

## Katkıda bulunmak

XLSX veya Elektronik Tablo dosya formatları hakkında bir şeyler mi paylaşmak istiyorsunuz? Bulgularınızı [Elektronik Tablo Dosya Biçimi Haberleri](https://news.fileformat.com/t/Spreadsheet) bölümünde yayınlayabilirsiniz.

## Referanslar

* [[MS-XLSX] - XLSX Dosya Biçimi](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

