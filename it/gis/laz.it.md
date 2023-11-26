{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ - File di scambio dati LIDAR compresso",
  "description":"Informazioni sul formato file LAZ e sulle API in grado di creare e aprire file LAZ.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Cos'è un file LAZ?

Il formato file LAZ è una versione compressa del formato file LAS (Lidar LASer), progettato specificamente per l'archiviazione dei dati della nuvola di punti lidar. I file LAZ conservano gli stessi dati e la stessa struttura dei file LAS ma utilizzano tecniche di compressione senza perdita per ridurre le dimensioni del file preservando la fedeltà dei dati originali.

## Formato file LAZ: breve storia

Il formato file LAZ è stato sviluppato per soddisfare la crescente domanda di archiviazione e trasmissione efficienti di set di dati lidar di grandi dimensioni. Comprimendo i file LAS, i file LAZ riducono significativamente le loro dimensioni, rendendoli più facili da gestire e trasferire. La compressione viene ottenuta impiegando una combinazione di diversi algoritmi, come la codifica entropica e la codifica a lunghezza variabile, per rappresentare gli attributi dei punti lidar in una forma più compatta.

## Formato file LAZ

Nonostante la compressione, i file LAZ mantengono la capacità di ripristinare completamente i dati LAS originali senza alcuna perdita di informazioni. Ciò significa che una volta decompresso un file LAZ, può essere elaborato e analizzato allo stesso modo di un file LAS non compresso. Il processo di compressione e decompressione viene generalmente eseguito utilizzando software o librerie specializzate che supportano il formato LAZ.

Il formato file LAZ mantiene la compatibilità con i file LAS, garantendo l'interoperabilità tra software lidar e strumenti di elaborazione. Ciò significa che le applicazioni in grado di leggere ed elaborare file LAS possono in genere gestire file LAZ senza alcuna modifica. Inoltre, i file LAZ includono ancora l'intestazione del file, i record a lunghezza variabile (VLR) e i record dei dati dei punti, preservando la stessa struttura dei file LAS.

## Vantaggi del formato file LAZ

**Dimensioni file ridotte:** la compressione LAZ riduce significativamente le dimensioni dei file dei set di dati lidar, rendendoli più gestibili e più facili da archiviare e trasferire.

**Integrità dei dati:** la compressione LAZ è senza perdite, il che significa che i dati decompressi sono una replica esatta dei dati LAS originali, garantendo nessuna perdita di informazioni o precisione.

**Interoperabilità:** i file LAZ sono compatibili con i file LAS, consentendo un'integrazione perfetta con il software e i flussi di lavoro lidar esistenti.

**Elaborazione efficiente:** grazie alle loro dimensioni ridotte, i file LAZ possono essere caricati ed elaborati più rapidamente, migliorando i tempi complessivi di elaborazione e analisi.

Il formato file LAZ è stato ampiamente adottato nella comunità lidar come standard per l'archiviazione e lo scambio di dati lidar compressi. Offre un equilibrio tra compressione efficiente dei dati e integrità dei dati, consentendo una gestione più semplice di set di dati lidar di grandi dimensioni mantenendo l'accuratezza e la qualità dei dati originali.

## Riferimenti

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
