{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Formato file", "CAD", "Apri", "Crea" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file DWG e le API che possono creare e aprire file DWG.",
  "title" :"Formato file DWG",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file DWG?

I file con estensione DWG rappresentano file binari proprietari utilizzati per contenere dati di progettazione 2D e 3D. Come DXF, che sono file ASCII, DWG rappresenta il formato di file binario per i disegni CAD (Computer Aided Design). Contiene immagini vettoriali e metadati per la rappresentazione dei contenuti dei file CAD. Sono disponibili visualizzatori gratuiti per la visualizzazione di file DWG sul sistema operativo Windows come il DWG TrueView gratuito di Autodesk. Esistono anche altre applicazioni di terze parti che supportano il raggiungimento di file DWG. I file DWG contengono informazioni create dall'utente e includono:

* Disegni
* Dati geometrici
* Mappe e foto

Questo formato è ampiamente utilizzato da architetti, ingegneri e designer per vari scopi di progettazione.

## Breve storia ##

Il formato del file DWG si è evoluto nel tempo dalla sua introduzione formale nel 1982. Di seguito è riportata una breve panoramica degli eventi passati dal punto di vista storico.

**1982:** Autodesk ha concesso in licenza il formato di file DWG, sviluppato da Mike Riddle nel 1970, come base per AutoCAD.

**1998:** Con il rilascio di AutoCAD R14.01, Autodesk ha aggiunto la verifica dei file tramite una funzione denominata DWGCHECK che incorporava un checksum crittografato e un codice prodotto, denominato WaterMark da Autodesk, nei file DWG creati dal programma.

**2006:** Autodesk ha modificato AutoCAD 2007, per includere "Tecnologia TrustedDWG" per incorporare la stringa di testo "Autodesk DWG. Questo file è un DWG affidabile salvato l'ultima volta da un'applicazione Autodesk o da un'applicazione con licenza Autodesk" nei file DWG. Lo scopo di questo era aiutare gli utenti del software Autodesk a garantire che questi file fossero creati da un'applicazione Autodesk o RealDWG, il che dovrebbe sicuramente aiutare a ridurre il rischio di incompatibilità.

## Struttura del file ##

DWG è stato uno dei formati di file ampiamente utilizzati da una vasta gamma di applicazioni e ha una struttura di file robusta. Poiché DWG è un formato di file binario, non è leggibile come il semplice formato di file ASCII [DXF](/it/cad/dxf/). I file DWG di solito includono informazioni sulle coordinate dell'immagine e su eventuali metadati ad essa associati. Le [specifiche](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) complete del formato file DWG sono disponibili per il download da OpenDesign. La struttura del file del formato di file DWG è riassunta come segue.

**Intestazione**: l'intestazione del file è composta da variabili di intestazione DWG e informazioni su Cyclic Redundancy Check (CRC) che viene utilizzato per il rilevamento degli errori. Ogni sottosezione è un vettore specializzato in cui vengono utilizzate diverse lunghezze di bit per rappresentare etichette diverse. Ad esempio, i primi 6 bit della variabile DWG Header rappresentano la stringa della versione.

**Definizioni di classi:** Un file DWG può contenere numerose classi a seconda dello scopo specifico del file .dwg. Informazioni come la dimensione dei metadati della classe dell'area dati della classe, il numero della classe e il checksum oltre ad altri.

**Modello**: questo è facoltativo e per le versioni R15 e R15, questa sezione si trova sotto la sezione Spazio libero oggetto.

**Padding**: i metadati hanno suffisso e suffisso un numero specifico di byte che rende le versioni precedenti del software AutoCAD compatibili con il nuovo formato di file DWG.

**Dati immagine**: i metadati per questa sezione dipendono dal tipo .dwg specifico. Per gli utenti R14 e R15, questa sezione è facoltativa.

**Dati oggetto**: i dati oggetto sono costituiti da un elenco completo di entità tabella, voci di dizionario, ecc. corrispondenti all'elenco esistente di oggetti.

**Mappa oggetti**: la posizione di ogni oggetto nel file è specificata in questa sezione del file. La maggior parte dei metadati in questa sezione sono handle di file che svolgono un ruolo nell'identificazione e nel re-rendering dell'oggetto.

**Spazio libero oggetto**: questa sezione è facoltativa per tutti gli utenti

**Seconda intestazione**: un duplicato della sezione dell'intestazione del file verso la fine del file DWG

## Riferimenti ##

* [Specifiche del formato file DWG](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [Specifica del file DWG](https://www.scan2cad.com/blog/dwg/file-spec/)
* [DWG - Di Wikipedia](https://en.wikipedia.org/wiki/.dwg)

