{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Format Definisi Saluran",
  "description" :"Pelajari tentang apa itu file CDF dan API yang dapat membuat dan membuka file CDF.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## Apa itu file CDF?

File dengan ekstensi .cdf adalah format file distribusi informasi berbasis XLM yang digunakan untuk menerbitkan pembaruan yang sering dilakukan sebagai "saluran". Informasi tersebut diterbitkan dari server web mana pun dan secara otomatis dikirim ke komputer dengan program penerima yang kompatibel seperti browser web. Pengguna berlangganan saluran aktif dan menjadwalkan pembaruan yang dikirimkan ke desktop mereka.
File CDF sebelumnya digunakan bersama dengan teknologi Microsoft Active Channel, Active Desktop dan Smart Offline Favorites.

## Format File CDF

File CDF disimpan sebagai file XML yang merupakan format file web umum untuk pertukaran informasi. Format file CDF adalah format lama sekarang dan tidak pernah diadopsi secara luas. Dibandingkan dengan ini, RSS Netscape lebih terkenal dan banyak digunakan.

### Contoh Format File CDF

Berikut ini adalah contoh umum dari format file CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://domain/folder/"
LASTMOD="1998-11-05T22:12"
PRECACHE = "YA"
TINGKAT="0">
<TITLE>Judul Saluran</TITLE>
<ABSTRACT>Sinopsis konten saluran.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE = "YA"
TINGKAT="1">
<TITLE>Judul Halaman Dua</TITLE>
<ABSTRACT>Sinopsis konten Halaman Dua.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Referensi

* [Format Definisi Saluran - Oleh Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)

