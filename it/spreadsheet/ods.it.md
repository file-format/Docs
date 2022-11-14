{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "file", "estensione", "formato file", "OpenDocument Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"La tua guida al formato dei file per sapere cos'è un file ODS e le API che possono crearli e aprirli.",
  "title" :"Cos'è un file ODS?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Che cos'è un file ODS?

I file con estensione .ods stanno per il formato OpenDocument Spreadsheet Document che sono modificabili dall'utente. I dati vengono archiviati all'interno del file ODF in righe e colonne. È un formato basato su XML ed è uno dei numerosi sottotipi della famiglia Open Document Formats (ODF). Il formato è specificato come parte delle specifiche ODF 1.2 pubblicate e mantenute da OASIS. Numerose applicazioni su Windows e altri sistemi operativi possono aprire file ODS per la modifica e la manipolazione, inclusi Microsoft Excel, NeoOffice e LibreOffice. I file ODS possono anche essere convertiti in altri formati di fogli di calcolo, come [XLS](/it/spreadsheet/xls/), [XLSX](/it/spreadsheet/xlsx/) e altri da diverse applicazioni.

## Breve storia ##

Le specifiche del formato di file ODS si basano sullo standard sviluppato come specifiche ODF. Queste specifiche si sono evolute in passato sotto forma di tre versioni sviluppate e pubblicate da OASIS come segue:

`2005`- La versione 1.0 è stata pubblicata nel maggio 2005

`2007` - La versione 1.1 è stata pubblicata nel febbraio 2007

`2011` - La versione 1.2 è stata pubblicata a settembre 2011

Ci sono stati cambiamenti piuttosto minori nella transizione dalle versioni ODF 1.0 alla 1.1. La [versione ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) è l'ultima versione per le specifiche ODF e dovrebbe essere consultata dagli sviluppatori per lo sviluppo di applicazioni relative alla lettura/scrittura ODS.

## Formato file ODS ##

Il formato OpenDocument supporta la rappresentazione del documento come un singolo documento XML, nonché una raccolta di diversi documenti secondari all'interno di un pacchetto come archivio [ZIP](/it/compression/zip/). Ciascuno dei file dell'archivio ZIP memorizza parte del documento completo. Ogni documento secondario memorizza un aspetto particolare del documento. Ad esempio, un documento secondario contiene le informazioni sullo stile e un altro documento secondario contiene il contenuto del documento. Un tipico documento ODF ha i seguenti componenti:

* `content.xml` – Contenuto del documento e stili automatici utilizzati nel contenuto.
* `styles.xml` – Stili usati nel contenuto del documento e stili automatici usati negli stili stessi.
* `meta.xml` – Le metainformazioni del documento, come l'autore o l'ora dell'ultima azione di salvataggio.
* `settings.xml` – Impostazioni specifiche dell'applicazione, come le dimensioni della finestra o le informazioni sulla stampante.

Oltre a questi, nel pacchetto possono essere presenti molti altri documenti secondari come la miniatura del documento, le immagini, ecc.

I file del documento del foglio di calcolo sono il sottoinsieme dei file ODF in cui il contenuto (fogli) è archiviato nel documento secondario content.xml.

## Riferimenti ##

* [OpenDocument - Di Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

