{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "dosya", "uzantı", "dosya formatı", "Microsoft Excel Makro Dosyası", "Elektronik Tablo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XLM Makroları dosyasının ne olduğunu ve XLM dosyalarını oluşturabilen ve açabilen API'leri öğrenmek için dosya biçimi kılavuzunuz.",
  "title" :"XLM dosyası nedir?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## XLM dosyası nedir?

XLM, Excel Makrosu için, Makroları depolamak için kullanılan bir Elektronik Tablo dosyası türüdür. Uygulama açısından, bir Makro, işlemleri otomatikleştirmek için kullanılan talimatlar kümesidir. [XLS](/tr/spreadsheet/xls/) dosya formatı için tekrar tekrar gerçekleştirilen adımları kaydetmek için bir makro kullanılır ve makroyu tekrar çalıştırarak işlemlerin yapılmasını kolaylaştırır. Makrolar, Visual Basic Düzenleyici kullanılarak Excel Çalışma Kitabı içinden Microsoft'un Visual Basic for Applications (VBA) ile programlanır ve doğrudan oradan çalıştırılabilir/hata ayıklanabilir.

## Kısa Tarih ##

Microsoft Excel, halka açık ilk lansmanından bu yana makroların programlanmasını destekledi. Makroların özellikleri, yeni özelliklere göre uzantılı Excel'in sonraki sürümlerinde aynı kaldı. XLM, Excel 4.0 aracılığıyla Excel için varsayılan makro diliydi. Excel 5.0, makroları varsayılan olarak VBA'da kaydetti, ancak sürüm 5.0 XLM kaydına bir seçenek olarak hala izin veriliyordu. 5.0 sürümünden sonra bu seçenek kullanımdan kaldırıldı. Excel 2010 dahil olmak üzere Excel'in tüm sürümleri, bir XLM makrosu çalıştırabilir, ancak Microsoft bunların kullanılmasını önermez.

## XLM'de Makro Kaydetme ##

Excel, makro kaydetmek için kullanımı kolay adımlar sağlar. Makrolarla çalışmak için Geliştirici araçlarının kurulu olmasını gerektirir. Bir makro kaydı devam ederken, daha sonra oynatılmak üzere her kullanıcı eylemini kaydeder. Makro kaydı aslında bir kullanıcının kayıt başladıktan sonra gerçekleştirdiği tüm adımları içerir. Böylece bir makro kaydı başlatıldıktan sonra hücre içeriğini kalın, italik yaparsanız ve metin yaslamasını ayarlarsanız, tüm bu komutlar kaydedilecektir. Kaydedilen her makroya daha sonra hızlı oynatma için bir kısayol da atanabilir. Makro kaydı, Visual Basic Editor (VBE) kullanılarak düzenlenebilen bir makro biçiminde VBA kodu üretir.

## Excel Nesne Modeli ##

Makrolar arkalarında VBA rutinlerini kullanır ve bu amaçla [Excel Nesne Modeli](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model)'i takip eder. Bu model, kullanıcı tanımlı komut araç çubukları, komut çubukları veya mesaj kutuları aracılığıyla elektronik tabloyla etkileşim için bir elektronik tablonun nesnelerini tanımlar. Örneğin, çalışma kitabının özelliklerine erişim Workbook nesnesi ile verilir. Benzer şekilde, çalışma kitabının çalışma sayfalarıyla programlı olarak çalışmak için modelde Worksheet nesnesi vardır.

## Makrolar ve Güvenlik ##

VBA, tüm uygulama alanlarına ve dosya sistemine erişim sağlar ve aynı zamanda tehlikeli olabilir. Bu, çalışma kitabını, dosyayı kendi ucunda çalıştırabilen biriyle paylaşırken endişe uyandırır. Yani Microsoft Excel böyle bir dosyayı açma konusunda uyarıyor. Diğer kullanıcıların güvenilir olduklarını doğrulaması için makrolar dijital imza ile onaylanabilir. Böylece, kaynakları doğrulandıktan sonra makrolar etkinleştirilebilir.

## Referanslar ##

* [[MS-XLS] - Excel İkili Dosya Biçimi Yapısı](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Makro Programlama](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

