{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Compresso", "File", "Estensione", "Formato file", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file LZO",
  "description":"Scopri il formato di file LZO e le API che possono creare e aprire file LZO.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Che cos'è un file LZO? ##

Un file con estensione .lzo è combinato con funzionalità di archiviazione dei file che possono ridurre tutte le dimensioni dei file nel file compresso. Tutti i file compressi possono comprendere uno o più file o anche gruppi di raccoglitori con più file di diverso tipo e dimensione. La dimensione di un file compresso è inferiore rispetto alla dimensione congiunta di tutti i file e le cartelle archiviati in un file compresso LZO. Tutti i file compressi LZO sono archiviati nel formato LZO e vengono eseguiti esplicitamente con le funzioni di compressione utilizzate dal software di compressione e decompressione file LZOP. Tutte le specifiche di compressione sono combinate in questo programma di compressione e decompressione file originato dalla libreria di compressione file Lempel-Ziv-Oberhume. In questi file LZO sono anche combinate velocità di decompressione più elevate e rapporti di compressione sviluppati.

## Specifica LZO ##

Markus Franz Xaver Johannes Oberhumer ha sviluppato l'originale algoritmo "lzop", basato su algoritmi precedenti di Abraham Lempel e Jacob Ziv, nel 1996. Questa libreria implementa una varietà di algoritmi con le seguenti caratteristiche:

* Compressione più veloce di DEFLATE
* Decompressione rapida
* Buffer aggiuntivi necessari durante la compressione (di 8 KB o 64 KB di dimensione, a seconda del livello di compressione)
* I buffer di origine e di destinazione sono tutta la memoria necessaria per la decompressione
* Fornisce il controllo sia del rapporto di compressione che della velocità di compressione

Come algoritmo di compressione a blocchi, LZO esegue la compressione sovrapposta e la decompressione sul posto. Per ottenere una compressione sovrapposta, la dimensione del blocco di compressione e decompressione deve corrispondere. L'algoritmo di compressione LZO divide i dati di input in corrispondenze (un dizionario scorrevole) e letterali che non corrispondono, dando buoni risultati con dati altamente ridondanti e risultati accettabili con dati non comprimibili, aumentando solo i dati incomprimibili di 1/64 dell'originale taglia.

## Problemi per aprire un file LZO ##

Di seguito sono riportati i pochi problemi che potrebbero causare un cattivo funzionamento del formato di file LZO:
  


* Il file potrebbe essere danneggiato. Per risolvere questo problema, scarica nuovamente il file o chiedi al mittente di inviare nuovamente il file
* Il secondo motivo è il file infetto in questo caso scansiona il file correttamente
* Collegamenti impropri al file LZO
* Rimozione della descrizione della LZO
* Risorse hardware insufficienti
* Driver obsoleti dell'attrezzatura
  


## Riferimenti ##

* [LZO - Di Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

