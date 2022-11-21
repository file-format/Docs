{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Kanal Tanımlama Formatı",
  "description" :"CDF dosyasının ne olduğunu ve CDF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## CDF dosyası nedir?

.cdf uzantılı bir dosya, sık güncellemeleri "kanallar" olarak yayınlamak için kullanılan XLM tabanlı bir bilgi dağıtım dosyası biçimidir. Bilgiler herhangi bir web sunucusundan yayınlanır ve web tarayıcıları gibi uyumlu alıcı programlara sahip bilgisayarlara otomatik olarak iletilir. Kullanıcılar aktif kanallara abone olur ve masaüstüne planlanmış güncellemeler gönderir.
CDF dosyaları daha önce Microsoft'un Active Channel, Active Desktop ve Smart Offline Favorites teknolojileri ile birlikte kullanılıyordu.

## CDF Dosya Biçimi

CDF dosyaları, bilgi alışverişi için genel bir web dosyası biçimi olan XML dosyaları olarak kaydedilir. CDF dosya formatı artık eski bir formattır ve hiçbir zaman yaygın olarak benimsenmemiştir. Buna kıyasla Netscape'in RSS'si daha ünlüydü ve yaygın olarak kullanılıyordu.

### CDF Dosya Biçimi Örneği

Aşağıda, CDF dosya biçiminin genel bir örneği verilmiştir.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://alan/klasör/"
SON MOD="1998-11-05T22:12"
PRECACHE=EVET
SEVİYE="0">
<TITLE>Kanal Başlığı</TITLE>
<ABSTRACT>Kanal içeriğinin özeti.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    SON MOD="1998-11-05T22:12"
    PRECACHE=EVET
SEVİYE="1">
<TITLE>İkinci Sayfanın Başlığı</TITLE>
<ABSTRACT>Sayfa İki'nin içeriğinin özeti.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Referanslar

* [Kanal Tanım Formatı - Wikipedia Tarafından](https://en.wikipedia.org/wiki/Channel_Definition_Format)

