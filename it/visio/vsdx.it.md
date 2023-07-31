{
  "date" : "2019-10-11",
  "keywords" :[ "file vsdx", "formato file vsdx", "cos'è un file vsdx", "file", "esempio vsdx", "estensione file vsdx", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDX",
  "description":"Scopri il formato di file VSDX e le API che possono creare e aprire file VSDX.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file VSDX?

I file con estensione .vsdx rappresentano il formato di file Microsoft Visio introdotto da Microsoft Office 2013 in poi. È stato sviluppato per sostituire il formato di file binario, [.VSD](/it/image/vsd/), supportato dalle versioni precedenti di Microsoft Visio. È inoltre supportato in Visio Services in Microsoft SharePoint Server 2013 e non richiede un formato file intermedio per la pubblicazione su SharePoint Server. I file Visio vengono utilizzati per creare disegni che contengono oggetti visivi, diagrammi di flusso, diagramma UML, flusso di informazioni, organigrammi, diagrammi software, layout di rete, modelli di database, mappatura di oggetti e altre informazioni simili. I file generati utilizzando Visio possono anche essere esportati in diversi formati di file come [PNG](/it/image/png/), [BMP](/it/image/bmp/), [PDF](/it/pdf/) e altri.

## Formato del file ##

I file VSDX sono basati su Open Packaging Conventions e XML e gli sviluppatori possono trarre vantaggio da questo formato imparando a lavorare con questi file a livello di codice. Il formato eredita molte delle stesse strutture XML delle sue parti dal formato di file di disegno XML di Visio (.vdx). L'interoperabilità con i file di Visio è notevolmente aumentata poiché il software di terze parti può manipolare i file di Visio a livello di formato file.

Alcuni altri tipi di file che comprendono il formato di file di Visio 2013 includono:

* .vsdm (disegno abilitato alle macro di Visio)
* .vssx (stencil di Visio)
* .vssm (stencil con abilitazione macro di Visio)
* .vstx (modello di Visio)
* .vstm (modello abilitato per le macro di Visio)

Sotto il cofano, il formato di file Visio 2013 utilizza un mezzo strutturato per archiviare i dati dell'applicazione insieme alle risorse correlate in un archivio come [ZIP](/it/compression/zip/). Il file ZIP può essere estratto utilizzando qualsiasi utilità di estrazione standard in cui contiene anche altri tipi di file. Puoi semplicemente sostituire l'estensione del file .vsdx con .zip in Windows Explorer per vedere il contenuto all'interno del file VSDX.

Ogni file di Visio è definito come pacchetto che contiene altri file o parti. Una parte del pacchetto può essere un file XML, un'immagine o anche una soluzione VBA. Le parti all'interno del pacchetto possono essere suddivise in parti "documento" e "relazione".

### Documento ###

Le parti del documento contengono il contenuto effettivo ei metadati del file di Visio, come il nome del file, la prima pagina e tutte le forme che contiene, e anche le connessioni dati per le forme. Le immagini e i file di testo all'interno del pacchetto sono considerati parti del documento.

### Relazioni ###

Le parti di relazione di un file di Visio sono archiviate nella cartella "\_rels" e descrivono come le parti all'interno del pacchetto sono correlate a ciascuna. Fornisce inoltre la struttura del file. Un documento XML autonomo utilizza la relazione padre/figlio degli elementi per determinare la relazione tra le entità. Un formato di file Visio 2013 valido contiene il set di parti corretto e il pacchetto contiene le relazioni tra le parti.

Le parti di relazione sono documenti XML che descrivono le relazioni tra le diverse parti del documento all'interno del pacchetto. Definiscono un'associazione tra due elementi: un'origine specificata (definita dal nome e dalla posizione del file di relazione) e una parte del documento di destinazione specificata. Ad esempio, le parti di relazione vengono utilizzate per descrivere quali master di forma sono associati al file, in che modo le pagine sono correlate al file e tra loro o in che modo immagini e oggetti sono correlati a una pagina specifica.

## Riferimenti ##

* [Introduzione al formato file di Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

