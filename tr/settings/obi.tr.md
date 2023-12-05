{
"tarih": "2023-05-02",
  "keywords": [
"obi dosyası",
"obi dosyası nedir",
"obi dosyasının formatı nedir",
"dosya",
"obi dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "OBI Dosya Formatı - Outlook RSS Abonelik Dosyası",
  "description":"OBI formatı ve OBI dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle" : "OBI",
  "menu": {
    "docs": {
      "identifier": "settings-obi",
      "parent": "settings"
}
},
"sonmod": "2023-05-02"
}

## .OBI dosyası nedir?

OBI dosyası, kullanıcıların Microsoft Outlook'ta bir RSS akışına abone olmasına olanak tanıyan Outlook RSS Abonelik Dosyasıdır. RSS, blog gönderileri, haber başlıkları veya podcast'ler gibi sıklıkla güncellenen içerikleri yayınlamak için kullanılan bir web besleme formatı olan Gerçekten Basit Dağıtım anlamına gelir.

Outlook'ta RSS akışına abone olmak için kullanıcılar bir web sitesindeki RSS akışı bağlantısını tıklayabilir veya RSS akışının URL'sini kopyalayıp Outlook'taki "Yeni RSS Akışı Ekle" iletişim kutusuna yapıştırabilir. Outlook daha sonra yeni içerik için RSS akışını düzenli aralıklarla kontrol edecek ve bunu kullanıcının RSS Akışı klasöründe görüntüleyecektir.

Outlook RSS Abonelik Dosyaları ".rss" dosya uzantısına sahiptir. Bu dosyalar RSS akışının URL'sini içerir ve RSS akışı aboneliklerini başkalarıyla paylaşmak veya RSS akışı aboneliklerini yedeklemek ve geri yüklemek için kullanılabilir.

## OBI Dosya Formatı - Daha Fazla Bilgi

OBI dosyaları OPML (Anahat İşlemci İşaretleme Dili) dosyası olarak bilinir ve Microsoft Outlook'ta abone olunan RSS beslemesi URL'lerinin listesini içerir.

Kullanıcı RSS beslemelerini OBI dosyasına aktardığında, bu dosya abone oldukları tüm RSS beslemelerinin listesini, her beslemenin başlığı, beslemenin URL'si ve diğer ilgili bilgiler dahil olmak üzere içerir. Bu, kullanıcıların RSS beslemesi aboneliklerini başka bir RSS okuyucuya kolayca aktarmalarına veya aboneliklerini koruma amacıyla yedeklemelerine olanak tanır.

OBI dosyaları, RSS beslemesi aboneliklerini Microsoft Outlook'a veya başka bir RSS okuyucuya aktarmak için de kullanılabilir. OBI dosyasını Outlook'a aktarmak için kullanıcılar "Dosya" > "Aç ve Dışa Aktar" > "İçe/Dışa Aktar" > "Başka bir programdan veya dosyadan içe aktar" > "Sonraki" > "RSS Akışlarını bir OPML dosyasından içe aktar" seçeneğine tıklayabilir ve daha sonra bilgisayarlarındaki OBI dosyasının konumuna göz atın.

## OBI dosyasının formatı nedir?

OBI dosyası olarak da bilinen Outlook RSS Abonelik Dosyası, dosyanın yapısını ve içeriğini tanımlamak için XML (Genişletilebilir İşaretleme Dili) kullanır.

OBI dosyaları, her biri kendi nitelik ve değer kümesine sahip bir dizi iç içe geçmiş öğeden oluşur. OBI dosyasındaki ana öğe, beslemenin başlığı, beslemenin URL'si ve diğer ilgili bilgiler de dahil olmak üzere RSS beslemesi hakkındaki bilgileri içeren "anahat" öğesidir.

Her "anahat" öğesi, RSS besleme listesindeki alt klasörleri veya alt kategorileri temsil eden alt öğeleri de içerebilir. OBI dosyasının yapısı, RSS beslemesi aboneliklerinin kolay organizasyonuna ve yönetimine olanak tanır ve farklı RSS okuyucuları arasında aboneliklerin aktarılması veya aboneliklerin yedeklenmesi ve geri yüklenmesi için kullanılabilir.

## Referanslar
* [RSS yayınları nedir?](https://support.microsoft.com/en-us/office/what-are-rss-feeds-e8aaebc3-a0a7-40cd-9e10-88f9c1e74b97)

