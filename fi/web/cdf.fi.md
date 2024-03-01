{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CDF - Channel Definition Format",
  "description": "Opi CDF-tiedostoista ja sovellusliittymistä, jotka voivat luoda ja avata CDF-tiedostoja.",
  "linktitle": "CDF",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cd-fif"
}
},
  "lastmod": "2021-08-18"
}

## Mikä on CDF-tiedosto?

Tiedosto, jonka pääte on .cdf, on XLM-pohjainen tiedonjakelutiedostomuoto, jota käytettiin säännöllisten päivitysten julkaisemiseen kanavina. Tiedot julkaistaan miltä tahansa verkkopalvelimelta ja toimitetaan automaattisesti tietokoneille, joissa on yhteensopivia vastaanottoohjelmia, kuten verkkoselaimia. Käyttäjät tilaavat aktiivisia kanavia, ja heidän työpöydälleen toimitetaan ajoitetut päivitykset.
CDF-tiedostoja käytettiin aiemmin yhdessä Microsoftin Active Channel-, Active Desktop- ja Smart Offline Favorites -tekniikoiden kanssa.

## CDF-tiedostomuoto

CDF-tiedostot tallennetaan XML-tiedostoina, jotka ovat yleinen verkkotiedostomuoto tiedonvaihtoon. CDF-tiedostomuoto on nyt vanha muoto, eikä sitä koskaan otettu laajalti käyttöön. Tähän verrattuna Netscapen RSS oli tunnetumpi ja laajemmin käytetty.

### Esimerkki CDF-tiedostomuodosta

Seuraava on yleinen esimerkki CDF-tiedostomuodosta.

```
<?xml version=1.0 encoding=UTF-8?>
<CHANNEL HREF=http://domain/folder/pageOne.extension
BASE=http://domain/folder/
LASTMOD=1998-11-05T22:12
PRECACHE=KYLLÄ
LEVEL=0>
<TITLE>Kanavan otsikko</TITLE>
<ABSTRACT>Yhteenveto kanavan sisällöstä.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY=14/>
</SCHEDULE>
<LOGO HREF=wideChannelLogo.gif STYLE=IMAGE-WIDE/>
<LOGO HREF=imageChannelLogo.gif STYLE=IMAGE/>
<LOGO HREF=iconChannelLogo.gif STYLE=ICON/>
<ITEM HREF=pageTwo.extension
    LASTMOD=1998-11-05T22:12
    PRECACHE=KYLLÄ
LEVEL=1>
<TITLE>Toisen sivun otsikko</TITLE>
<ABSTRACT>Tiivistelmä toisen sivun sisällöstä.</ABSTRACT>
<LOGO HREF=pageTwoLogo.gif STYLE=IMAGE/>
<LOGO HREF=pageTwoLogo.gif STYLE=ICON/>
</ITEM>
</CHANNEL>
```

## Viitteet

* [Channel Definition Format - Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)


