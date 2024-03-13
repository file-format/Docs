{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CDF - Kanal Tərifi Format",
  "description": "CDF faylı və CDF faylları yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "CDF",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cd-azf"
}
},
  "lastmod": "2021-08-18"
}

## CDF faylı nədir?

.cdf uzantılı fayl XLM əsaslı məlumat paylama fayl formatıdır və tez-tez yenilənmələri kanallar kimi dərc etmək üçün istifadə olunur. Məlumat istənilən veb serverdən dərc edilir və avtomatik olaraq veb brauzerlər kimi uyğun qəbuledici proqramları olan kompüterlərə çatdırılır. İstifadəçilər aktiv kanallara abunə olurlar və planlaşdırılmış yeniləmələri masaüstünə çatdırırlar.
CDF faylları əvvəllər Microsoft-un Active Channel, Active Desktop və Smart Offline Favorites texnologiyaları ilə birlikdə istifadə edilmişdir.

## CDF fayl formatı

CDF faylları məlumat mübadiləsi üçün ümumi veb fayl formatı olan XML faylları kimi saxlanılır. CDF fayl formatı indi köhnə formatdır və heç vaxt geniş şəkildə qəbul edilməmişdir. Bununla müqayisədə, Netscape-in RSS-i daha məşhur idi və geniş istifadə olunurdu.

### CDF Fayl Formatının Nümunəsi

Aşağıda CDF fayl formatının ümumi nümunəsi verilmişdir.

```
<?xml version=1.0 encoding=UTF-8?>
<CHANNEL HREF=http://domain/folder/pageOne.extension
BASE=http://domain/qovluq/
LASTMOD=1998-11-05T22:12
PRECACHE=Bəli
LEVEL=0>
<TITLE>Kanalın Başlığı</TITLE>
<ABSTRACT>Kanalın məzmununun xülasəsi.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY=14/>
</SCHEDULE>
<LOGO HREF=wideChannelLogo.gif STYLE=IMAGE-WIDE/>
<LOGO HREF=imageChannelLogo.gif STYLE=IMAGE/>
<LOGO HREF=iconChannelLogo.gif STYLE=ICON/>
<ITEM HREF=pageTwo.extension
    LASTMOD=1998-11-05T22:12
    PRECACHE=Bəli
LEVEL=1>
<TITLE>İkinci Səhifənin Başlığı</TITLE>
<ABSTRACT>İkinci Səhifənin məzmununun xülasəsi.</ABSTRACT>
<LOGO HREF=pageTwoLogo.gif STYLE=IMAGE/>
<LOGO HREF=pageTwoLogo.gif STYLE=ICON/>
</ITEM>
</CHANNEL>
```

## İstinadlar

* [Kanal Tərifi Format - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Channel_Definition_Format)


