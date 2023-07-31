{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file PDB - Un file di database di programma",
  "description":"Scopri il formato di file PDB e le API che possono creare e aprire file PDB.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Che cos'è un file PDB?

Un file con estensione .pdb è un file di database di programma che contiene informazioni di debug per un eseguibile compilato (EXE/DLL). I file PDB vengono generati dai compilatori Microsoft quando un programma applicativo viene compilato in modalità di debug. La presenza del file PDB può aiutare nel reverse engineering di un eseguibile in quanto contiene informazioni significative su tutti i simboli dei moduli. È per questo motivo che questi file vengono mantenuti separati dall'eseguibile finale. L'[API DgbHelp] di Microsoft (https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) può aprire un file PDB per ottenere informazioni quali public ed esportazioni, simboli globali, simboli locali, digitare dati, file di origine e numeri di riga.

## Formato file PDB

PDB è il formato di file proprietario di Microsoft e non è stato ancora documentato ufficialmente da nessuna parte. Tuttavia, una documentazione iniziale è disponibile [qui](https://github.com/Microsoft/microsoft-pdb) e può essere referenziata.

### Stream PDB

I file PDB sono costituiti da più flussi in cui ogni flusso agisce come un singolo file virtuale e contiene informazioni. I writer di file PDB possono scrivere su questi file e il file viene finalizzato solo dopo l'emissione di un commit esplicito. Un compilatore può continuare a scrivere su un file PDB ma eseguire il commit solo se tutto il codice utente viene compilato correttamente. Un file PDB è costituito dai seguenti flussi:

|Numero flusso |Contenuto |Breve descrizione|
---|---|---|
|1| Pdb (intestazione) |Informazioni sulla versione e informazioni per connettere questo PDB a EXE|
|2| Tpi (gestore dei tipi) |Tutti i tipi utilizzati nell'eseguibile.|
|3| Dbi (Informazioni di debug) |Contiene i contributi della sezione e l'elenco di 'Mod'|
|4| NomeMappa| Contiene una tabella di stringhe hash|
|4-(n+4)| n Mod (informazioni sul modulo)| Ogni flusso Mod contiene simboli e numeri di riga per una compilazione|
|n+4| Hash dei simboli globali| Un indice che permette la ricerca nei simboli globali per nome|
|n+5| Hash simbolo pubblico| Un indice che permette la ricerca nei simboli pubblici per indirizzi|
|n+6| Record di simboli| Record di simboli effettivi di simboli globali e pubblici|
|n+7| Digita hash| Hash utilizzato dal flusso TPI.|

Ciascun flusso in un file PDB comprende diverse pagine che non sono necessariamente numerate consecutivamente.

### Intestazione PDB

Un file PDB è dotato di un'intestazione che consiste in una firma per identificare e convalidare il formato specifico. La lunghezza della firma dipende dal formato PDB. L'intestazione potrebbe essere più lunga di una singola pagina.

### Metadati PDB
I metadati PDB sono responsabili di riconoscere tutti i flussi componenti, fornendo la lunghezza e la sequenza delle pagine per ogni flusso. Gli ordini vengono dati ai flussi consecutivamente; a partire da 0. C'è anche un flusso radice non ordinato, che contiene alcuni dei metadati.

## Riferimenti
* [PDB - Wikipedia](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

