{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Formato di definizione del canale",
  "description" :"Scopri cos'è un file CDF e le API che possono creare e aprire file CDF.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## Che cos'è un file CDF?

Un file con estensione .cdf è un formato di file di distribuzione delle informazioni basato su XLM utilizzato per pubblicare aggiornamenti frequenti come "canali". Le informazioni vengono pubblicate da qualsiasi server web e vengono inviate automaticamente a computer con programmi di ricezione compatibili come browser web. Gli utenti si iscrivono ai canali attivi e ricevono aggiornamenti programmati sul proprio desktop.
I file CDF sono stati precedentemente utilizzati insieme alle tecnologie Active Channel, Active Desktop e Smart Offline Favorites di Microsoft.

## Formato file CDF

I file CDF vengono salvati come file XML che è un formato di file Web generico per lo scambio di informazioni. Il formato di file CDF è un vecchio formato ora e non è mai stato ampiamente adottato. In confronto a questo, l'RSS di Netscape era più famoso e ampiamente utilizzato.

### Esempio di formato file CDF

Quello che segue è un esempio generico del formato di file CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://dominio/cartella/"
LASTMOD="1998-11-05T22:12"
PRECACHE="SI"
LIVELLO="0">
<TITLE>Titolo del canale</TITLE>
<ABSTRACT>Sinossi dei contenuti del canale.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="SI"
LIVELLO="1">
<TITLE>Titolo della pagina due</TITLE>
<ABSTRACT>Sinossi dei contenuti di Pagina Due.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Riferimenti

* [Formato di definizione del canale - Di Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)

