{
"data":"2023-07-18",
   "keywords":[
"PAR",
"File PAR",
"come aprire un file par",
"file",
"Estensione file PAR",
"estensione",
"file"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file PAR - File indice Parchive",
   "description":"Ulteriori informazioni sul formato PAR e sulle API in grado di creare e aprire file PAR.",
"linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
"parent" : "compression"
}
},
"lastmod":"2023-07-18"
}

## Cos'è un file PAR?

All'interno degli archivi Parchive (PAR), un file .par fa riferimento a un file di indice che contiene un gruppo di volumi di parità o blocchi di parità. Questo file di indice viene utilizzato per il rilevamento degli errori e il ripristino quando uno o più file nell'archivio vengono persi o danneggiati.

Un archivio Parchive è tipicamente costituito sia dai file di dati originali che dai corrispondenti volumi di parità. I volumi di parità vengono creati utilizzando algoritmi di correzione degli errori Reed-Solomon. Questi volumi di parità contengono informazioni ridondanti che possono essere utilizzate per ripristinare i file di dati originali.

Il file .par, noto anche come set di volumi di parità, contiene informazioni sulla struttura e sulla posizione dei volumi di parità all'interno dell'archivio. Serve come indice o mappa per il processo di recupero. Utilizzando il file .par, un software PAR specializzato può determinare quali volumi di parità sono necessari e come dovrebbero essere utilizzati per ricostruire i file mancanti o danneggiati.

Quando uno o più file all'interno dell'archivio Parchive diventano inaccessibili o danneggiati, il file .par può essere utilizzato insieme ai volumi di parità disponibili per recuperare i dati persi. Il software PAR legge il file .par, identifica i file mancanti o danneggiati e utilizza i volumi di parità per ricostruirli.

## Come aprire un file PAR?

Per aprire e utilizzare i file .par, avrai bisogno di un software PAR specializzato. Ecco alcune opzioni software popolari in grado di gestire i file .par:

- **QuickPar:** QuickPar è un software PAR ampiamente utilizzato per Windows. Ti consente di creare, verificare e riparare file PAR. Puoi aprire un file .par in QuickPar per verificarne l'integrità o utilizzarlo per riparare file danneggiati o mancanti in un archivio Parchive.

- **MultiPar:** MultiPar è un altro popolare software PAR disponibile per Windows. Supporta i formati di file PAR e PAR2 e fornisce funzionalità avanzate per la creazione, la verifica e la riparazione degli archivi. MultiPar può aprire file .par ed eseguire operazioni di rilevamento e ripristino degli errori in base ai volumi di parità forniti.

- **MacPAR deLuxe:** MacPAR deLuxe è un software PAR progettato specificamente per macOS. Supporta i formati di file PAR e PAR2 e fornisce funzionalità simili a QuickPar e MultiPar. MacPAR deLuxe può aprire file .par e assistere nella verifica degli archivi e nel recupero di file danneggiati o mancanti.

## Formato file PAR: ulteriori informazioni

Il formato file PAR, comunemente indicato come Parchive, è un formato file specifico utilizzato per creare dati di parità ed eseguire il rilevamento e il ripristino degli errori negli archivi di file. Il formato file PAR è generalmente costituito da tre tipi: PAR, PAR2 e PAR3.

- **PAR:** Il formato file PAR originale, noto anche come PAR1, è stato sviluppato dal progetto Parchive. Include i dati di parità generati dai file di dati originali. I file PAR forniscono un livello base di rilevamento e ripristino degli errori, ma presentano limitazioni in termini di capacità di correzione degli errori.

- **PAR2:** PAR2 è una versione migliorata del formato file PAR. Offre funzionalità di correzione degli errori più avanzate e funzionalità di ripristino avanzate. I file PAR2 vengono generalmente utilizzati per creare dati di parità in grado di recuperare file persi o danneggiati all'interno di un archivio. I file PAR2 forniscono una migliore protezione contro la corruzione dei dati e sono ampiamente utilizzati per scopi di archiviazione dei file.

- **PAR3:** PAR3 è l'ultima versione del formato file PAR e fornisce ulteriori miglioramenti nella correzione e nel ripristino degli errori. Offre livelli ancora più elevati di ridondanza e funzionalità di correzione degli errori rispetto a PAR2. I file PAR3 sono progettati per fornire opzioni di protezione e ripristino più solide per i dati archiviati negli archivi.

Entrambi i formati di file PAR2 e PAR3 sono ampiamente supportati dal software PAR e offrono la possibilità di verificare l'integrità dei file all'interno di un archivio e recuperare dati persi o danneggiati. I file PAR e PAR2 sono ancora comunemente utilizzati, mentre i file PAR3 stanno gradualmente guadagnando adozione grazie alle loro capacità avanzate di correzione degli errori.

## Riferimenti
* [Parchive](https://en.wikipedia.org/wiki/Parchive)

