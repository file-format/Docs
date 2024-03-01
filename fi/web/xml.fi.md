{
  "date": "2019-10-11",
  "keywords": [
"xml",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Tiedostopääte",
"laajennettava merkintäkieli"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XML-tiedostomuoto",
  "description": "Opi XML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata XML-tiedostoja.",
  "linktitle": "XML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xm-fil"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on XML-tiedosto?

XML stands for Extensible Markup Language that is similar to **[HTML](/web/html/)** but different in using tags for defining objects. The whole idea behind creation of XML file format was to store and transport data without being dependent on software or hardware tools. Its popularity is due to it being both human as well as machine readable. This enables it to create common data protocols in the form of objects to be stored and shared over network such as World Wide Web (WWW). The "X" in XML is for extensible which implies that the language can be extended to any number of symbols as per user requirements. It is for these features that many standard file formats make use of it such as Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/web/xhtml/)** and **[SVG](/page-description-language/svg/)**.

## XML-tiedostomuoto

XML-tiedostomuoto perustuu XML Document Object Model (DOM) -malliin, joka on HTML- ja XML-dokumenttien ohjelmointisovellusliittymä. XML-DOM määrittelee vakiomenetelmän XML-asiakirjan elementtien käyttämiseen ja käsittelemiseen. Se tekee XML-dokumentista puurakennenäkymän, jonka avulla voidaan käyttää kaikkia elementtejä DOM-puun kautta. Olemassa olevia elementtejä voidaan muokata/poistaa sekä uusia elementtejä voidaan luoda XML-puuhun. Jokaista XML-dokumentin elementtiä kutsutaan solmuksi. XML DOM on seuraavan kuvan mukainen.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### XML:n yleinen lähestymistapa

XML:n teho tekee siitä universaalin kielen tiedonsiirtoon verkossa yksinkertaistamalla tiedonsiirtoa ja alustamuutoksia. Tämä varmistaa myös tietojen vaihdon yhteensopimattomien järjestelmien välillä tallentamalla tiedot tekstimuodossa. HTML on tiedon esittämiseen verkossa, kun taas XML on tiedonvaihtoon. XML:n sisällä käytetyt merkintätagiparit määrittelevät rakenteen keskeiset elementit, joita lukusovellukset hyödyntävät.

## XML-esimerkki

Seuraavassa on yksinkertaistettu esimerkki CD-luettelosta, jossa jokainen levy sisältää tietoja CD-levyistä, kuten esittäjä, maa, yritys, hinta ja valmistusvuosi.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Viitteet

* [XML - Wikipedia](https://en.wikipedia.org/wiki/XML)


