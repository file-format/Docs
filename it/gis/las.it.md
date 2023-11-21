{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS - Formato file Lidar LASer",
  "description":"Ulteriori informazioni sul formato file LAS e sulle API in grado di creare e aprire file LAS.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Cos'è un file LAS?

Il formato file LAS (Lidar LASer) è un formato file binario progettato specificamente per l'archiviazione dei dati della nuvola di punti lidar. È stato sviluppato ed è gestito dall'American Society for Photogrammetry and Remote Sensing (ASPRS) come formato standardizzato per lo scambio di dati lidar e l'interoperabilità.

I file LAS memorizzano informazioni dettagliate sui singoli punti lidar, comprese le loro coordinate 3D (x, y e z), valori di intensità, codici di classificazione e attributi aggiuntivi. Il formato supporta sia i dati lidar con ritorno discreto che con forma d'onda completa, consentendo la memorizzazione di più ritorni per impulso laser.

## Formato file LAS

La struttura di un file LAS è composta da tre sezioni principali: l'intestazione del file, i record a lunghezza variabile (VLR) e i record dei dati dei punti.

1. Intestazione del file: l'intestazione del file contiene informazioni essenziali sul file LAS, come la versione del formato dei dati, il formato dei dati dei punti, il numero di punti, le coordinate del riquadro di delimitazione, il sistema di riferimento delle coordinate (CRS) e altri metadati. Fornisce un riepilogo dei dati lidar contenuti nel file.

2. Record a lunghezza variabile (VLR): i VLR sono facoltativi e possono memorizzare metadati aggiuntivi e informazioni personalizzate sui dati lidar. I VLR consentono flessibilità nell'estensione del formato per soddisfare le esigenze specifiche dell'utente. Esempi di VLR includono informazioni sul sistema di sensori, parametri di elaborazione dei dati o schemi di classificazione.

3. Record di dati di punto: i record di dati di punto memorizzano le misurazioni lidar effettive. Ogni record di dati di punti rappresenta un singolo punto lidar e contiene attributi come coordinate x, yez, valori di intensità, codici di classificazione (ad esempio terreno, vegetazione, edifici) e altri attributi definiti dall'utente. I record dei punti possono anche memorizzare timestamp, conteggi restituiti e angoli di scansione.

I file LAS supportano diversi formati di dati (da 0 a 10) per accogliere vari tipi di dati lidar e il livello di informazioni necessarie. Ad esempio, il formato 0 rappresenta un formato punto semplice con informazioni di base, mentre i formati da 1 a 3 forniscono dati più completi, comprese le informazioni sulla forma d'onda per ciascun ritorno.

I file LAS sono ampiamente supportati dal software lidar e dagli strumenti di elaborazione, rendendoli un formato standard per lo scambio e l'analisi dei dati lidar. Inoltre, i file LAS possono essere compressi utilizzando tecniche di compressione senza perdita di dati per ridurre le dimensioni del file preservando la fedeltà dei dati originali. La versione compressa dei file LAS viene spesso definita LAZ e offre efficienti funzionalità di archiviazione e trasferimento dati.

## Riferimenti

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
