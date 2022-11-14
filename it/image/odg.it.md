{
  "date" : "2019-10-11",
  "keywords" :[ "file odg", "formato file odg", "cos'è un file odg", "file", "esempio odg", "estensione file odg", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file ODG",
  "description":"Scopri il formato di file ODG e le API che possono creare e aprire file ODG.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file ODG?

Il formato di file ODG viene utilizzato dall'applicazione Draw di Apache OpenOffice per memorizzare gli elementi di disegno come immagine vettoriale. Segue le specifiche del formato file basato su XML delineate da Advancement of Structural Information Standards (OASIS). ODG rappresenta i disegni come immagini vettoriali utilizzando punti, linee e curve. Oltre a OpenOffice, LibreOffice e altre applicazioni forniscono anche supporto per lavorare con il formato di file ODG. Altri formati supportati da OpenOffice, ad esempio, includono [ODT](/it/word-processing/odt/), ODF, [ODP](/it/presentation/odp/) e [ODS](/it/spreadsheet/ods/).


## Specifiche del formato file ODG

Il formato di file ODG si basa sul formato OpenDocument che è un formato di documento XML strutturato con uno schema ben definito.
Ogni componente strutturale di un formato OpenDocument è rappresentato da un elemento a cui sono associati attributi. La struttura basata su XML è comune a tutti i tipi di documenti come documenti di testo, fogli di calcolo o file di disegno. Un documento può contenere stili diversi. Una struttura di file OpenDocument è composta dai seguenti elementi.
* Radice del documento
* Documento Metadati
* Tipi di elementi del corpo e di documenti
* Impostazioni dell'applicazione
* Script
* Dichiarazioni dei volti dei caratteri
* Stili
* Stili di pagina e layout

## Radici del documento ##

Un elemento radice del documento contiene l'intero documento ed è l'elemento principale di un file in formato OpenDocument. Gli stessi tipi di elementi radice del documento sono applicabili a tutti i tipi di documento come testo, documenti, fogli di calcolo e documenti di disegno.

### Elementi radice ###
Un singolo documento XML è rappresentato dal proprio elemento radice. I cinque diversi elementi radice supportati sono i seguenti.

`<office:document> ` - Documento Office completo in un unico documento XML.
`<office:document-content> ` - Contenuto del documento e stili automatici utilizzati nel contenuto.
`<office:document-styles> ` - Stili utilizzati nel contenuto del documento e stili automatici utilizzati negli stili stessi.
`<office:document-meta> ` - Metainformazioni del documento, come l'autore o l'ora dell'ultima azione di salvataggio.
`<office:document-settings> ` - Impostazioni specifiche dell'applicazione, come le dimensioni della finestra o le informazioni sulla stampante.

### Metadati del documento ODG ###
OpenDocument contiene tutti gli elementi di metadati in \<office:meta> elemento. Queste informazioni generali su un documento sono contenute all'inizio del documento e le applicazioni possono aggiornare più istanze degli stessi elementi.

### Elementi del corpo e tipi di documenti ###
Il corpo del documento indica il tipo di contenuto contenuto nel documento utilizzando l'elemento tipo di documento. Questi tipi di documenti sono:
* documenti di testo
* documenti di disegno
* documenti di presentazione
* fogli di calcolo
* documenti grafici
* documenti immagine

### Impostazioni dell'applicazione ###
Le impostazioni per le applicazioni per ufficio rappresentano impostazioni diverse correlate alla configurazione del documento o all'aspetto visivo del documento. Ogni categoria è rappresentata da un `<config:config-item-set> `. Esempi di tali categorie di impostazioni includono:
* Impostazioni del documento, ad es. stampante predefinita
* Visualizza le impostazioni, ad esempio il livello di zoom

### Script ###
È comune che un documento contenga diversi script. Ogni script in un file OpenDocument è rappresentato da un `<office:script> ` elemento. Questi elementi di script sono contenuti in un singolo `<office:scripts> ` elemento. Gli script non aggiornano un documento durante il caricamento del documento.
### Dichiarazioni dei volti dei caratteri ###

Una dichiarazione di tipo di carattere contiene informazioni sui caratteri utilizzati dall'autore di un documento. Queste informazioni aiutano a individuare questi caratteri su altri sistemi.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Stili ###
Gli stili seguenti sono supportati dal formato OpenDocument.

`Stili comuni` - Le rappresentazioni XML di tali stili vengono chiamate stili
`Stili automatici` - Contiene proprietà di formattazione che, nella vista dell'interfaccia utente di un documento, sono assegnate a un oggetto come un paragrafo.
`Stili Mater`: uno stile comune che contiene informazioni sulla formattazione e contenuto aggiuntivo che viene visualizzato con il contenuto del documento quando viene applicato lo stile. Un esempio di stile master sono le pagine master.

## Riferimenti ##
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Formato OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

