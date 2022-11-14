{
  "date" : "2019-10-11",
  "keywords" :["file psd", "formato file psd", "cos'è un file psd", "file", "esempio psd", "estensione file psd", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - Formato file immagine Photoshop",
  "description":"Scopri il formato di file PSD e le API che possono creare e aprire file PSD.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file PSD?

PSD, Photoshop Document, rappresenta il formato di file nativo di Adobe Photoshop utilizzato per la progettazione e lo sviluppo della grafica. I file PSD possono includere livelli di immagine, livelli di regolazione, maschere di livello, annotazioni, informazioni sui file, parole chiave e altri elementi specifici di Photoshop. I file di Photoshop hanno un'estensione predefinita come .PSD e hanno un'altezza e una larghezza massime di 30.000 pixel e un limite di lunghezza di due gigabyte.

## Specifiche del formato file PSD ##

I dati in un file PSD vengono archiviati in ordine di byte big endian. Ciò implica lo scambio degli interi short e long durante la lettura o la scrittura su piattaforma Windows. Il formato del file di Photoshop è diviso in cinque parti principali. Ha molti indicatori di lunghezza che possono essere utilizzati per spostarsi da una sezione all'altra. Gli indicatori di lunghezza sono generalmente riempiti di byte da arrotondare all'intervallo di 2 o 4 byte più vicino. Le cinque parti principali sono:

* Intestazione del file
* Dati modalità colore
* Risorse di immagine
* Informazioni su livelli e maschere
* Dati immagine

Per conformità, i dati dovrebbero essere scritti in tutti questi campi della sezione, poiché Photoshop potrebbe provare a leggere l'intera sezione. Implica anche che gli zeri vengano scritti nei campi ignorati durante la scrittura su un file. Il campo della lunghezza nelle sezioni delimitate dalla lunghezza dovrebbe essere utilizzato per decidere quando interrompere la lettura. Nella maggior parte dei casi, il campo della lunghezza indica il numero di byte, non di record, che seguono. I seguenti punti devono essere ricordati durante la lettura di un file.

* I valori nella colonna "Lunghezza" in tutte le tabelle sono in byte.
* Tutti i valori definiti come stringa Unicode sono costituiti da:
* Un campo di 4 byte, che rappresenta il numero di caratteri nella stringa (non byte).
* La stringa di valori Unicode, due byte per carattere.

### Intestazione del file ###

L'intestazione del file contiene le proprietà di base dell'immagine.

|Lunghezza|Descrizione
---|---|
|4|Firma: sempre uguale a '8BPS' . Non tentare di leggere il file se la firma non corrisponde a questo valore.
|2|Versione: sempre uguale a 1. Non provare a leggere il file se la versione non corrisponde a questo valore. (~*~*PSB~*~* la versione è 2.)
|6|Riservato: deve essere zero.
|2|Il numero di canali nell'immagine, inclusi eventuali canali alfa. L'intervallo supportato è compreso tra 1 e 56.
|4|L'altezza dell'immagine in pixel. L'intervallo supportato è compreso tra 1 e 30.000.
|4|La larghezza dell'immagine in pixel. L'intervallo supportato è compreso tra 1 e 30.000.
|2|Profondità: il numero di bit per canale. I valori supportati sono 1, 8, 16 e 32.
|2|La modalità colore del file. I valori supportati sono: Bitmap # 0; Scala di grigi n. 1; Indicizzato # 2; RGB # 3; CMYK # 4; Multicanale # 7; Bicromia # 8; Laboratorio n. 9.

### Sezione dati modalità colore ###

La sezione dei dati della modalità colore è strutturata come segue:


|Lunghezza|Descrizione
---|---|
|4|La lunghezza dei seguenti dati Colore
|variabile|I dati del colore

I dati sulla modalità colore sono disponibili solo per il colore indicizzato e la due tonalità come definito dal campo della modalità nella sezione Intestazione file. Per tutte le altre modalità, questa sezione è rappresentata da valori azzerati a 4 byte. Per le immagini a colori indicizzate, la lunghezza è 768 e i dati del colore contengono la tabella dei colori dell'immagine, in ordine non interlacciato. Per le immagini a due tonalità, i dati sui colori contengono la specifica dei due toni (il cui formato non è documentato). Altre applicazioni che leggono i file di Photoshop possono trattare un'immagine a due tonalità come un'immagine grigia e conservare semplicemente il contenuto delle informazioni sui due toni durante la lettura e la scrittura del file.

### Sezione risorse immagine ###

La terza sezione del file contiene risorse di immagine. Inizia con un campo di lunghezza, seguito da una serie di blocchi di risorse.


|Lunghezza|Descrizione
---|---|
|4|Lunghezza della sezione della risorsa immagine. La lunghezza può essere zero.
|Variabile|Risorse immagine (Blocchi risorse immagine)

Le risorse immagine vengono utilizzate per archiviare dati non pixel associati a immagini come i percorsi degli strumenti penna. Sono indicati come blocchi di risorse perché contengono i dati che erano archiviati nella risorsa del Macintosh nelle prime versioni di Photoshop. La struttura di base dei blocchi di risorse immagine è quella mostrata di seguito:


|Lunghezza|Descrizione
---|---|
|4|Firma: '8BIM'
|2|Identificatore univoco per la risorsa. ID risorsa immagine contiene un elenco di ID risorsa utilizzati da Photoshop.
|Variabile|Nome: stringa Pascal, imbottita per rendere la dimensione pari (un nome nullo è composto da due byte di 0)
|4|Dimensioni effettive dei dati delle risorse che seguono
|Variabile|I dati della risorsa, descritti nelle sezioni sui singoli tipi di risorsa. È imbottito per uniformare le dimensioni.

Le risorse di immagine utilizzano diversi numeri ID standard.

### Informazioni su livelli e maschere ###

La quarta sezione di un file di Photoshop contiene informazioni su livelli e maschere come numero di livelli, canali nei livelli, intervalli di fusione, chiavi del livello di regolazione, livelli di effetti e parametri della maschera. Se non ci sono livelli o maschere, questa sezione è rappresentata da un campo di 4 byte azzerato. È necessario prestare particolare attenzione alla lunghezza delle sezioni durante la lettura di questa sezione a causa dei valori azzerati. La disposizione della sezione Layer e Mask è la seguente:


|Lunghezza|Descrizione
---|---|
|4|Lunghezza della sezione delle informazioni sul livello e sulla maschera. (La lunghezza del PSB è di 8 byte.)
|Variabile|Informazioni livello
|Variabile|Informazioni globali sulla maschera di livello
|Variabile|Serie di blocchi contrassegnati contenenti vari tipi di dati.

#### Informazioni sul livello ####

La tabella seguente mostra l'organizzazione di alto livello delle informazioni sul livello.


|Lunghezza|Descrizione
---|---|
|4|Lunghezza della sezione delle informazioni sui livelli, arrotondata per eccesso a un multiplo di 2. (La lunghezza del PSB è 8 byte.)
|2|Conteggio livelli. Se è un numero negativo, il suo valore assoluto è il numero di livelli e il primo canale alfa contiene i dati di trasparenza per il risultato unito.
|Variabile|Informazioni su ciascun livello. Vedere record di livello descrive la struttura di queste informazioni per ogni livello.
|Variabile|Dati immagine canale. Contiene uno o più record di dati immagine per ogni livello. I livelli sono nello stesso ordine delle informazioni sui livelli

### Dati immagine ###

I dati dei pixel dell'immagine sono contenuti nella sezione Dati immagine del file. La disposizione dei dati nella sezione Dati immagine è in ordine planare, cioè prima tutti i dati rossi, poi tutti i dati verdi, ecc. Ogni piano è memorizzato in ordine di scan-line, senza byte pad, La sezione dati immagine è organizzata in un formato come mostrato nella tabella seguente.

|Lunghezza|Descrizione
---|---|
|2|Metodo di compressione: *0 = Dati immagine grezzi * 1 = RLE compresso i dati dell'immagine iniziano con il conteggio dei byte per tutte le linee di scansione (righe * canali), con ciascun conteggio memorizzato come valore a due byte. Seguono i dati compressi RLE, con ciascuna linea di scansione compressa separatamente. La compressione RLE è lo stesso algoritmo di compressione utilizzato dalla routine ROM Macintosh PackBits e dallo standard TIFF. *2 = ZIP senza previsione *3 = ZIP con previsione.
|Variabile|I dati dell'immagine. Ordine planare = RRR GGG BBB, ecc.

## Riferimenti ##

* [Specifiche del formato file PSD - di Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Formato file Adobe Photoshop](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

