{
  "date" : "2019-10-11",
  "keywords" :[ "file tar", "formato file tar", "cos'è un file tar", "file", "esempio tar", "estensione file tar", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Formato file di archivio Unix",
  "description":"Scopri cos'è un file Tar e le API che possono creare e aprire file TAR.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file TAR?

I file con estensione .tar sono archivi creati con l'utilità basata su Unix per la raccolta di uno o più file. Più file vengono archiviati in un formato non compresso con il supporto dell'aggiunta di file e cartelle all'archivio. L'utilità TAR su Unix è basata su comandi, ma i file così creati sono supportati dalla maggior parte dei sistemi di archiviazione file su quasi tutti i sistemi operativi. È stato creato per la prima volta nel 1979 dagli AT&T Bell Laboratories e le versioni successive sono state pubblicate con il passare del tempo.

## Formato file TAR

TAR è un formato di file aperto con specifiche complete disponibili come riferimento per gli sviluppatori. La sua struttura di file è stata standardizzata in POSIX.1-1988 e successivamente in POSIX.1-2001. I set di dati creati da tar conservano informazioni sui parametri del file system come:

* Nome
* Timbri temporali
* Proprietà
* Permessi di accesso ai file
* Organizzazione della directory

Un file Tar non ha alcun numero magico. Contiene una serie di blocchi in cui ogni blocco è di byte BLOCKSIZE.

Ogni file archiviato è rappresentato da un blocco di intestazione che descrive il file, seguito da zero o più blocchi che danno il contenuto del file. Alla fine del file di archivio ci sono due blocchi da 512 byte riempiti con zeri binari come indicatore di fine file. Un sistema ragionevole dovrebbe scrivere tale marcatore di fine file alla fine di un archivio, ma non deve presumere che tale blocco esista durante la lettura di un archivio. In particolare GNU tar emette sempre un avviso se non lo incontra.

I blocchi possono essere bloccati per operazioni di I/O fisiche. Ogni record di n blocchi (dove n è impostato dall'opzione blocking-factor = 512-size su tar) viene scritto con una singola operazione "write()". Su nastri magnetici, il risultato di tale scrittura è un singolo record. Quando si scrive un archivio, l'ultimo record di blocchi deve essere scritto a dimensione intera, con i blocchi dopo lo zero che contengono tutti zeri. Durante la lettura di un archivio, un sistema ragionevole dovrebbe gestire correttamente un archivio il cui ultimo record è più breve del resto o che contiene record spazzatura dopo un blocco zero.

### Intestazione catrame

Come qualsiasi altra intestazione di file, il record di intestazione del file tar contiene metadati su un file ed è mostrato nella tabella seguente.


|Offset campo|Dimensioni campo (byte)|Campo
---|---|---|
|0|100|Nome del file
|100|8|Modalità file
|108|8|ID utente numerico del proprietario
|116|8|ID utente numerico del gruppo
|124|12|Dimensione del file in byte (base ottale)
|136|12|Ora dell'ultima modifica in formato numerico Unix (ottale)
|148|8|Somma di controllo per il record di intestazione
|156|1|Indicatore di collegamento (tipo di file)
|157|100|Nome del file collegato

I campi inutilizzati vengono riempiti con byte NUL. Un'intestazione comprende 257 byte che viene riempita con byte NUL per riempirla fino a un record di 512 byte.

## Riferimenti ##

* [TAR - Di Wikipedia](https://en.wikipedia.org/wiki/Tar_(computing))
* [Formato di base TAR](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

