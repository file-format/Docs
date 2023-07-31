{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX", "bestand", "formaat", "bestandstype", "extensie", "wat is een DOCX-bestand?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"Meer informatie over de DOCX-bestandsindeling en API's die DOCX-bestanden kunnen maken en openen.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Wat is een DOCX-bestand? ##

DOCX is een bekend formaat voor Microsoft Word-documenten. Geïntroduceerd vanaf 2007 met de release van Microsoft Office 2007, werd de structuur van dit nieuwe documentformaat gewijzigd van gewoon binair naar een combinatie van XML en binaire bestanden. Docx-bestanden kunnen worden geopend met Word 2007 en laterale versies, maar niet met de eerdere versies van MS Word die DOC-bestandsextensies ondersteunen.

## Korte geschiedenis ##

Nadat Microsoft de specificaties voor het DOC-bestandsformaat had geopend, was het voor zijn concurrenten gemakkelijk om het formaat te reverse-engineeren en dezelfde ondersteuning te bieden in hun eigen applicaties. Bovendien dwong de concurrentie van Open Office in de vorm van zijn Open Document Format, Microsoft om meer open en brede standaarden te hanteren. Het was begin 2000 toen Microsoft besloot om voor de verandering te gaan om de standaard voor **Office Open XML** te accommoderen. Documenten onder deze nieuwe standaard kregen [.docx extensie](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), de "X" voor XML zijn. In 2007 werd dit nieuwe bestandsformaat onderdeel van Office 2007 en wordt het ook voortgezet in de nieuwe versies van Microsoft Office. Het nieuwe bestandstype heeft voordelen toegevoegd van kleine bestandsgroottes, minder veranderingen van corruptie en goed opgemaakte afbeeldingen.

## Specificaties DOCX-bestandsindeling - Meer informatie

Een Docx-bestand bestaat uit een verzameling XML-bestanden die zich in een ZIP-archief bevinden. De inhoud van een nieuw Word-document kan worden bekeken door de inhoud uit te pakken. De collectie bevat een lijst met XML-bestanden die zijn gecategoriseerd als:

* MetaData-bestanden - bevat informatie over andere bestanden die beschikbaar zijn in het archief
* Document - bevat de feitelijke inhoud van het document

### Metadatabestanden ###

Microsoft Word gebruikt deze bestanden om de relatie tussen bestanden te vinden en om de inhoud van het document te vinden. Wanneer een Word-documentarchief wordt uitgepakt, bevat het een aantal van dergelijke bestanden, zoals hieronder beschreven.

#### Relaties - \_rels/.rels ####

Dit bestand bevat informatie die MS Word vertelt waar de documentinhoud en andere verwijzingen moeten worden gezocht. Elke relatie wordt geïdentificeerd door een unieke relatie-ID en specificeert het XML-bestand waarnaar wordt verwezen als doel. Een voorbeeldrelatiebestand wordt als volgt weergegeven:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Inhoudstypen ####

Een document kan verschillende mediatypen bevatten, zoals afbeeldingen, thema's, woordkunst, enz. De [Content_Types].xml bevat informatie over dergelijke mediatypen die in het document aanwezig zijn. De inhoud van zo'n XML-bestand wordt als volgt weergegeven:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Verwijzingen naar bronnen - \_rels/document.xml.rels ####

In dit XML-bestand wordt verwezen naar informatie over bronnen, zoals afbeeldingen die in het document zijn ingesloten.

#### Inhoud hoofddocument ####

Dit verwijst naar het XML-hoofdbestand van het archief dat de tekstinhoud van het document bevat. Deze inhoud wordt weergegeven door verschillende knooppunten volgens de OpenOffice XML-specificaties. Meestal bestaat de inhoud van dit bestand uit alinea's en tabellen, hoewel het ook andere knooppunten kunnen zijn.

### Bestandsindeling Knooppunten ###

Het hoofdbestand document.xml is een verzameling knooppunten voor de weergave van de algemene inhoud van een bestand. Elk knooppunt heeft een begin en einde dat ofwel verdere knooppunten of de inhoud inkapselt. Een vereenvoudigd voorbeeld van zo'n xml-bestand is als volgt:

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

Hieronder volgt de informatie over enkele van de knooppunten in een DOCX-bestand voor weergave van de inhoud.

`<w:document> ` - Vertegenwoordigt het root-element van de hoofdinhoud van het bestand.

`<w:body> ` - Vertegenwoordigt de hoofdtekst van het document die uit vele andere elementknooppunten kan bestaan, zoals alinea's, tabellen en secties.

#### Alinea's ####

Een alinea is de belangrijkste inhoudshouder in een document. Het wordt vertegenwoordigd door **<w:p> ** element binnen een document. Een alinea bestaat verder uit één of meerdere runs**<w:r> ** die de eigenlijke tekst van de paragraaf bevat. Naast runs kunnen alinea's ook andere documentelementen bevatten, zoals hyperlinks, opmerkingen, enz. Een voorbeeld van een alineastructuur is als volgt:

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

## Referenties ##

* [MS - DOCX-bestandsindeling](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

