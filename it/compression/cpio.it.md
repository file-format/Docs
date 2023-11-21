{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File CPIO - Formato file di archivio CPIO Unix",
  "description":"Scopri cosa è un file CPIO e le API che possono creare e aprire file CPIO.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Cos'è un file CPIO?

Un file CPIO è un file di archivio creato nel formato CPIO (Copy In Copy Out) di Unix. È simile al formato file TAR, tranne per il fatto che non è compresso. I file CPIO possono memorizzare file del dispositivo, collegamenti simbolici e attributi di file estesi.

## Formato file CPIO

Un archivio CPIO viene creato come file binario non leggibile dall'uomo. Memorizza la raccolta di file e directory. Il contenuto di un archivio CPIO è identificato con informazioni di metadati quali nomi di file, autorizzazioni, proprietà e timestamp. Queste informazioni sui metadati vengono anche archiviate nel file di archivio per l'accesso laterale da parte del sistema.

## Formato dell'archivio CPIO

Un file CPIO è composto da uno o più file membro concatenati. Ogni file nell'archivio è costituito da un'intestazione seguita facoltativamente dal contenuto del file come indicato nell'intestazione. L'archivio contiene un'altra intestazione alla fine che è descritta da un file vuoto chiamato TRAILER!!.

### Tipi di archivi CPIO

Esistono due tipi di archivi CPIO. Questi differiscono solo nello stile dell'intestazione.

* Archivi ASCII: questi archivi CPIO hanno un'intestazione stampabile che diventa parte dell'archivio CPIO se l'archivio stesso è costituito da file ASCII
* Archivi binari: questi archivi CPIO hanno intestazioni binarie.

## Lavorare con l'archivio CPIO

### Come creare archivi CPIO?

È possibile creare un CPIO su sistemi simili a Unix utilizzando il comando **cpio**. Il seguente comando troverà tutti i file e le directory nella directory corrente e nelle sue sottodirectory. Questo output viene quindi reindirizzato al comando cpio che genererà un nuovo archivio CPIO denominato archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Come estrarre file dagli archivi CPIO?

Il comando seguente estrae i file da un archivio esistente.

```
cpio -id < archive_cpio.cpio
```
Leggerà il file archive.cpio dallo standard input ed estrarrà i file nella directory corrente.


## Riferimenti

* [CPIO - Da Wikipedia](https://en.wikipedia.org/wiki/Cpio)
* [Formato file CPIO](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

