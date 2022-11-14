{
  "date" : "2019-10-11",
  "keywords" :[ "file vsdm", "formato file vsdm", "cos'è un file vsdm", "file", "esempio vsdm", "estensione file vsdm", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM - Formato file di disegno di Microsoft Visio",
  "description":"Scopri il formato di file VSDM e le API che possono creare e aprire file VSDM.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file VSDM?

I file con estensione .vsdm sono file di disegno creati con l'applicazione Microsoft Visio che supporta le macro. I file VSDM sono disegni OPC/XML simili a VSDX ma offrono anche la possibilità di eseguire macro all'apertura del file. Le macro sono azioni/passaggi definiti dall'utente che vengono sviluppati in Visual Basic, Applications Edition (VBA) e possono essere utilizzati per eseguire attività ripetitive. Il formato di file VSDM è stato introdotto con il lancio di Microsoft Visio 2013. I file Visio vengono utilizzati per creare disegni che contengono oggetti visivi, diagrammi di flusso, diagramma UML, flusso di informazioni, organigrammi, diagrammi software, layout di rete, modelli di database, mappatura di oggetti e altro informazioni simili. I file generati utilizzando Visio possono anche essere esportati in diversi formati di file come [PNG](/it/image/png/), [BMP](/it/image/bmp/), [PDF](/it/pdf/) e altri.

## Formato file VSDM

I file VSDM sono basati su Open Packaging Conventions e XML e gli sviluppatori possono trarre vantaggio da questo formato imparando a lavorare con questi file a livello di codice. Il formato eredita molte delle stesse strutture XML delle sue parti dal formato di file di disegno XML di Visio (.vdx). L'interoperabilità con i file di Visio è notevolmente aumentata poiché il software di terze parti può manipolare i file di Visio a livello di formato file.

Ogni file di Visio è definito come pacchetto che contiene altri file o parti. Una parte del pacchetto può essere un file XML, un'immagine o anche una soluzione VBA. Le parti all'interno del pacchetto possono essere suddivise in parti "documento" e "relazione".

### Documento ###

Le parti del documento contengono il contenuto effettivo ei metadati del file di Visio, ad esempio il nome del file, la prima pagina e tutte le forme che contiene e persino le connessioni dati per le forme. Le immagini e i file di testo all'interno del pacchetto sono considerati parti del documento.

### Relazioni ###

Le parti di relazione di un file di Visio sono archiviate nella cartella "\_rels" e descrivono come le parti all'interno del pacchetto sono correlate a ciascuna. Fornisce inoltre la struttura del file. Un documento XML autonomo utilizza la relazione padre/figlio degli elementi per determinare la relazione tra le entità. Un formato di file Visio 2013 valido contiene il set di parti corretto e il pacchetto contiene le relazioni tra le parti.

Le parti di relazione sono documenti XML che descrivono le relazioni tra le diverse parti del documento all'interno del pacchetto. Definiscono un'associazione tra due elementi: un'origine specificata (definita dal nome e dalla posizione del file di relazione) e una parte del documento di destinazione specificata. Ad esempio, le parti di relazione vengono utilizzate per descrivere quali master di forma sono associati al file, in che modo le pagine sono correlate al file e tra loro o in che modo immagini e oggetti sono correlati a una pagina specifica.

## Riferimenti ##

* [Introduzione al formato file di Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

