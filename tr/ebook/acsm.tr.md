{
  "date" : "2021-03-10",
  "keywords" :[ "ACSM", "Adobe Content Server Mesajı", "uzantı", "biçim", "eKitap", "dosya", "Adobe Digital Editions"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Adobe tarafından sağlanan ACSM dosya formatı ve ACSM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"ACSM - Adobe İçerik Sunucusu Mesaj Dosyası Formatı",
  "linktitle" : "ACSM",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## ACSM dosyası nedir?

.acsm uzantılı dosyalara Adobe Content Server Mesaj dosyaları denir. Bu dosyalar **Adobe Digital Editions** tarafından Adobe DRM korumalı içeriği etkinleştirmek ve indirmek için kullanılır. Aslında, bir ACSM dosyası bir e-Kitap dosyası değildir; diğer e-Kitaplar (ör. PDF) gibi açılıp okunamaz; Yalnızca bir e-kitabı etkinleştirmek ve indirmek için gereken verileri içerir. Bu, bir ACSM dosyasının yalnızca Adobe sunucularıyla iletişim kuran bilgilerden oluştuğu anlamına gelir. Digital Editions kullanıcıları, bir e-Kitap indireceklerse ACSM dosyasını görebilirler, ancak indirme işlemi herhangi bir nedenle durmuş olabilir. Kullanıcılar, .acsm dosyasına çift tıklayarak indirmeye devam edebilir.

## ACSM dosyası nasıl çalışır?

Adobe Content Server, e-Kitapları ve diğer dijital öğeleri korumaktan sorumlu olduğundan. Satın alma işleminden sonra içerik otomatik olarak alıcının Adobe ID'sine bağlanır. Kimlik özeldir ve başkalarına aktarılamaz. Kullanıcı, Adobe kopya korumalı herhangi bir belge satın almadan önce bunu ayarlamalıdır. Müşteriler, Adobe ID'lerini arka planda çalışan Adobe sunucu uygulamasına geçirmeden kopya korumalı belgelerine erişemezler.

Müşteriler satın alma işlemini gerçekleştirdiklerinde, ilk başta indirebilecekleri tek dosya ACSM'dir. ACSM dosyasını açmak için müşterinin sistemine Adobe Digital Editions yazılımını yüklemiş ve bunu Adobe ID'sine bağlamış olması gerekir. Adobe Digital Editions, ACSM dosyasını dönüştürme yetkisi için kimliği doğrulayacaktır. Kimliği doğrulanırsa, kullanıcı eKitaplarını [EPUB](/tr/ebook/epub/) veya [PDF](/tr/pdf/) formatında indirebilir. Adobe Digital Editions ayrıca indirme dizinini tanımak için ACSM dosyasını kullanır.

## Referanslar

* [Adobe Content Server - Wikipedia Tarafından](https://en.wikipedia.org/wiki/Adobe_Content_Server)


