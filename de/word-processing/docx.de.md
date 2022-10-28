{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX","Datei", "Format", "Dateityp", "Erweiterung","Was ist eine DOCX-Datei?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"Erfahren Sie mehr über das DOCX-Dateiformat und APIs, die DOCX-Dateien erstellen und öffnen können.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Was ist eine DOCX-Datei? ##

DOCX ist ein bekanntes Format für Microsoft Word-Dokumente. Die Struktur dieses neuen Dokumentformats, das 2007 mit der Veröffentlichung von Microsoft Office 2007 eingeführt wurde, wurde von einer reinen Binärdatei in eine Kombination aus XML- und Binärdateien geändert. Docx-Dateien können mit Word 2007 und späteren Versionen geöffnet werden, jedoch nicht mit früheren Versionen von MS Word, die DOC-Dateierweiterungen unterstützen.

## Kurze Geschichte ##

Nachdem Microsoft die Spezifikationen für das DOC-Dateiformat geöffnet hatte, war es für seine Konkurrenten einfach, das Format zurückzuentwickeln und die gleiche Unterstützung in ihren eigenen Anwendungen bereitzustellen. Darüber hinaus zwang die Konkurrenz von Open Office in Form seines Open Document Format Microsoft dazu, offenere und breitere Standards einzuführen. Anfang des Jahres 2000 beschloss Microsoft, die Änderung vorzunehmen, um den Standard für **Office Open XML** aufzunehmen. Dokumente unter diesem neuen Standard erhielten die Erweiterung [.docx](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), das „X“ für XML sein. 2007 wurde dieses neue Dateiformat Teil von Office 2007 und wird auch in den neuen Versionen von Microsoft Office weitergeführt. Der neue Dateityp hat zusätzliche Vorteile wie kleine Dateigrößen, weniger Änderungen durch Beschädigung und gut formatierte Bilddarstellung.

## DOCX-Dateiformatspezifikationen – Weitere Informationen

Eine Docx-Datei besteht aus einer Sammlung von XML-Dateien, die in einem ZIP-Archiv enthalten sind. Der Inhalt eines neuen Word-Dokuments kann angezeigt werden, indem dessen Inhalt entpackt wird. Die Sammlung enthält eine Liste von XML-Dateien, die wie folgt kategorisiert sind:

* MetaData-Dateien - enthält Informationen über andere im Archiv verfügbare Dateien
* Dokument - enthält den eigentlichen Inhalt des Dokuments

### Metadatendateien ###

Microsoft Word verwendet diese Dateien, um die Beziehung zwischen Dateien zu finden und den Inhalt des Dokuments zu finden. Wenn ein Word-Dokumentarchiv extrahiert wird, enthält es eine Reihe solcher Dateien, wie unten beschrieben.

#### Beziehungen - \_rels/.rels ####

Diese Datei enthält Informationen, die MS Word mitteilen, wo nach Dokumentinhalten und anderen Referenzen gesucht werden soll. Jede Beziehung wird durch eine eindeutige Beziehungs-ID identifiziert und gibt die referenzierte XML-Datei als Ziel an. Eine beispielhafte Beziehungsdatei wird wie folgt angezeigt:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Inhaltstypen ####

Ein Dokument kann mehrere Medientypen wie Bilder, Themen, Wortkunst usw. enthalten. Die XML-Datei [Content_Types].xml enthält Informationen über solche Medientypen, die im Dokument vorhanden sind. Der Inhalt einer solchen XML-Datei wird wie folgt angezeigt:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Verweise auf Ressourcen - \_rels/document.xml.rels ####

In dieser XML-Datei werden Informationen zu Ressourcen, wie beispielsweise in das Dokument eingebettete Bilder, referenziert.

#### Inhalt des Hauptdokuments ####

Dies bezieht sich auf die Haupt-XML-Datei des Archivs, die den Textinhalt des Dokuments enthält. Dieser Inhalt wird gemäß den OpenOffice-XML-Spezifikationen durch verschiedene Knoten dargestellt. Der Inhalt dieser Datei besteht hauptsächlich aus Absätzen und Tabellen, obwohl es sich auch um andere Knoten handeln kann.

### Dateiformatknoten ###

Die Hauptdatei document.xml ist eine Sammlung von Knoten zur Darstellung des Gesamtinhalts einer Datei. Jeder Knoten hat einen Anfang und ein Ende, die entweder weitere Knoten oder den Inhalt kapseln. Ein vereinfachtes Beispiel für eine solche XML-Datei sieht wie folgt aus:

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

Nachfolgend finden Sie Informationen zu einigen Knoten, die in einer DOCX-Datei zur Darstellung von Inhalten enthalten sind.

`<w:document> ` - Repräsentiert das Stammelement des Hauptinhalts der Datei.

`<w:body> ` - Stellt den Hauptteil des Dokuments dar, der aus vielen anderen Elementknoten wie Absätzen, Tabellen und Abschnitten bestehen kann.

#### Absätze ####

Ein Absatz ist der Hauptinhaltshalter innerhalb eines Dokuments. Es wird dargestellt durch **<w:p> ** Element innerhalb eines Dokuments. Ein Absatz besteht weiter aus einem oder mehreren Läufen **<w:r> ** das den eigentlichen Text des Absatzes enthält. Zusätzlich zu Läufen können Absätze auch andere Dokumentelemente wie Hyperlinks, Kommentare usw. enthalten. Eine beispielhafte Absatzstruktur sieht wie folgt aus:

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## Verweise ##

* [MS - DOCX-Dateiformat] (https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

