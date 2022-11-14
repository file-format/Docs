{
  "date" : "2019-10-11",
  "keywords" :[ "file odp", "formato file odp", "cos'è un file odp", "file", "esempio odp", "estensione file odp", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - Formato file di presentazione di OpenOffice",
  "description":"Scopri il formato di file ODP e le API che possono creare e aprire file ODP.",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file ODP?

I file con estensione .odp rappresentano il formato di file di presentazione utilizzato da OpenOffice.org nello standard OASISOpen. Un file di presentazione è una raccolta di diapositive in cui ciascuna diapositiva può comprendere testo, immagini, formattazione, animazioni e altri media. Queste diapositive vengono presentate al pubblico sotto forma di presentazioni con impostazioni di presentazione personalizzate. I file ODP possono essere aperti da applicazioni conformi al formato OpenDocument (come OpenOffice o StarOffice).

## Breve storia

Le specifiche del formato file ODP si basano sullo standard sviluppato come specifiche ODF. Queste specifiche si sono evolute in passato sotto forma di tre versioni sviluppate e pubblicate da OASIS come segue:

`2005` - La versione 1.0 è stata pubblicata nel maggio 2005
`2007` - La versione 1.1 è stata pubblicata nel febbraio 2007
`2011` - La versione 1.2 è stata pubblicata a settembre 2011

Ci sono stati cambiamenti piuttosto minori nella transizione dalle versioni ODF 1.0 alla 1.1. La [versione ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) è l'ultima versione per le specifiche ODF e dovrebbe essere consultata dagli sviluppatori per lo sviluppo di applicazioni relative alla lettura/scrittura ODS.

## Specifiche del formato file

Il formato OpenDocument supporta la rappresentazione del documento come un singolo documento XML, nonché una raccolta di diversi documenti secondari all'interno di un pacchetto come archivio [ZIP](https://docs.fileformat.com/Compression/ZIP/). Ciascuno dei file dell'archivio ZIP memorizza parte del documento completo. Ogni documento secondario memorizza un aspetto particolare del documento. Ad esempio, un documento secondario contiene le informazioni sullo stile e un altro documento secondario contiene il contenuto del documento. Un tipico documento ODF ha i seguenti componenti:

* `content.xml` – Contenuto del documento e stili automatici utilizzati nel contenuto.
* `styles.xml` – Stili usati nel contenuto del documento e stili automatici usati negli stili stessi.
* `meta.xml` – Le metainformazioni del documento, come l'autore o l'ora dell'ultima azione di salvataggio.
* `settings.xml` – Impostazioni specifiche dell'applicazione, come le dimensioni della finestra o le informazioni sulla stampante.

Oltre a questi, nel pacchetto possono essere presenti molti altri documenti secondari come la miniatura del documento, le immagini, ecc.

I file del documento del foglio di calcolo sono il sottoinsieme dei file ODF in cui il contenuto (fogli) è archiviato nel documento secondario content.xml.

## Riferimenti

* [OpenDocument - Di Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

