{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Format de definire a canalului",
  "description" :"Aflați despre ce este un fișier CDF și API-urile care pot crea și deschide fișiere CDF.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## Ce este un fișier CDF?

Un fișier cu extensia .cdf este un format de fișier de distribuție a informațiilor bazat pe XLM care a fost folosit pentru a publica actualizări frecvente ca „canale”. Informațiile sunt publicate de pe orice server web și sunt livrate automat computerelor cu programe de recepție compatibile, cum ar fi browsere web. Utilizatorii se abonează la canalele active și au actualizări programate livrate pe desktop.
Fișierele CDF au fost utilizate anterior împreună cu tehnologiile Microsoft Active Channel, Active Desktop și Smart Offline Favorites.

## Format de fișier CDF

Fișierele CDF sunt salvate ca fișiere XML, care este un format de fișier web generic pentru schimbul de informații. Formatul de fișier CDF este un format vechi acum și nu a fost niciodată adoptat pe scară largă. În comparație cu acesta, RSS-ul Netscape a fost mai faimos și utilizat pe scară largă.

### Exemplu de format de fișier CDF

Următorul este un exemplu generic al formatului de fișier CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://domeniu/dosar/"
LASTMOD="1998-11-05T22:12"
PRECACHE="DA"
LEVEL="0">
<TITLE>Titlul canalului</TITLE>
<ABSTRACT>Rezumat al conținutului canalului.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="DA"
LEVEL="1">
<TITLE>Titlul paginii a doua</TITLE>
<ABSTRACT>Rezumat al conținutului paginii a doua.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Referințe

* [Format de definiție a canalului - După Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)

