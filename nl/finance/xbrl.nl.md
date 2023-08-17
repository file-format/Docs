{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl","xbrl-bestand", "xbrl-bestandsformaat", "xbrl-bestandstype", "bestand", "type", "wat is een xbrl-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - Bestandsformaat voor zakelijke en financiële rapportage",
  "description":"Meer informatie over XBRL-bestandsindeling en API's die XBRL-bestanden kunnen maken en openen.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Wat is een XBRL-bestand?

Een bestand met de extensie .xbrl (eXtensible Business Reporting Language) is een vrij beschikbaar en wereldwijd raamwerk voor het uitwisselen van bedrijfsinformatie. Het wordt nu veel gebruikt als een van de standaardindelingen die de oudere papieren rapporten heeft vervangen door nuttigere en nauwkeurigere digitale documenten. Gegevens die worden uitgewisseld met behulp van de XBRL-bestanden omvatten grootboeken, financiële gegevens en balansen. Het ondersteunt datatags die gegevensverwerking mogelijk maken van de voorbereiding tot de analysefase van allerlei soorten bedrijfsinformatie. XBRL-bestanden kunnen worden geopend met software zoals Rivet Software Dragon View XBRL Viewer en API's zoals [Aspose.Finance](https://products.aspose.com/finance/).

## XBRL-bestandsindeling

XBRL is een open internationale standaard voor digitale bedrijfsrapportage die wereldwijd veel wordt gebruikt. Het is een op [XML](/nl/web/xml/) gebaseerde taal die XBRL-elementen, ook wel tags genoemd, gebruikt om elk item van bedrijfsgegevens te beschrijven om gegevens te formuleren voor het sorteren en analyseren van rapporten. Specificaties voor XBRL-bestandsindelingen zijn ontwikkeld en gepubliceerd door XBRL International, Inc, met [XBRL versie 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) momenteel beschikbaar voor gebruikers.

### XBRL-documentstructuur

Volledige informatie over de [XBRL 2.1-tags](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) kan worden doorverwezen door programmeurs om toepassingen te schrijven voor het werken met dit bestandsformaat. Een XBRL bestaat uit een XBRL-instantie en een verzameling taxonomieën.

**`XBRL-instantie`** - De XBRL-instantie begint met de<xbrl> wortelelement. Een groot XML-document kan meer dan één ingesloten XBRL-instantie bevatten.

**`XBRL-taxonomie`** - De [XBRL-taxonomie](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) wordt gedefinieerd als een XML-schemastructuren en een set van direct verwezen externe links-elementen. Een schaalbaar taxonomieschema met de linkbase-referenties is als volgt.

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


## Referenties ##

* [XBRL - Door Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html)

