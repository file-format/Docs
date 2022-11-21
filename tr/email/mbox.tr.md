{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - E-posta Posta Kutusu Dosyası",
  "description":"MBOX dosya formatı ve MBOX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## MBOX dosyası nedir?

MBox dosya formatı, elektronik posta mesajlarının toplanması için bir kapsayıcıyı temsil eden genel bir terimdir. İletiler, ekleriyle birlikte kabın içinde saklanır. Tüm bir klasördeki mesajlar tek bir veritabanı dosyasına kaydedilir ve yeni mesajlar dosyanın sonuna eklenir. Çok sayıda uygulama ve API, Apple Mail ve Mozilla Thunderbird gibi MBox dosya biçimini destekler.

## MBOX Dosya Biçimi ##

MBox dosya formatı, uygulamanın/mbox'ın RFC 2822 formatında [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Mesajlar olarak standartlaştırıldığı 2005 yılına kadar oldukça uzun bir süre standart dışı kaldı. , birbiri ardına MBox dosya biçiminde birleştirilir. Her mesaj, mesajı göndereni tanımlayan bir ayırıcı çizgi ile başlar ve ayrıca mesajın son alıcı (aktarım yolundaki son atlama sistemi veya alıcı olarak hizmet veren sistem) tarafından alındığı tarih ve saati de tanımlar. posta deposu). Her mesaj tipik olarak boş bir satırla sonlandırılır. Veritabanının sonu, genellikle herhangi bir ek verinin olmamasıyla veya açık bir dosya sonu işaretçisinin varlığıyla tanınır.

## MBox Dosyasından Mesaj Okuma ##

Bir okuyucu, From_ satırlarını arayan bir mbox dosyasını tarar. Herhangi bir From_ satırı, bir mesajın başlangıcını işaretler. Okuyucu, her From_ satırının (dosyanın başlangıcından sonra) boş olması gerçeğinden yararlanmaya çalışmamalıdır. Okuyucu bir mesaj bulduğunda, Kimden_ satırından (muhtemelen bozuk) bir zarf göndericisini ve teslim tarihini çıkarır. Ardından, hangisi önce gelirse, bir sonraki From_ satırına veya dosyanın sonuna kadar okur. Son boş satırı çıkarır ve >Satırlardan_ ve >>Satırlardan_ vb alıntıları siler. Sonuç, bir RFC 822 mesajıdır.

## Kodlama Hususları ##

Alınan bir e-posta ek olarak bir Mbox dosyası içerdiğinde ve başka bir Mbox dosyasına kaydedildiğinde, bir MBox dosyasının içeriği geri alınamaz şekilde birbirine karışabilir. Bundan kaçınmak için, mesajlaşma sistemleri, böyle bir nesne mesajlaşma protokolleri aracılığıyla aktarıldığında şeffaf olmayan aktarım kodlaması (BASE64 veya Alıntılanmış-Yazdırılabilir gibi) ile bir mbox veritabanını kodlamalıdır. Uygulayıcılar, uyumlu olmayan veriler alındığında mbox verilerini yerel olarak kodlamaya da hazırlıklı olmalıdır.

## Referanslar ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)

