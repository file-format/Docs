{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl","xbrl-fil", "xbrl-filformat", "xbrl-filtyp", "fil", "typ", "vad är en xbrl-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - Filformat för affärs- och finansiell rapportering",
  "description":"Läs mer om XBRL-filformat och API:er som kan skapa och öppna XBRL-filer.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Vad är en XBRL fil?

En fil med tillägget .xbrl (eXtensible Business Reporting Language) är ett fritt tillgängligt och globalt ramverk för utbyte av affärsinformation. Det används nu i stor utsträckning som ett av standardformaten som har ersatt de äldre pappersbaserade rapporterna med mer användbara och korrekta digitala register. Data som utbyts med XBRL-filer inkluderar reskontra, finansiella detaljer och balansräkningar. Den stöder datataggar som tillåter databearbetning från förberedelse till analysstadiet av affärsinformation av alla slag. XBRL-filer kan öppnas med programvara som Rivet Software Dragon View XBRL Viewer och API:er som [Aspose.Finance](https://products.aspose.com/finance).

## XBRL filformat

XBRL är en öppen internationell standard för digital affärsrapportering som används flitigt globalt. Det är ett [XML](/sv/web/xml/)-baserat språk som använder XBRL-element, så kallade taggar, för att beskriva varje del av affärsdata för att formulera data för rapportsortering och analys. XBRL-filformatsspecifikationer utvecklas och publiceras av XBRL International, Inc, med [XBRL version 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) för närvarande tillgängliga för användarna.

### XBRL-dokumentstruktur

Komplett information om [XBRL 2.1-taggarna](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html) kan hänvisas av programmerare för att skriva applikationer för att arbeta med detta filformat. En XBRL består av en XBRL-instans och en samling taxonomier.

**`XBRL Instance`** - XBRL-instansen börjar med<xbrl> rotelement. Ett stort XML-dokument kan innehålla mer än en XBRL-instans inbäddad i det.

**`XBRL Taxonomy`** - [XBRL Taxonomy](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +corrected-errata-2013-02-20.html#_5) definieras som ett XML-schemastrukturer och en uppsättning av direkt refererade externa länkelement. Ett skalbart taxonomischema som visar länkbasreferenserna är som följer.

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


## Referenser ##

* [XBRL - av Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- errata-2013-02-20.html)

