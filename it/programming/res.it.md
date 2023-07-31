{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - Script di risorse compilato in C++",
  "description":"Scopri il formato di file RES con l'esempio RES e le API che possono creare e aprire file RES.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Che cos'è un file RES?
Il file con suffisso o estensione .res può appartenere a molte categorie di formati di file. Qui stiamo discutendo del formato di file RES che è uno script di risorse compilato C++; un file binario creato dal Microsoft Resource Compiler (rc) che contiene i dati delle risorse; in base al contenuto del file di definizione delle risorse; rilevante per il suo progetto software padre. Il file .res di solito viene riformattato in un file oggetto risorsa per collegarlo al file eseguibile di un'applicazione.

## Formato file RES
Il formato di file RES appartiene a Microsoft Resource Compiler (rc). Il compilatore di risorse è uno strumento che compila risorse come cursori, icone, menu e finestre di dialogo utilizzate dall'applicazione. I file di risorse di solito hanno un'estensione .res; contiene risorse, come cursori, immagini e informazioni sulla versione. Un file RES potrebbe essere un file di risorse a 16 o 32 bit.
## Struttura del file di risorse
Un file di risorse contiene una serie di varie voci di risorse. Ogni voce contiene un'intestazione di risorsa e dati rilevanti. Un'intestazione di risorsa è generalmente allineata DWORD nel file e contiene quanto segue:

- Una **DWORD** per specificare la dimensione dell'intestazione della risorsa
- Una **DWORD** per specificare la dimensione dei dati della risorsa
- Il tipo di risorsa
- Il nome della risorsa
- Ulteriori informazioni sulle risorse

La struttura dell'intestazione della risorsa definisce il formato del file RES. I dati per la risorsa seguono l'intestazione della risorsa. Alcune risorse aggiungono anche un modello di intestazione di gruppo specifico della risorsa per fornire informazioni su un gruppo di risorse. Di seguito sono riportati alcuni dei tipi di voci delle risorse e la loro descrizione:

### Risorse della tabella dell'acceleratore
Una tabella acceleratore è una voce di risorsa in un file RES senza un'intestazione di gruppo. Il pattern **ACCELTABLEENTRY** definisce ogni voce nella tabella dell'acceleratore. Un file RES può avere più tabelle di accelerazione.

### Risorse per il cursore e l'icona
Sebbene, il sistema consideri ogni icona e cursore come un singolo file, ma questi sono archiviati nei file RES come un gruppo di risorse icona o un gruppo di risorse cursore. I formati di file delle risorse dell'icona e del cursore sono gli stessi. Un'intestazione di gruppo di risorse segue tutti i componenti di singole icone o gruppi di cursori nel file .res.

### Risorse della finestra di dialogo
Viene realizzata anche una finestra di dialogo come voce di risorsa nel file RES. Contiene un modello di intestazione della finestra di dialogo **DLGTEMPLATE** e un modello **DLGITEMTEMPLATE** per ogni controllo specifico nella finestra di dialogo. I modelli **DLGTEMPLATEEX** e **DLGITEMTEMPLATEEX** spiegano il formato delle risorse della finestra di dialogo estesa.

### Risorse sui caratteri
Una risorsa di menu contiene un modello **MENUHEADER** successivamente uno o più modelli **NORMALMENUITEM** o **POPUPMENUITEM**, uno per ciascuna voce di menu nel modello di menu. I modelli **MENUEX_TEMPLATE_HEADER** e **MENUEX_TEMPLATE_ITEM** spiegano il formato delle risorse di menu estese.

### Risorse della tabella dei messaggi
Una tabella dei messaggi è costituita da testo formattato da visualizzare come messaggio di errore o in una finestra di messaggio. Il modello principale in una risorsa tabella messaggi è la struttura **MESSAGE_RESOURCE_DATA**.

### Risorse della versione
Il modello principale in una risorsa di versione è **VS_FIXEDFILEINFO**. Ulteriori modelli includono **VarFileInfo** per archiviare i dati relativi alle informazioni sulla lingua e **StringFileInfo** per informazioni sulle stringhe personalizzate.




## Riferimenti

* [Formati file di risorse](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



