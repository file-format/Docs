{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MBOX - E-poçt poçt qutusu faylı",
  "description": "MBOX faylları yarada və aça bilən MBOX fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "MBOX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-mbo-azx"
}
},
  "lastmod": "2019-09-10"
}

## MBOX faylı nədir?

MBox fayl formatı elektron poçt mesajlarının toplanması üçün konteyneri təmsil edən ümumi termindir. Mesajlar əlavələri ilə birlikdə konteynerin içərisində saxlanılır. Bütün qovluqdan gələn mesajlar bir verilənlər bazası faylında saxlanılır və yeni mesajlar faylın sonuna əlavə olunur. Çoxsaylı proqramlar və API, Apple Mail və Mozilla Thunderbird kimi MBox fayl formatı üçün dəstək verir.

## MBOX fayl formatı ##

The MBox file format remained non-standardized for quite long time until 2005 when the application/mbox  was standardized as [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Messages, in RFC 2822 format, are concatenated inside MBox file format one after another. Each message begins with a separator line that identifies the message sender, and also identifies the date and time at which the message was received by the final recipient (either the last-hop system in the transfer path, or the system which serves as the recipient's mailstore). Each message is typically terminated by an empty line. The end of the database is usually recognized by either the absence of any additional data, or by the presence of an explicit end-of-file marker.

## MBox faylından mesaj oxunur ##

Oxucu From_ sətirlərini axtaran mbox faylını skan edir. İstənilən From_ sətri mesajın başlanğıcını qeyd edir. Oxucu hər From_ sətirinin (faylın əvvəlindən keçən) boş sətir olması faktından istifadə etməyə çalışmamalıdır. Oxucu mesaj tapdıqdan sonra o, From_ xəttindən zərfin göndəricisini və çatdırılma tarixini çıxarır (ehtimal ki, zədələnmiş). Sonra o, hansının birinci gəldiyindən asılı olaraq növbəti From_ sətrinə və ya faylın sonuna qədər oxunur. O, son boş sətri silir və >From_ sətir və >>From_ sətir və s. sitatlarını silir. Nəticə RFC 822 mesajıdır.

## Kodlaşdırma Mülahizələri ##

Alınan e-poçt Mbox faylını əlavə olaraq ehtiva etdikdə və başqa Mbox faylında saxlandıqda MBox faylının məzmunu geri dönməz şəkildə qarışa bilər. Bunun qarşısını almaq üçün mesajlaşma sistemləri mbox verilənlər bazasını qeyri-şəffaf ötürmə kodlaşdırması ilə (məsələn, BASE64 və ya Sitat-Çap edilə bilən) belə bir obyekt mesajlaşma protokolları vasitəsilə ötürüldükdə kodlamalıdır. Uyğun olmayan məlumatlar alınarsa, icraçılar həmçinin mbox məlumatlarını yerli olaraq kodlaşdırmağa hazır olmalıdırlar.

## İstinadlar ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)

* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)


