{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Microsoft Outlook E-posta Biçimi",
  "description":"MSG dosya formatı ve MSG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## MSG dosyası nedir?

MSG, e-posta mesajlarını depolamak için [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) ve Exchange tarafından kullanılan bir dosya biçimidir. , iletişim, randevu veya diğer görevler. Bu tür mesajlar, gönderen, alıcı, konu, tarih ve mesaj gövdesi veya iletişim bilgileri, randevu ayrıntıları ve bir veya daha fazla görev belirtimi içeren bir veya daha fazla e-posta alanı içerebilir. Dahil olmak üzere Mesaj nesnesini oluşturan özellikler de MSG dosyasının bir parçasıdır. MSG dosyası, düz ASCII metni olarak başlıklara, ana mesaj gövdesine ve köprülere sahiptir. MSG dosyaları, Microsoft'un Mesajlaşma Uygulamaları Programlama Arayüzüne (MAPI) ihtiyaç duyan programlarla da uyumludur.

## MSG Dosya Yapısı

CFB_3 formatı, MSG dosyasının temelidir. Paradigma, dizinlere ve dosyalara oldukça yakın olan depolar ve akış kavramlarına dayanmaktadır. Bu nedenle, öncekindeki en büyük fark, bileşik dosya adı verilen ayrı bir dosyada paketlenmiş tüm hiyerarşidir. Nesneler mesaj dosyalarını oluşturur ve tek bir özellikten veya koleksiyonlarından oluşur. Bu yetenek, uygulamaların karmaşık, yapılandırılmış verileri tek bir dosyada depolamasını kolaylaştırır. Bu biçim aynı zamanda birden fazla depolamayı belirtir, her depolama, Mesaj nesnesini ana bileşen olarak temsil eder. Bu depolar, o bileşenin bir özelliğini temsil eden bir dizi akış içerir. Depolamanın yuvalanması da mümkündür.

## Mapi Özellikleri

.msg dosyasının en üst seviyesinde, depolar, içlerinde özellikleri depolayan akışları içerir. Özellikler aşağıdaki gibi kategorize edilebilir:

* Sabit uzunluk özellikleri
* Değişken uzunluk özellikleri
* Çok değerli özellikler

Kategoriden bağımsız olarak, bir özellik ya etiketlenir ya da adlandırılır. Ancak, adlandırılmış özellikler için eşleme depolarında belirtildiği gibi uygun eşleme bilgileri gereklidir.

## Depolar

Depolar, Mesaj nesnesinin temel bileşenlerini oluşturur. MSG dosya formatı aşağıdaki depoları belirtir:

## Üst Düzey Yapı

Mesaj nesnesi, MSG dosya formatının tüm üst seviyesini temsil eder. Türüne, özelliklerine, alıcı sayısına ve Ek nesnelerine bağlı olarak, bir mesaj nesnesinin karşılık gelen .MSG dosyasında farklı akış depoları olabilir.

### Diğer Yapılarla İlişki

Msg dosya biçimi, diğer yapılarla aşağıdaki ilişkilere sahiptir:

* .msg'nin temeli Bileşik Dosya İkili Dosya Biçimidir.
* İleti ve Ek Nesne Protokolü tarafından kullanılan özellikler bu format tarafından kullanılır.

## MSG Formatlarından kaçınmak için senaryolar

İleti nesnesi, .msg dosya sistemini kullanan istemciler veya ileti depoları arasında paylaşılabilir. Bir Mesaj nesnesini .msg dosya biçiminde saklamanın uygun olmayacağı birkaç durum vardır. Örneğin:

* Büyük bir bağımsız arşivin sürdürülmesi durumunda, görünümlerin daha kesin bir şekilde işlenebileceği tam özellikli bir format kullanmak daha iyidir.
* Alıcı bilinmiyorsa, formatın alıcı tarafından desteklenmemesi ve özel veya alakasız teslim edilmesi mümkündür.

## MSG Dosyası Örneği

Bir MSG dosyasının nasıl göründüğü hakkında bir fikir edinmek için bir [örnek MSG dosyası](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) indirebilir ve bilgisayarınızda açabilirsiniz. içeriğini görüntülemek için bilgisayar.

## Referanslar

* [[MS-OXMSG]: Outlook MSG Dosya Biçimi](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

