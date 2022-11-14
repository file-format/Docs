{
  "date" : "2019-11-25",
  "keywords" :[ "file jpeg", "formato file jpeg", "cos'è un file jpeg", "file", "esempio jpeg", "estensione file jpeg", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - Formato file immagine",
  "description":"Scopri il formato di file JPEG e le API che possono creare e aprire file JPEG.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## Che cos'è un file JPEG? ##

Un JPEG è un tipo di formato immagine che viene salvato utilizzando il metodo di compressione con perdita di dati. L'immagine di output, come risultato della compressione, è un compromesso tra la dimensione della memoria e la qualità dell'immagine. Gli utenti possono regolare il livello di compressione per ottenere il livello di qualità desiderato riducendo allo stesso tempo le dimensioni dello storage. La qualità dell'immagine viene influenzata in modo trascurabile se all'immagine viene applicata la compressione 10:1. Maggiore è il valore di compressione, maggiore è il degrado della qualità dell'immagine.

## Specifiche del formato file ##

Il formato del file immagine JPEG è stato standardizzato dal Joint Photographic Experts Group e, da qui, il nome JPEG. Il formato è stato la scelta di archiviare e trasmettere immagini fotografiche sul web. Quasi tutti i sistemi operativi ora dispongono di visualizzatori che supportano la visualizzazione di immagini JPEG, che spesso vengono archiviate anche con estensione JPG. Anche i browser web supportano la visualizzazione di immagini JPEG. Prima di entrare nelle specifiche del formato di file JPEG, è necessario menzionare il processo complessivo dei passaggi coinvolti nella creazione di JPEG.

### Passaggi di compressione JPEG ###

**Trasformazione:** Le immagini a colori vengono trasformate da RGB in un'immagine di luminanza/crominanza (l'occhio è sensibile alla luminanza, non alla crominanza, quindi la parte di crominanza può perdere molti dati e quindi può essere altamente compressa.

**Campionamento verso il basso:** Il campionamento verso il basso viene eseguito per la componente colorata e non per la componente di luminanza. Il campionamento verso il basso viene eseguito con un rapporto 2:1 in orizzontale e 1:1 in verticale (2h 1 V). Pertanto, l'immagine si riduce di dimensioni poiché il componente 'y' non viene toccato, non si verifica una notevole perdita di qualità dell'immagine.

**Organizzazione in gruppi:** I pixel di ogni componente colore sono organizzati in gruppi di 8×2 pixel chiamati “unità dati” se il numero di righe o colonne non è un multiplo di 8, la riga inferiore e le colonne più a destra vengono duplicate.

**Trasformazione del coseno discreta:** La trasformazione del coseno discreta (DCT) viene quindi applicata a ciascuna unità di dati per creare una mappa 8×8 dei componenti trasformati. La DCT comporta una certa perdita di informazioni a causa della precisione limitata dell'aritmetica del computer. Ciò significa che anche senza la mappa ci sarà una perdita di qualità dell'immagine, ma normalmente è piccola.

**Quantizzazione:** Ciascuno dei 64 componenti trasformati nell'unità di dati viene diviso per un numero separato chiamato "Coefficiente di quantizzazione (QC)" e quindi arrotondato a un numero intero. È qui che le informazioni vengono perse irrimediabilmente, il controllo di qualità grande causa maggiori perdite. In generale, la maggior parte delle implementazioni JPEG consente l'uso di tabelle QC consigliate dallo standard JPEG.

**Codifica:** I 64 coefficienti trasformati quantizzati (che ora sono interi) di ciascuna unità di dati sono codificati utilizzando una combinazione di codifica RLE e Huffman.

**Aggiunta di intestazione:** L'ultimo passaggio aggiunge l'intestazione e tutti i parametri JPEG utilizzati e genera il risultato.

Il decodificatore JPEG utilizza i passaggi al contrario per generare l'immagine originale da quella compressa.

### Struttura del file ###

Un'immagine JPEG è rappresentata come una sequenza di segmenti in cui ogni segmento inizia con un marcatore. Ogni indicatore inizia con 0xFF byte seguito da un contrassegno dell'indicatore per rappresentare il tipo di indicatore. Il carico utile seguito da marker è diverso a seconda del tipo di marker. I tipi comuni di marcatori JPEG sono elencati di seguito:

|Nome breve|Byte|Carico utile|Nome|Commenti
---|---|---|---|---|
|SOI|0xFF, 0xD8|nessuno|Inizio dell'immagine|
|S0F0|0xFF, 0xC0|dimensione variabile|Inizio frame|
|S0F2|0xFF, 0xC2|dimensione variabile|Inizio per frame|
|DHT|0xFF, 0xC4|dimensione variabile|Definisci tabelle di Huffman|
|DQT|0xFF, 0xDB|dimensione variabile|Definisci tabelle di quantizzazione|
|DRI|0xFF, 0xDD|4 byte|Definisci intervallo di riavvio|
|SOS|0xFF, 0xDA|dimensione variabile|Inizio scansione|
|RSTn|0xFF, 0xD//n//(/it//n//#0..7)|nessuno|Riavvia|
|APPn|0xFF, 0xE//n//|dimensione variabile|Specifico dell'applicazione|
|COM|0xFF, 0xFE|dimensione variabile|Commento|
|EOI|0xFF, 0xD9|nessuno|Fine immagine|

All'interno dei dati codificati entropia, dopo qualsiasi byte 0xFF, l'encoder inserisce un byte 0x00 prima del byte successivo, in modo che non sembri esserci un marker dove non è previsto, prevenendo errori di framing. I decodificatori devono saltare questo byte 0x00. Questa tecnica, chiamata [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (vedi la sezione delle specifiche JPEG F.1.2.3), viene applicata solo ai dati codificati entropia, non ai dati del carico utile del marker . Si noti tuttavia che i dati codificati entropia hanno alcuni indicatori propri; in particolare i marcatori di ripristino (da 0xD0 a 0xD7), che vengono utilizzati per isolare blocchi indipendenti di dati codificati entropia per consentire la decodifica parallela, e i codificatori sono liberi di inserire questi marcatori di ripristino a intervalli regolari (sebbene non tutti i codificatori lo facciano).

