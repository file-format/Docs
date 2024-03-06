{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CDF — kanāla definīcijas formāts",
  "description": "Uzziniet, kas ir CDF fails un API, kas var izveidot un atvērt CDF failus.",
  "linktitle": "CDF",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cd-lvf"
}
},
  "lastmod": "2021-08-18"
}

## Kas ir CDF fails?

Fails ar paplašinājumu .cdf ir uz XLM balstīts informācijas izplatīšanas faila formāts, kas tika izmantots, lai publicētu biežus atjauninājumus kā kanālus. Informācija tiek publicēta no jebkura tīmekļa servera un automātiski tiek piegādāta datoros ar saderīgām uztveršanas programmām, piemēram, tīmekļa pārlūkprogrammām. Lietotāji abonē aktīvos kanālus, un viņu darbvirsmā tiek piegādāti plānotie atjauninājumi.
CDF faili iepriekš tika izmantoti kopā ar Microsoft Active Channel, Active Desktop un Smart Offline Favorites tehnoloģijām.

## CDF faila formāts

CDF faili tiek saglabāti kā XML faili, kas ir vispārīgs tīmekļa faila formāts informācijas apmaiņai. CDF faila formāts tagad ir vecs formāts un nekad nav plaši pieņemts. Salīdzinot ar šo, Netscape RSS bija vairāk slavens un plaši izmantots.

### CDF faila formāta piemērs

Tālāk ir sniegts vispārīgs CDF faila formāta piemērs.

```
<?xml version=1.0 encoding=UTF-8?>
<CHANNEL HREF=http://domain/folder/pageOne.extension
BASE=http://domēns/mape/
LASTMOD=1998-11-05T22:12
PRECACHE=JĀ
LEVEL=0>
<TITLE>Kanāla nosaukums</TITLE>
<ABSTRACT>Kanāla satura kopsavilkums.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY=14/>
</SCHEDULE>
<LOGO HREF=wideChannelLogo.gif STYLE=IMAGE-WIDE/>
<LOGO HREF=imageChannelLogo.gif STYLE=IMAGE/>
<LOGO HREF=iconChannelLogo.gif STYLE=ICON/>
<ITEM HREF=pageTwo.extension
    LASTMOD=1998-11-05T22:12
    PRECACHE=JĀ
LEVEL=1>
<TITLE>Otrās lapas nosaukums</TITLE>
<ABSTRACT>Otrās lapas satura kopsavilkums.</ABSTRACT>
<LOGO HREF=pageTwoLogo.gif STYLE=IMAGE/>
<LOGO HREF=pageTwoLogo.gif STYLE=ICON/>
</ITEM>
</CHANNEL>
```

## Atsauces

* [Kanāla definīcijas formāts — Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)


