{
  "date" : "2019-10-11",
  "keywords" :[ "file gz", "formato file gz", "cos'è un file gz", "file", "esempio gz", "estensione file gz", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file GZ - File di archivio compresso GNU",
  "description":"Scopri cos'è un file GZ e le API che possono creare e aprire file GZ.",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file GZ?

Un file GZ è un archivio compresso che viene creato utilizzando l'algoritmo di compressione standard [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Può contenere più file compressi, directory e stub di file. Questo formato è stato inizialmente sviluppato per sostituire i formati di compressione sui sistemi UNIX. ed è ancora uno dei tipi di archivio più comuni sui sistemi Linux. Applicazioni come [WinZip](https://www.winzip.com/en/) possono aprire file GZ per visualizzarne il contenuto sia su Windows che su MacOS.

## Formato file GZ - Ulteriori informazioni

Gzip utilizza l'algoritmo [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) per la compressione dell'archivio e differisce dal formato di archivio [ZIP](/it/compression/zip/) nell'applicare l'algoritmo di compressione sull'archivio completo piuttosto che singoli file. Le specifiche del formato di file GZIP versione 4.3 pubblicate da Internet Engineering Task Force (IETF) contengono informazioni dettagliate sul formato del file. Il formato del file è composto da:

* Intestazione del file
* Intestazioni opzionali
* Dati compressi
* Piè di pagina del file

## Intestazione file GZ ##

L'intestazione del file GZ è composta da 10 byte come segue:

|Offset|Dimensione|Valore|Descrizione
---|---|---|---|
|0|2|0x1f 0x8b|Numero magico che identifica il tipo di file
|2|1| |Metodo di compressione * 0-7 (Riservato) * 8 (Sgonfia)
|3|1| |File Flag
|4|4| |Data e ora a 32 bit
|8|1| |Bandiere di compressione
|9|1| |ID sistema operativo

### Flag di file ###

|Valore|Identificatore|Descrizione
---|---|---|
|0x01|FTEXT|Se impostato, i dati non compressi devono essere trattati come testo anziché come dati binari. Questo flag suggerisce la conversione di fine riga per file di testo multipiattaforma ma non la impone.
|0x02|FHCRC|Il file contiene un checksum dell'intestazione (CRC-16)
|0x04|FEXTRA|Il file contiene campi extra
|0x08|FNAME|Il file contiene una stringa del nome file originale
|0x10|FCOMMENT|Il file contiene un commento
|0x20| |Riservato
|0x40| |Riservato
|0x80| |Riservato

### Sistema operativo ###

|Valore|Descrizione
---|---|
|0|File system FAT (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (o OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari TOS
|6|Filesystem HPFS (OS/2, NT)
|7|Macintosh
|8|Sistema Z
|9|PC/M
|10|TOPS-20
|11|Filesystem NTFS (NT)
|12|QDOS
|13|ghianda RISCOS
|255|sconosciuto

## Intestazioni opzionali GZ ##

Le intestazioni aggiuntive opzionali sono quelle indicate dai flag di file e includono informazioni come il nome del file originale, campi aggiuntivi, commenti e checksum dell'intestazione.

## Dati compressi ##

Questa sezione contiene i dati compressi che utilizzano l'algoritmo di compressione DEFLATE.

## Piè di pagina del file GZ ##

Il piè di pagina del file ha una dimensione di 8 byte e contiene le seguenti informazioni.

|Offset|Dimensione|Descrizione
---|---|---|
|0|4|Checksum (CRC-32)
|4|4|Valore della dimensione dei dati non compresso in byte

## Riferimenti ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: specifica del formato file GZIP](http://tools.ietf.org/html/rfc1952), di IETF.

