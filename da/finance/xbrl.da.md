{
  "date" : "2019-10-11",
  "keywords" : [ "xbrl","xbrl file", "xbrl file format", "xbrl file type", "file", "type", "what is an xbrl file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XBRL - Business and Financial Reporting File Format",
  "description":"Lær om XBRL-filformat og API'er, der kan oprette og åbne XBRL-filer.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl-da",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Hvad er en XBRL fil?

En fil med udvidelsen .xbrl (eXtensible Business Reporting Language) er en frit tilgængelig og global ramme til udveksling af virksomhedsoplysninger. Det er nu meget udbredt som et af de standardformater, der har erstattet de ældre papirbaserede rapporter med mere nyttige og nøjagtige digitale optegnelser. Data, der udveksles ved hjælp af XBRL-filerne, omfatter hovedbøger, finansielle detaljer og balancer. Det understøtter datatags, der tillader databehandling fra forberedelse til analysestadiet af forretningsinformation af enhver art. XBRL-filer kan åbnes ved hjælp af software såsom Rivet Software Dragon View XBRL Viewer og API'er som [Aspose.Finance](https://products.aspose.com/finance/).

## XBRL filformat

XBRL er en åben international standard for digital virksomhedsrapportering, der er meget udbredt globalt. Det er et [XML](/web/xml/)-baseret sprog, der bruger XBRL-elementer, kendt som tags, til at beskrive hvert element af forretningsdata for at formulere data til rapportsortering og analyse. XBRL-filformatspecifikationer er udviklet og udgivet af XBRL International, Inc., hvor [XBRL version 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) i øjeblikket er tilgængelig for brugere.

### XBRL-dokumentstruktur

Fuldstændig information om [XBRL 2.1 tags](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) kan henvises af programmører til at skrive applikationer til at arbejde med dette filformat. En XBRL består af en XBRL-instans og en samling taksonomier.

**`XBRL Instance`** - XBRL-instansen begynder med<xbrl> rodelement. Et stort XML-dokument kan indeholde mere end én XBRL-instans indlejret i det.

**`XBRL-taksonomi`** - [XBRL Taxonomy](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) er defineret som et XML-skemastrukturer og et sæt af direkte refererede eksterne linkselementer. Et skalerbart taksonomiskema, der viser linkbasereferencerne, er som følger.

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


## Referencer ##

* [XBRL - Af Wikipedia](https://en.wikipedia.org/wiki/XBRL)

* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- errata-2013-02-20.html)


