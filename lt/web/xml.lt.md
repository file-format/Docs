{
  "date": "2019-10-11",
  "keywords": [
"xml",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Failo plėtinys",
"išplečiama žymėjimo kalba"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XML failo formatas",
  "description": "Sužinokite apie XML failo formatą ir API, kurios gali kurti ir atidaryti XML failus.",
  "linktitle": "XML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xm-ltl"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra XML failas?

XML stands for Extensible Markup Language that is similar to **[HTML](/web/html/)** but different in using tags for defining objects. The whole idea behind creation of XML file format was to store and transport data without being dependent on software or hardware tools. Its popularity is due to it being both human as well as machine readable. This enables it to create common data protocols in the form of objects to be stored and shared over network such as World Wide Web (WWW). The "X" in XML is for extensible which implies that the language can be extended to any number of symbols as per user requirements. It is for these features that many standard file formats make use of it such as Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/web/xhtml/)** and **[SVG](/page-description-language/svg/)**.

## XML failo formatas

XML failo formatas yra pagrįstas XML dokumento objekto modeliu (DOM), kuris yra HTML ir XML dokumentų programavimo API. XML DOM apibrėžia standartinį metodą pasiekti ir valdyti XML dokumento elementus. Tai sukuria XML dokumento medžio struktūros vaizdą, kurį galima naudoti norint pasiekti visus elementus per DOM medį. Esamus elementus galima modifikuoti / ištrinti, taip pat galima sukurti naujus elementus XML medyje. Kiekvienas XML dokumento elementas vadinamas mazgu. XML DOM yra toks, kaip parodyta kitame paveikslėlyje.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### Universalus XML metodas

Dėl XML galios ji tampa universalia duomenų perdavimo tinkle kalba, nes supaprastinamas duomenų perdavimas ir platformos pakeitimai. Tai taip pat užtikrina galimybę keistis duomenimis tarp nesuderinamų sistemų, nes duomenys saugomi paprasto teksto formatu. HTML skirtas duomenims pateikti žiniatinklyje, o XML – keitimuisi duomenimis. XML viduje naudojamos žymėjimo žymų poros apibrėžia pagrindinius struktūros elementus, kurie turi būti naudojami skaitant programas.

## XML pavyzdys

Toliau pateikiamas supaprastintas kompaktinių diskų katalogo pavyzdys, kuriame kiekviename įraše yra informacijos apie kompaktinius diskus, pvz., atlikėją, šalį, įmonę, kainą ir pagaminimo metus.

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

## Nuorodos

* [XML – Vikipedija](https://en.wikipedia.org/wiki/XML)


