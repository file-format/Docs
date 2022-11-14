{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "File database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file NSF e le API che possono creare e aprire file NSF.",
  "title" :"Formato file NSF - Formato database Lotus Notes",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Che cos'è un file NSF?

Un file con estensione .nsf (Notes Storage Facility) è un formato di file di database utilizzato dal [software IBM Notes](https://en.wikipedia.org/wiki/HCL_Domino), precedentemente noto come Lotus Notes. Definisce lo schema per memorizzare diversi tipi di oggetti come e-mail, appuntamenti, documenti, moduli e viste. Tutte queste informazioni sono contenute in un unico file NSF per la collaborazione aziendale simile a un file PST/OST. Alcune delle applicazioni che possono aprire file NSF includono IBM Lotus Notes e IBM Domino.

## Specifiche del formato file NSF

I file NSF sono di natura binaria e le loro specifiche sono disponibili da Joachim Metz su [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database% 20file%20format.asciidoc). Secondo questi dettagli, un file NSF comprende:

* Intestazione del file
* Intestazione del database

Inoltre, è composto da:

* Superblocco
* Blocco descrittore del secchio
* Bitmap
* Secchio di vettore di trasferimento dei record
* Secchi di riepilogo
* Secchi non di riepilogo


### Intestazione del file NSF

L'intestazione del file NSF ha una dimensione di 6 byte. Esso consiste in:

|Offset|Dimensione|Valore|Descrizione|
---|---|---|---|
0|2|0x1a 0x00|Firma|
2|4| |La dimensione dell'intestazione del database|

### Intestazione del database

L'intestazione del database NSD contiene i seguenti valori confermati.

* Informazioni sul database
* Identificatore database (DBID)
* Informazioni sulla replica
* Flag del buffer delle informazioni del database
* Titolo
* Categorie
* Classe
* Classe di design (nome modello)
* Identificatori di note speciali
* Imbottitura
* Informazioni sul database 2
* Informazioni sul database 3
* Informazioni sul database 4
* Informazioni sul database 5
* Imbottitura
* Identificatore dell'istanza del database (DBIID)
* Cronologia della replica

## Riferimenti

* [Formato NSF - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

