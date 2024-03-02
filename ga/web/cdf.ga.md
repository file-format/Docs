{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CDF - Formáid Sainmhíniú Cainéal",
  "description": "Foghlaim faoi cad is comhad CDF agus APIs ann ar féidir comhaid CDF a chruthú agus a oscailt.",
  "linktitle": "CDF",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cd-gaf"
}
},
  "lastmod": "2021-08-18"
}

## Cad is comhad CDF ann?

Is éard atá i gcomhad le síneadh .cdf ná formáid comhaid dáileadh faisnéise bunaithe ar XLM a úsáideadh chun nuashonruithe minice a fhoilsiú mar chainéil”. Foilsítear an fhaisnéis ó aon fhreastalaí gréasáin agus seachadtar go huathoibríoch í chuig ríomhairí le cláir chomhoiriúnacha glactha ar nós brabhsálaithe gréasáin. Síníonn úsáideoirí le cainéil ghníomhacha agus tá nuashonruithe sceidealta seachadta chuig a ndeasc.
Úsáideadh comhaid CDF níos luaithe i gcomhar le teicneolaíochtaí Microsoft's Active Channel, Active Desktop agus Smart Offline Ceanán.

## Formáid Comhaid CDF

Déantar comhaid CDF a shábháil mar chomhaid XML atá ina bhformáid chomhaid gréasáin cineálach chun faisnéis a mhalartú. Is seanfhormáid í formáid comhaid CDF anois agus níor glacadh go forleathan léi riamh. I gcomparáid leis sin, bhí níos mó cáil ar RSS Netscape agus baineadh úsáid as go forleathan.

### Sampla Formáid Comhaid CDF

Seo a leanas sampla cineálach den fhormáid comhaid CDF.

```
<?xml version=1.0 encoding=UTF-8?>
<CHANNEL HREF=http://domain/folder/pageOne.extension
BASE=http://domain/folder/
LASTMOD=1998-11-05T22:12
PRECACHE=TÁ
LEIBHÉAL=0>
<TITLE>Teideal an Chainéal</TITLE>
<ABSTRACT>Achoimre ar ábhar an chainéil.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY=14/>
</SCHEDULE>
<LOGO HREF=wideChannelLogo.gif STYLE=IMAGE-WIDE/>
<LOGO HREF=imageChannelLogo.gif STYLE=IMAGE/>
<LOGO HREF=iconChannelLogo.gif STYLE=ICON/>
<ITEM HREF=pageTwo.extension
    LASTMOD=1998-11-05T22:12
    PRECACHE=TÁ
LEIBHÉAL=1>
<TITLE>Teideal Leathanach a Dó</TITLE>
<ABSTRACT>Achoimre ar ábhar Leathanach a Dó.</ABSTRACT>
<LOGO HREF=pageTwoLogo.gif STYLE=IMAGE/>
<LOGO HREF=pageTwoLogo.gif STYLE=ICON/>
</ITEM>
</CHANNEL>
```

## Tagairtí

* [Formáid sainmhínithe cainéil - Le Vicipéid](https://en.wikipedia.org/wiki/Channel_Definition_Format)


