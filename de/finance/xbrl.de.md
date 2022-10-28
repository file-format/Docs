{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl","xbrl-Datei", "xbrl-Dateiformat", "xbrl-Dateityp", "Datei", "Typ", "was ist eine xbrl-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - Dateiformat für Geschäfts- und Finanzberichte",
  "description":"Erfahren Sie mehr über das XBRL-Dateiformat und APIs, die XBRL-Dateien erstellen und öffnen können.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
"identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Was ist eine XBRL-Datei?

Eine Datei mit der Erweiterung .xbrl (eXtensible Business Reporting Language) ist ein frei verfügbarer und globaler Rahmen für den Austausch von Geschäftsinformationen. Es ist heute weit verbreitet als eines der Standardformate, das die älteren papierbasierten Berichte durch nützlichere und genauere digitale Aufzeichnungen ersetzt hat. Zu den über die XBRL-Dateien ausgetauschten Daten gehören Hauptbücher, Finanzdetails und Bilanzen. Es unterstützt Daten-Tags, die eine Datenverarbeitung von der Vorbereitung bis zur Analyse von Geschäftsinformationen aller Art ermöglichen. XBRL-Dateien können mit Software wie Rivet Software Dragon View XBRL Viewer und APIs wie [Aspose.Finance](https://products.aspose.com/finance) geöffnet werden.

## XBRL-Dateiformat

XBRL ist ein offener internationaler Standard für die digitale Geschäftsberichterstattung, der weltweit weit verbreitet ist. Es handelt sich um eine auf [XML](/de/web/xml/) basierende Sprache, die XBRL-Elemente, bekannt als Tags, verwendet, um jedes Geschäftsdatenelement zu beschreiben und Daten für die Sortierung und Analyse von Berichten zu formulieren. XBRL-Dateiformatspezifikationen werden von XBRL International, Inc entwickelt und veröffentlicht, derzeit mit [XBRL-Version 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html). Benutzern zur Verfügung.

### XBRL-Dokumentstruktur

Vollständige Informationen zu den [XBRL 2.1-Tags] (https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html) können von Programmierern zum Schreiben von Anwendungen zum Arbeiten mit diesem Dateiformat herangezogen werden. Ein XBRL besteht aus einer XBRL-Instanz und einer Sammlung von Taxonomien.

**`XBRL-Instanz`** – Die XBRL-Instanz beginnt mit dem<xbrl> Wurzelelement. Ein großes XML-Dokument kann mehr als eine darin eingebettete XBRL-Instanz enthalten.

**`XBRL-Taxonomie`** - Die [XBRL-Taxonomie](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +corrected-errata-2013-02-20.html#_5) ist als XML-Schemastruktur und Satz von direkt referenzierten externen Links-Elementen definiert. Ein skalierbares Taxonomieschema, das die Linkbase-Referenzen zeigt, sieht wie folgt aus.

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


## Verweise ##

* [XBRL – Von Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+korrigiert- errata-2013-02-20.html)

