{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "file", "estensione", "formato file", "Excel", "Foglio di calcolo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file OTS e le API che possono creare e aprire file OTS.",
  "title" :"OTS - Formato file modello foglio di calcolo OpenDocument",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Che cos'è un file OTS?

Un file con estensione .ots è un file modello di foglio di calcolo OpenDocument creato con il software applicativo Calc incluso in Apache OpenOffice. Il software applicativo Calc è simile a Excel disponibile in Microsoft Office. Il formato file OTS viene utilizzato per creare modelli che contengono impostazioni predefinite relative a stili, font, dati, layout del foglio di calcolo e formattazione. I file OTF hanno `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. Questi file modello possono essere utilizzati come punto di partenza per generare e salvare file di dati effettivi che vengono salvati in [formato file ODS](/it/spreadsheet/ods/). I file OTS possono essere utilizzati con applicazioni come OpenOffice e LibreOffice.

## Formato file OTS

I file OTS vengono salvati nel formato di file basato su XML OpenDocument di OASIS che comprende una raccolta di diversi documenti secondari con un pacchetto come archivio [ZIP](/it/compression/zip/). Ogni archivio zip memorizza parte del documento completo e ogni documento secondario memorizza un aspetto particolare del documento. Ad esempio, un documento secondario contiene le informazioni sullo stile e un altro documento secondario contiene il contenuto del documento. Un tipico documento ODF ha i seguenti componenti:

### Contenuto OTS.xml

Il file content.xml contiene il contenuto effettivo del documento. Tuttavia, questo non include dati binari come immagini.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml di formato file OTS

Il file styles.xml contiene informazioni sullo stile ed è ampiamente utilizzato per la formattazione e il layout. I tipi di stili includono:

* Stili di paragrafo
* Stili di pagina
* Stili di carattere
* Stili di cornice
* Elenca gli stili

### Meta.xml

Il file meta.xml contiene informazioni sui metadati del file come Autore, Data dell'ultima modifica, ecc.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Impostazioni.xml

Il file `settings.xml` include impostazioni a livello di documento come il fattore di zoom e la posizione del cursore.

## Riferimenti ##

* [Specifica OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - Di Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

