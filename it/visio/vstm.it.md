{
  "date" : "2019-10-11",
  "keywords" :[ "file vstm", "formato file vstm", "cos'è un file vstm", "file", "esempio vstm", "estensione file vstm", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTM - Formato file modello Microsoft Visio",
  "description":"Scopri il formato di file VSTM e le API che possono creare e aprire file VSTM.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file VSTM?

I file con estensione VSTM sono file modello creati con Microsoft Visio che supportano le macro. A differenza dei file VSDX, i file creati da modelli VSTM possono eseguire macro sviluppate nel codice Visual Basic, Applications Edition (VBA). È possibile creare un file modello per fornire le impostazioni di base del documento che possono essere utilizzate per generare ulteriori documenti con queste impostazioni. I file Visio vengono utilizzati per creare disegni che contengono oggetti visivi, diagrammi di flusso, diagramma UML, flusso di informazioni, organigrammi, diagrammi software, layout di rete, modelli di database, mappatura di oggetti e altre informazioni simili. I file generati utilizzando Visio possono anche essere esportati in diversi formati di file come PNG, BMP, PDF e altri.

## Formato del file ##

I file VSTM sono basati su Open Packaging Conventions e XML e gli sviluppatori possono trarre vantaggio da questo formato imparando a lavorare con questi file a livello di codice. Il formato eredita molte delle stesse strutture XML delle sue parti dal formato di file di disegno XML di Visio (.vdx). L'interoperabilità con i file di Visio è notevolmente aumentata poiché il software di terze parti può manipolare i file di Visio a livello di formato file.

Ogni file di Visio è definito come pacchetto che contiene altri file o parti. Una parte del pacchetto può essere un file XML, un'immagine o anche una soluzione VBA. Le parti all'interno del pacchetto possono essere suddivise in parti "documento" e "relazione".

### Documento ###

Le parti del documento contengono il contenuto effettivo ei metadati del file di Visio, come il nome del file, la prima pagina e tutte le forme che contiene, e anche le connessioni dati per le forme. Le immagini e i file di testo all'interno del pacchetto sono considerati parti del documento.

### Relazioni ###

Le parti di relazione di un file di Visio sono archiviate nella cartella "_rels" e descrivono come le parti all'interno del pacchetto sono correlate a ciascuna. Fornisce inoltre la struttura del file. Un documento XML autonomo utilizza la relazione padre/figlio degli elementi per determinare la relazione tra le entità. Un formato di file Visio 2013 valido contiene il set di parti corretto e il pacchetto contiene le relazioni tra le parti.

Le parti di relazione sono documenti XML che descrivono le relazioni tra le diverse parti del documento all'interno del pacchetto. Definiscono un'associazione tra due elementi: un'origine specificata (definita dal nome e dalla posizione del file di relazione) e una parte del documento di destinazione specificata. Ad esempio, le parti di relazione vengono utilizzate per descrivere quali master di forma sono associati al file, in che modo le pagine sono correlate al file e tra loro o in che modo immagini e oggetti sono correlati a una pagina specifica.

## Riferimenti ##

* [Introduzione al formato file di Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

