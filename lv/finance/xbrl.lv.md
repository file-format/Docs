{
  "date" : "2019-10-11",
  "keywords" : [ "xbrl","xbrl file", "xbrl file format", "xbrl file type", "file", "type", "what is an xbrl file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XBRL — biznesa un finanšu pārskatu faila formāts",
  "description":"Uzziniet par XBRL faila formātu un API, kas var izveidot un atvērt XBRL failus.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl-lv",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Kas ir XBRL fails?

Fails ar paplašinājumu .xbrl (eXtensible Business Reporting Language) ir brīvi pieejama un globāla biznesa informācijas apmaiņas sistēma. Tagad tas tiek plaši izmantots kā viens no standarta formātiem, kas ir aizstājis vecākos papīra pārskatus ar noderīgākiem un precīzākiem digitālajiem ierakstiem. Dati, ar kuriem tiek apmainīti, izmantojot XBRL failus, ietver virsgrāmatas, finanšu informāciju un bilances. Tā atbalsta datu tagus, kas ļauj apstrādāt datus no visu veidu biznesa informācijas sagatavošanas līdz analīzes stadijai. XBRL failus var atvērt, izmantojot programmatūru, piemēram, Rivet Software Dragon View XBRL Viewer un API, piemēram, [Aspose.Finance](https://products.aspose.com/finance/).

## XBRL faila formāts

XBRL ir atvērts starptautisks digitālās uzņēmējdarbības pārskatu standarts, kas tiek plaši izmantots visā pasaulē. Tā ir uz [XML](/web/xml/) balstīta valoda, kas izmanto XBRL elementus, kas pazīstami kā tagi, lai aprakstītu katru uzņēmējdarbības datu vienumu, lai formulētu datus pārskatu kārtošanai un analīzei. XBRL faila formāta specifikācijas izstrādā un publicē XBRL International, Inc, un pašlaik lietotājiem ir pieejams [XBRL version 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html).

### XBRL dokumenta struktūra

Programmētāji var iegūt pilnīgu informāciju par [XBRL 2.1 tags](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html), lai rakstītu lietojumprogrammas darbam šajā faila formātā. XBRL sastāv no XBRL instances un taksonomiju kolekcijas.

**`XBRL instance`** — XBRL instance sākas ar<xbrl> saknes elements. Liels XML dokuments var saturēt vairāk nekā vienu XBRL gadījumu, kas tajā ir iegults.

**`XBRL taksonomija`** — [XBRL Taxonomy](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) ir definēta kā XML shēmas struktūras un tieši norādītu ārējo saišu elementu kopa. Mērogojama taksonomijas shēma, kas parāda saites bāzes atsauces, ir šāda.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## Atsauces Nr.

* [XBRL — Wikipedia](https://en.wikipedia.org/wiki/XBRL)

* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- errata-2013-02-20.html)


