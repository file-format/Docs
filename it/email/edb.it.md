{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file EDB - Un file di database di posta di Exchange",
  "description":"Scopri il formato di file EDB e le API che possono creare e aprire file EDB.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## Che cos'è un file EDB?

Un file con estensione .edb è un database delle cassette postali creato da Microsoft Exchange Server per archiviare i dati relativi alla posta. EDB, Exchange Database, archivia i messaggi in corso e non SMTP. Gli EDB sono anche noti come file di database Extensible Storage Engine (ESE) e archiviano i file utilizzando la struttura b-tree. Essendo file di archiviazione, i file EDB possono essere convertiti in altri formati di file di archiviazione della posta come [PST](/it/email/pst/) e [OST](/it/email/ost/).

## Formato file EDB

Non sono disponibili specifiche del formato di file EDB ufficiali/aperte a cui è possibile fare riferimento. Sono stati compiuti alcuni progressi per il reverse engineering del formato del file, con conseguente parziale decodifica delle specifiche. Come per questi, un file EDB è composto da:
* Intestazione file: contiene le informazioni sull'intestazione del file di database
* Pagine a dimensione fissa - Contiene il database che consiste di tabelle e indici

### Intestazione del file di database
L'intestazione del file di database risiede nella prima pagina del database ed è di almeno 668 byte. L'intestazione del file contiene "Versione formato file" e "Tipo file" oltre ad altri campi.

#### Tipi di file
|Tipo|Descrizione
---|---|
|0| Banca dati|
|1| streaming|

`Nota:` Gli identificatori per questi tipi non sono noti.

#### Versione formato file
Il formato originale di EDB è iniziato nell'aprile 1997 e ha continuato a evolversi per le modifiche successive.

|Data di revisione|Versione|Revisione|descrizione
---|---|---|---|
|aprile 1997| 0x00000620|0x00000000| Sistema operativo originale in formato Beta.|
|Maggio 1997 |0x00000620|0x00000001| Aggiungi colonne nel catalogo per l'indicizzazione condizionale e OLD.|
|giugno 1997|0x00000620|0x00000002|Aggiungi il flag fLocalizedText in IDB.|
|Ottobre 1997|0x00000620|0x00000003|Aggiungi SPLIT_BUFFER alle pagine radice dell'albero spaziale.|
|Gen 1998|0x00000620|0x00000002|Ripristina la revisione in modo che ESE97 rimanga compatibile con le versioni successive.|
||0x00000620|0x00000003|Aggiungi nuove colonne con tag al catalogo ("CallbackData" e "CallbackDependencies").|
|Maggio 1998|0x00000620|0x00000004|Supporto Super Long Value (SLV): signSLV, fSLVEsiste in dbheader.|
|Maggio 1998|0x00000620|0x00000005|Nuovo albero spaziale SLV.|
|Ottobre 1998|0x00000620|0x00000006|Mappa spaziale SLV.|
|Dic 1998|0x00000620|0x00000007|IDXSEG a 4 byte.|
|Gen 1999|0x00000620|0x00000008|Nuovo formato colonna modello.|
|giugno 1999|0x00000620|0x00000009|Colonne modello ordinate. Utilizzato in Windows XP SP3|
||0x00000620|0x0000000b|Contiene l'intestazione della pagina con il checksum ECCUsed in Exchange|
||0x00000620|0x0000000c|Utilizzato in Windows Vista (SP0)|
||0x00000620|0x00000011|Supporto per pagine da 2 KiB, 16 KiB e 32 KiB.Intestazione pagina estesa con checksum ECC aggiuntivi.Compressione colonna.Suggerimenti per lo spazio.Utilizzato in Windows 7 (SP0)|
|Maggio 1999|0x00000623|0x00000000|Nuovo Space Manager.|

### File di database

Il file di database EDB contiene lo schema per tutte le tabelle nel database. Inoltre, include anche i record per tutte le tabelle del database e gli indici per le tabelle. La sua posizione è determinata dai seguenti identificatori.

* JetCreateDatabase
* JetCreateDatabase2
* JetAttachDatabase
* JetAttachDatabase2

Sulla base di questi, lo stato del database può essere valutato come segue.

|Valore|Identificatore|Descrizione
---|---|---|
|1|JET_dbstateJustCreated|Il database è stato appena creato.|
|2|JET_dbstateDirtyShutdown|Il database richiede un ripristino hardware o software per essere eseguito per diventare utilizzabile o mobile. Non si dovrebbe provare a spostare i database in questo stato.|
|3|JET_dbstateCleanShutdown|Il database è in uno stato pulito. Il database può essere allegato senza alcun file di registro.|
|4|JET_dbstateBeingConverted|Il database è in fase di aggiornamento.|
|5|JET_dbstateForceDetachInternal|Questo valore è introdotto in WindowsXP|
 

## Riferimenti
* [Specifiche del file di database (EDB) di Extensible Storage Engine (ESE)](https://github.com/libyal/libesedb/tree/main/documentation)

