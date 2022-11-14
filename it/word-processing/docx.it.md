{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX", "file", "formato", "tipo di file", "estensione", "cos'è un file DOCX?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"Scopri il formato di file DOCX e le API che possono creare e aprire file DOCX.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Che cos'è un file DOCX? ##

DOCX è un formato ben noto per i documenti di Microsoft Word. Introdotto dal 2007 con il rilascio di Microsoft Office 2007, la struttura di questo nuovo formato del documento è stata modificata da semplice binario a una combinazione di file XML e binari. I file Docx possono essere aperti con Word 2007 e versioni laterali ma non con le versioni precedenti di MS Word che supportano le estensioni di file DOC.

## Breve storia ##

Dopo che Microsoft ha aperto le specifiche per il formato di file DOC, è stato facile per i suoi concorrenti decodificare il formato e fornire lo stesso supporto nelle proprie applicazioni. Inoltre, la concorrenza di Open Office nella forma del suo Open Document Format, ha costretto Microsoft ad adottare standard più aperti e ampi. Fu all'inizio del 2000 quando Microsoft decise di adottare la modifica per accogliere lo standard per **Office Open XML**. Ai documenti in base a questo nuovo standard è stata assegnata [estensione .docx](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), la "X" essendo per XML. Entro il 2007, questo nuovo formato di file è entrato a far parte di Office 2007 e viene mantenuto anche nelle nuove versioni di Microsoft Office. Il nuovo tipo di file ha aggiunto vantaggi di file di piccole dimensioni, meno modifiche alla corruzione e rappresentazione delle immagini ben formattata.

## Specifiche del formato file DOCX - Ulteriori informazioni

Un file Docx comprende una raccolta di file XML contenuti all'interno di un archivio ZIP. Il contenuto di un nuovo documento di Word può essere visualizzato decomprimendone il contenuto. La raccolta contiene un elenco di file XML classificati come:

* File di metadati: contiene informazioni su altri file disponibili nell'archivio
* Documento: contiene il contenuto effettivo del documento

### File di metadati ###

Microsoft Word utilizza questi file per trovare la relazione tra i file e per individuare il contenuto del documento. Quando un archivio di documenti di Word viene estratto, contiene un numero di tali file come descritto di seguito.

#### Relazioni - \_rels/.rels ####

Questo file contiene informazioni che indicano a MS Word dove cercare il contenuto del documento e altri riferimenti. Ciascuna relazione è identificata da un ID relazione univoco e specifica il file XML di riferimento come destinazione. Un file di relazione di esempio è mostrato come segue:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Tipi di contenuto ####

Un documento può contenere diversi tipi di media all'interno come immagini, temi, word art, ecc. [Content_Types].xml contiene informazioni su tali tipi di media presenti nel documento. Il contenuto di un tale file XML è mostrato come segue:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Riferimenti alle risorse - \_rels/document.xml.rels ####

Le informazioni sulle risorse, come le immagini incorporate nel documento, sono referenziate in questo file XML.

#### Contenuto del documento principale ####

Si riferisce al file XML principale dell'archivio che contiene il contenuto testuale del documento. Questo contenuto è rappresentato da una varietà di nodi secondo le specifiche OpenOffice XML. Per lo più il contenuto di questo file è costituito da paragrafi e tabelle, sebbene possano essere anche altri nodi.

### Nodi formato file ###

Il file document.xml principale è una raccolta di nodi per la rappresentazione del contenuto generale di un file. Ogni nodo ha un inizio e una fine che incapsula altri nodi o il contenuto. Un esempio semplificato di tale file xml è il seguente:

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

Di seguito sono riportate le informazioni su alcuni dei nodi contenuti in un file DOCX per la rappresentazione dei contenuti.

`<w:document> ` - Rappresenta l'elemento radice del contenuto principale del file.

`<w:body> ` - Rappresenta il corpo del documento che può comprendere molti altri nodi di elementi come paragrafi, tabelle e sezioni.

#### Paragrafi ####

Un paragrafo è il principale titolare del contenuto all'interno di un documento. È rappresentato da **<w:p> ** elemento all'interno di un documento. Un paragrafo è inoltre costituito da una o più esecuzioni **<w:r> ** che contiene il testo vero e proprio del paragrafo. Oltre alle esecuzioni, i paragrafi possono contenere anche altri elementi del documento come collegamenti ipertestuali, commenti, ecc. Di seguito è illustrata una struttura di paragrafo di esempio:

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

## Riferimenti ##

* [Formato file MS - DOCX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

