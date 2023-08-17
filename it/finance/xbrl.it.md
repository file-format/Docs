{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl","file xbrl", "formato file xbrl", "tipo di file xbrl", "file", "tipo", "cos'è un file xbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - Formato file di rendicontazione aziendale e finanziaria",
  "description":"Scopri il formato di file XBRL e le API che possono creare e aprire file XBRL.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Che cos'è un file XBRL?

Un file con estensione .xbrl (eXtensible Business Reporting Language) è un framework globale e disponibile gratuitamente per lo scambio di informazioni aziendali. Ora è ampiamente utilizzato come uno dei formati standard che ha sostituito i vecchi rapporti cartacei con record digitali più utili e precisi. I dati scambiati utilizzando i file XBRL includono libri mastri, dettagli finanziari e bilanci. Supporta tag di dati che consentono l'elaborazione dei dati dalla fase di preparazione fino alla fase di analisi di informazioni aziendali di ogni tipo. I file XBRL possono essere aperti utilizzando software come Rivet Software Dragon View XBRL Viewer e API come [Aspose.Finance](https://products.aspose.com/finance/).

## Formato file XBRL

XBRL è uno standard internazionale aperto per il reporting aziendale digitale ampiamente utilizzato a livello globale. È un linguaggio basato su [XML](/it/web/xml/) che utilizza elementi XBRL, noti come tag, per descrivere ogni elemento dei dati aziendali per formulare dati per l'ordinamento e l'analisi dei report. Le specifiche del formato file XBRL sono sviluppate e pubblicate da XBRL International, Inc, con [XBRL versione 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) attualmente a disposizione degli utenti.

### Struttura del documento XBRL

Informazioni complete sui [tag XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) possono essere indirizzati dai programmatori per scrivere applicazioni per lavorare su questo formato di file. Un XBRL è costituito da un'istanza XBRL e da una raccolta di tassonomie.

**`Istanza XBRL`** - L'istanza XBRL inizia con il<xbrl> elemento radice. Un documento XML di grandi dimensioni può contenere più di un'istanza XBRL incorporata.

**`Tassonomia XBRL`** - La [Tassonomia XBRL](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) è definito come una struttura di schema XML e un insieme di elementi di collegamenti esterni referenziati direttamente. Uno schema di tassonomia scalabile che mostra i riferimenti di linkbase è il seguente.

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


## Riferimenti ##

* [XBRL - Di Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html)

