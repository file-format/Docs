{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "File database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file ACCDT e le API che possono creare e aprire file ACCDT.",
  "title" :"ACCDT - Formato file database modello Microsoft Access 2007",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Che cos'è un file ACCDT?

Un file con estensione .accdt è un file modello di database di Microsoft Access che contiene elementi di database predefiniti. Questi elementi sono una raccolta di strutture che definiscono applicazioni di database come schemi di database per la memorizzazione dei dati, descrizione del layout per le visualizzazioni dei dati e metadati che descrivono il database. Essendo file modello, i file ACCDT possono essere utilizzati per creare database basati sulle impostazioni del modello disponibili in questi. I file di database risultanti vengono salvati come file [ACCDB](/it/database/accdb/) e popolati con i dati nelle tabelle. Microsoft Access 2007 e versioni successive possono aprire file ACCDT.

## Formato file ACCDT

I file modello ACCDT si basano sulle specifiche Office Open XML e tutti i dati sono contenuti in un pacchetto ZIP. Le informazioni sulla struttura e sui contenuti del database sono contenute nei file [XML](/it/web/xml/) e nei file di testo e sono collegate tra loro tramite relazioni. È possibile rinominare un file ACCDT con estensione [.zip](/it/compression/zip/) e utilizzare qualsiasi software di compressione per estrarre il contenuto dell'archivio ZIP.

### Struttura del file

I file ACCDT sono pacchetti che contengono una raccolta di parti correlate. Ciascuna **parte** memorizza informazioni sui contenuti di un'applicazione di database utilizzando formati XML, di testo e binari, che includono:

* Oggetti di database
* Metadati associati
* Struttura del pacchetto

#### Pacchetto

Un pacchetto è un archivio [ZIP](/it/compression/zip/) che contiene più parti ed è conforme alle convenzioni Open Packaging specificate in [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html). I file ACCDT devono contenere almeno una parte di metadati del modello che dovrebbe essere la destinazione di una relazione. Questi metadati del modello sono la parte iniziale di un file ACCDT.

#### Parte

Una parte è un flusso di byte a cui è associato un tipo per specificare la natura e il tipo di contenuto in essa archiviato. L'enumerazione delle parti specifica le parti valide, i tipi di contenuto validi e le relazioni obbligatorie tra tutte le parti in un pacchetto.

#### Relazione

`Package Relationship` - dove la destinazione è una parte e l'origine è il pacchetto nel suo insieme.

`Relazione da parte a parte' - dove la destinazione è una parte e l'origine è una parte del pacchetto.

`Relazione esplicita` - dove si fa riferimento a una risorsa dal contenuto di una parte di origine facendo riferimento a un elemento di relazione in base al valore del suo attributo ID.

`Relazione implicita` - una relazione che non è esplicita.

`Relazione interna` - dove il target fa parte del pacchetto.

`Relazione esterna` - dove la destinazione è una risorsa esterna non nel pacchetto.

## Riferimenti ##

* [Accesso al formato file modello](https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

