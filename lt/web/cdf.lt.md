{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CDF – kanalo apibrėžimo formatas",
  "description": "Sužinokite, kas yra CDF failas ir API, kurios gali kurti ir atidaryti CDF failus.",
  "linktitle": "CDF",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cd-ltf"
}
},
  "lastmod": "2021-08-18"
}

## Kas yra CDF failas?

Failas su .cdf plėtiniu yra XLM pagrindu sukurtas informacijos platinimo failo formatas, kuris buvo naudojamas dažnai naujinimams skelbti kaip kanalus. Informacija skelbiama iš bet kurio žiniatinklio serverio ir automatiškai pristatoma į kompiuterius su suderinamomis priėmimo programomis, pvz., žiniatinklio naršyklėmis. Vartotojai prenumeruoja aktyvius kanalus ir suplanuoti naujiniai pristatomi į jų darbalaukį.
CDF failai anksčiau buvo naudojami kartu su Microsoft Active Channel, Active Desktop ir Smart Offline Favorites technologijomis.

## CDF failo formatas

CDF failai išsaugomi kaip XML failai, kurie yra bendras žiniatinklio failo formatas, skirtas keistis informacija. CDF failo formatas dabar yra senas ir niekada nebuvo plačiai naudojamas. Palyginti su tuo, Netscape RSS buvo garsesnis ir plačiau naudojamas.

### CDF failo formato pavyzdys

Toliau pateikiamas bendras CDF failo formato pavyzdys.

```
<?xml version=1.0 encoding=UTF-8?>
<CHANNEL HREF=http://domain/folder/pageOne.extension
BASE=http://domenas/aplankas/
LASTMOD=1998-11-05T22:12
PRECACHE=TAIP
LEVEL=0>
<TITLE>Kanalo pavadinimas</TITLE>
<ABSTRACT>Kanalo turinio santrauka.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY=14/>
</SCHEDULE>
<LOGO HREF=wideChannelLogo.gif STYLE=IMAGE-WIDE/>
<LOGO HREF=imageChannelLogo.gif STYLE=IMAGE/>
<LOGO HREF=iconChannelLogo.gif STYLE=ICON/>
<ITEM HREF=pageTwo.extension
    LASTMOD=1998-11-05T22:12
    PRECACHE=TAIP
LEVEL=1>
<TITLE>Antrojo puslapio pavadinimas</TITLE>
<ABSTRACT>Antrojo puslapio turinio santrauka.</ABSTRACT>
<LOGO HREF=pageTwoLogo.gif STYLE=IMAGE/>
<LOGO HREF=pageTwoLogo.gif STYLE=ICON/>
</ITEM>
</CHANNEL>
```

## Nuorodos

* [Kanalo apibrėžimo formatas – pagal Vikipediją](https://en.wikipedia.org/wiki/Channel_Definition_Format)


