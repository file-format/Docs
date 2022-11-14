{
  "date" : "2021-04-08",
  "keywords" :[ "file dar", "formato file dar", "cos'è un file dar", "file", "esempio dar", "estensione file dar", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Formato file archivio disco",
  "description":"Scopri il formato di file DAR e le API che possono creare e aprire file DAR.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Che cos'è un file DAR?

Un file con estensione .dar è un archivio compresso creato utilizzando l'archivio del disco DAR. Può creare backup/archivio per l'intero disco o un gruppo di file. È stato creato per sostituire il formato di file [TAR](/it/compression/tar/) sul sistema operativo UNIX e può essere creato come file di archivio diviso per un numero elevato di file. L'archivio DAR supporta l'opzione di eliminazione dei file dal sistema che sono collegati ai file principali nell'archivio. Le sue capacità di fornire backup differenziale, incrementale e decrementale lo rendono superiore ai file TAR.

## Formato file DAR

I file DAR sono archivi compressi che possono utilizzare qualsiasi compressione per file come [gzip](/it/compression/gz/), [bzip2](/it/compression/bz2/), lzo, xz o lzma. Il formato file esatto di un file DAR dipende dal tipo di formattazione utilizzato per comprimere il contenuto dell'archivio. Consente inoltre la crittografia opzionale Blowfish, Twofish, AES, Serpent, Camellia e crittografia e firma a chiave pubblica (OpenPGP).

### Caratteristiche DAR

Alcune delle caratteristiche del formato file DAR sono le seguenti.

* Si prende cura di qualsiasi tipo di inode (directory, file semplici, collegamenti simbolici, dispositivi speciali, named pipe, socket, porte, ...)
* Si prende cura degli inode collegati (file semplici collegati, dispositivi char, dispositivi a blocchi, collegamenti simbolici collegati)
* Si prende cura dei file sparsi
* Si occupa degli attributi estesi dei file Linux,
* Si occupa del file ACL di Linux
* Si prende cura dei fork dei file di Mac OS X
* Si prende cura di alcuni attributi specifici del filesystem come la data di nascita del filesystem HFS+ e gli attributi immutabili, data-journaling, secure-deletion, no-tail-merging, undeletable, noatime del filesystem ext2/3/4.
* Compressione per file con gzip, bzip2, lzo, xz o lzma (invece di comprimere l'intero archivio). Un individuo può scegliere di non comprimere file già compressi in base al suffisso del nome file.
* Estrazione rapida di file da qualsiasi punto dell'archivio
* Elenco veloce dei contenuti dell'archivio salvando il catalogo dei file nell'archivio
* Backup del filesystem in tempo reale: rileva quando un file è stato modificato mentre era letto per il backup e può riprovare a salvarlo fino a un determinato numero massimo di tentativi
* File hash (MD5, SHA1 o SHA-512) generato al volo per ogni fetta, il file risultante è compatibile con md5sum o sha1sum, per poter controllare rapidamente l'integrità di ogni fetta
* Indipendente dal filesystem: può essere utilizzato per ripristinare un sistema su una partizione di dimensioni diverse e/o su una partizione con un filesystem diverso[5]

## Riferimenti

* [DAR](http://dar.linux.free.fr/)
* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

