{
  "date": "2019-10-11",
  "keywords": [
"xml",
"Fails",
"Pagarinājums",
"Faila formāts",
"Faila paplašinājums",
"paplašināma iezīmēšanas valoda"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XML faila formāts",
  "description": "Uzziniet par XML failu formātu un API, kas var izveidot un atvērt XML failus.",
  "linktitle": "XML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xm-lvl"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir XML fails?

XML stands for Extensible Markup Language that is similar to **[HTML](/web/html/)** but different in using tags for defining objects. The whole idea behind creation of XML file format was to store and transport data without being dependent on software or hardware tools. Its popularity is due to it being both human as well as machine readable. This enables it to create common data protocols in the form of objects to be stored and shared over network such as World Wide Web (WWW). The "X" in XML is for extensible which implies that the language can be extended to any number of symbols as per user requirements. It is for these features that many standard file formats make use of it such as Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/web/xhtml/)** and **[SVG](/page-description-language/svg/)**.

## XML faila formāts

XML faila formāts ir balstīts uz XML dokumenta objektu modeli (DOM), kas ir programmēšanas API HTML un XML dokumentiem. XML DOM definē standarta metodi, lai piekļūtu XML dokumenta elementiem un apstrādātu tos. Tas veido XML dokumenta koka struktūras skatu, ko var izmantot, lai piekļūtu visiem elementiem, izmantojot DOM koku. Esošos elementus var modificēt/dzēst, kā arī izveidot jaunus elementus XML kokā. Katrs XML dokumenta elements tiek saukts par mezglu. XML DOM ir tāds, kā parādīts nākamajā attēlā.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### Universāla XML pieeja

XML jauda padara to par universālu valodu datu saziņai tīklā, vienkāršojot datu transportēšanu un platformas izmaiņas. Tas arī nodrošina datu apmaiņu starp nesaderīgām sistēmām, saglabājot datus vienkārša teksta formātā. HTML ir paredzēts datu attēlošanai tīmeklī, savukārt XML ir datu apmaiņai. XML iekšpusē izmantotie iezīmēšanas tagu pāri nosaka galvenos struktūras elementus, kas jāizmanto lasīšanas lietojumprogrammām.

## XML piemērs

Tālāk ir sniegts vienkāršots kompaktdisku kataloga piemērs, kurā katrs ieraksts satur informāciju par kompaktdiskiem, piemēram, izpildītāju, valsti, uzņēmumu, cenu un izlaiduma gadu.

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

## Atsauces

* [XML — Wikipedia](https://en.wikipedia.org/wiki/XML)


