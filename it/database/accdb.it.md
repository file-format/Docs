{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "File database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file ACCDB e le API che possono creare e aprire file ACCDB.",
  "title" :"Formato file ACCDB - File di database di Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Che cos'è un file ACCDB?

Un file con estensione .accdb è un file di database di Microsoft Access 2007 che archivia i dati degli utenti in tabelle. Supporta la memorizzazione
moduli personalizzati, query SQL e altri dati. I file ACCDB hanno sostituito i file [MDB](/it/database/mdb/) dopo che Microsoft è passata alla struttura dei file basata su XML. I file ACCDB possono ancora essere convertiti in MDB con la vecchia compatibilità. Tuttavia, gli ACCDB sono attualmente il formato di file di database di Access ampiamente utilizzato. Microsoft ha anche supportato funzionalità aggiuntive in formato ACCDB come la possibilità di archiviare allegati di file, dati binari e supporto per campi multivalore.

## Formato file ACCDB

Come MDB, non sono disponibili specifiche pubbliche per il formato di file ACCDB. Microsoft supporta l'accesso a questi file in modo programmatico tramite lo standard ODBC (Open Database Connectivity) e Visual Basic, Applications Edition (VBA).

### Un'intuizione

Un dump esadecimale di un semplice file ACCDB suggerisce che ci sono somiglianze generali nella struttura con le ultime versioni della precedente famiglia di formati MDB. Entrambi i formati di file utilizzano dimensioni di pagina fisse di 4096 byte. Un'altra somiglianza tra ACCDB e MDB è la forma del numero magico, che include la stringa "Standard ACE DB" per ACCDB. Una versione o un codice di compatibilità si trova nella stessa posizione in entrambi i formati. Gli strumenti mdb | Il file HACKING indica "L'offset 0x14 contiene la versione Jet di questo database" e la guida MDB non ufficiale concorda. Le informazioni in queste fonti, combinate con la voce di Wikipedia per [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), suggeriscono che un valore di 0x02 indica ACE 12 (Access 2007) e 0x03 indica ACE 14 (Accesso 2010). Tuttavia, un database minimo creato in Access 2010 e uno simile creato in Access 2016 hanno entrambi 0x02 in questa posizione. Un database minimo creato in Access 2016, ma che definisce una colonna con il tipo di dati "numero intero" introdotto di recente, aveva un valore di 0x05. Nei file ACCDB, questo indicatore sembra riflettere la compatibilità del file anziché la versione del motore ACE utilizzato per crearlo.

## Riferimenti

* [Specifiche di accesso 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Motore di database Microsoft Jet](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Quale formato di file di Access dovrei usare?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)
