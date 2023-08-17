{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl", "soubor xbrl", "formát souboru xbrl", "typ souboru xbrl", "soubor", "typ", "co je soubor xbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - Formát souboru obchodního a finančního výkaznictví",
  "description":"Další informace o formátu souboru XBRL a rozhraních API, která mohou vytvářet a otevírat soubory XBRL.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Co je soubor XBRL?

Soubor s příponou .xbrl (eXtensible Business Reporting Language) je volně dostupný a globální rámec pro výměnu obchodních informací. Nyní je široce používán jako jeden ze standardních formátů, který nahradil starší papírové zprávy užitečnějšími a přesnějšími digitálními záznamy. Data vyměňovaná pomocí souborů XBRL zahrnují účetní knihy, finanční podrobnosti a rozvahy. Podporuje datové značky, které umožňují zpracování dat od přípravy až po fázi analýzy obchodních informací všeho druhu. Soubory XBRL lze otevřít pomocí softwaru, jako je Rivet Software Dragon View XBRL Viewer, a rozhraní API jako [Aspose.Finance](https://products.aspose.com/finance/).

## Formát souboru XBRL

XBRL je otevřený mezinárodní standard pro digitální obchodní výkaznictví, který je široce používán po celém světě. Je to jazyk založený na [XML](/cs/web/xml/), který používá prvky XBRL, známé jako značky, k popisu každé položky obchodních dat za účelem formulování dat pro třídění a analýzu sestav. Specifikace formátu souboru XBRL jsou vyvinuty a publikovány společností XBRL International, Inc, v současné době [XBRL verze 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) k dispozici uživatelům.

### Struktura dokumentu XBRL

Kompletní informace o [značkách XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) mohou programátoři odkázat na psaní aplikací pro práci s tímto formátem souborů. XBRL se skládá z instance XBRL a kolekce taxonomií.

**`Instance XBRL`** – Instance XBRL začíná znakem<xbrl> kořenový prvek. Velký dokument XML může obsahovat více než jednu instanci XBRL.

**`XBRL Taxonomy`** – The [XBRL Taxonomy](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) je definován jako struktura XML schématu a sada přímo odkazovaných prvků externích odkazů. Škálovatelné schéma taxonomie zobrazující odkazy na báze odkazů je následující.

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


## Reference ##

* [XBRL – podle Wikipedie](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html)

