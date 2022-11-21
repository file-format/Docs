{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - Microsoft Outlook E-posta Şablon Dosyası",
  "description":"OFT dosya formatı ve OFT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## OFT dosyası nedir?

.oft uzantılı dosyalar, Microsoft Outlook kullanılarak oluşturulan şablon dosyalarıdır. Mesaj şablonları için ayarlanan önceden biçimlendirilmiş düzen, zaman kazanmak için ortak bilgiler içeren e-postaların gönderilmesi için kullanılır. Bu tür dosyalar, yeni bir e-posta oluşturularak, gerekli bilgiler eklenerek ve ardından Microsoft Outlook'tan Office Şablonu Olarak Kaydet (.oft) açılır menüsü kullanılarak oluşturulabilir. Kullanıcılar, OFT dosyalarını çift tıklatarak açabilir ve o sistemdeki ilgili uygulamada açılır.

## OFT Dosya Yapısı ##

.OFT dosya biçimi, temelinde [MSG](/tr/email/msg/) dosya biçimini kullanır. Tek fark, OFT dosyalarının depolama sınıfı (WriteClassStg) olarak CLSID_TemplateMessage ({0006F046-0000-0000-C000-000000000046}) olması, MSG dosyalarının ise CLSID_MailMessage ({00020D0B-0000-0000-C000-000000000046}) kullanmasıdır.

CFB_3 formatı, MSG dosyasının temelidir. Paradigma, dizinlere ve dosyalara oldukça yakın olan depolar ve akış kavramlarına dayanmaktadır. Bu nedenle, öncekindeki en büyük fark, bileşik dosya adı verilen ayrı bir dosyada paketlenmiş tüm hiyerarşidir. Nesneler mesaj dosyalarını oluşturur ve tek bir özellikten veya koleksiyonlarından oluşur. Bu yetenek, uygulamaların karmaşık, yapılandırılmış verileri tek bir dosyada depolamasını kolaylaştırır. Bu biçim aynı zamanda birden fazla depolamayı belirtir, her depolama, Mesaj nesnesini ana bileşen olarak temsil eder. Bu depolar, o bileşenin bir özelliğini temsil eden bir dizi akış içerir. Depolamanın yuvalanması da mümkündür.

### OFT Özellikleri

.msg dosyasının en üst seviyesinde, depolar, içlerinde özellikleri depolayan akışları içerir. Özellikler aşağıdaki gibi kategorize edilebilir:

* Sabit uzunluk özellikleri
* Değişken uzunluk özellikleri
* Çok değerli özellikler

Kategoriden bağımsız olarak, bir özellik ya etiketlenir ya da adlandırılır. Ancak, adlandırılmış özellikler için eşleme depolarında belirtildiği gibi uygun eşleme bilgileri gereklidir.

### OFT Depoları

Depolar, Mesaj nesnesinin temel bileşenlerini oluşturur. MSG dosya formatı aşağıdaki depoları belirtir:

### Üst Düzey Yapı

Mesaj nesnesi, Mesaj dosyası formatının tüm üst seviyesini temsil eder. Türüne, özelliklerine, alıcı sayısına ve Ek nesnelerine bağlı olarak, bir mesaj nesnesinin karşılık gelen .MSG dosyasında farklı akış depoları olabilir.

#### Diğer Yapılarla İlişki

MSG/OFT dosya biçimi, diğer yapılarla aşağıdaki ilişkilere sahiptir:

* .msg'nin temeli Bileşik Dosya İkili Dosya Biçimidir.
* İleti ve Ek Nesne Protokolü tarafından kullanılan özellikler bu format tarafından kullanılır.

## Referanslar

* [[MS-OXMSG]: Outlook MSG Dosya Biçimi](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

