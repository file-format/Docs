{
  "date": "2019-10-11",
  "keywords": [
"xml",
"Fil",
"Udvidelse",
"Filformat",
"Filudvidelse",
"udvideligt opmærkningssprog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XML filformat",
  "description": "Lær om XML-filformat og API'er, der kan oprette og åbne XML-filer.",
  "linktitle": "XML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xm-dal"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en XML-fil?

XML stands for Extensible Markup Language that is similar to **[HTML](/web/html/)** but different in using tags for defining objects. The whole idea behind creation of XML file format was to store and transport data without being dependent on software or hardware tools. Its popularity is due to it being both human as well as machine readable. This enables it to create common data protocols in the form of objects to be stored and shared over network such as World Wide Web (WWW). The "X" in XML is for extensible which implies that the language can be extended to any number of symbols as per user requirements. It is for these features that many standard file formats make use of it such as Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/web/xhtml/)** and **[SVG](/page-description-language/svg/)**.

## XML filformat

XML-filformatet er baseret på XML Document Object Model (DOM), der er en programmerings-API til HTML- og XML-dokumenter. XML DOM definerer en standardmetode til at få adgang til og manipulere XML-dokumentelementerne. Det laver en træstrukturvisning af et XML-dokument, der kan bruges til at få adgang til alle elementer gennem DOM-træet. Eksisterende elementer kan ændres/slettes, ligesom der kan oprettes nye elementer i XML-træet. Hvert element i et XML-dokument kaldes en node. XML DOM er som vist i det følgende billede.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### Universal tilgang til XML

Kraften ved XML gør det til et universelt sprog til datakommunikation over netværket ved at gøre datatransport og platformsændringer forenklet. Dette sikrer også, at udveksling af data mellem inkompatible systemer er mulig ved at gemme data i almindeligt tekstformat. HTML er til datarepræsentation over nettet, hvorimod XML er til udveksling af data. Markup-tag-parrene, der bruges i XML, definerer nøgleelementerne i strukturen, der skal bruges til at læse applikationer.

## XML eksempel

Det følgende er et forenklet eksempel på et cd-katalog, hvor hver plade indeholder oplysninger om cd'er såsom kunstner, land, firma, pris og produktionsår.

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

## Referencer

* [XML - af Wikipedia](https://en.wikipedia.org/wiki/XML)


