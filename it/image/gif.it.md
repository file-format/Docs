{
  "date" : "2019-10-11",
  "keywords" :[ "file gif", "formato file gif", "cos'è un file gif", "file", "esempio gif", "estensione file gif", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Formato file immagine",
  "description":"Scopri il formato di file GIF e le API che possono creare e aprire file GIF.",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file GIF? ##

Un formato GIF o Graphical Interchange Format è un tipo di immagine altamente compressa. Di proprietà di Unisys, GIF utilizza l'algoritmo di compressione LZW che non degrada la qualità dell'immagine. Per ogni immagine GIF in genere consentono fino a 8 bit per pixel e sono consentiti fino a 256 colori nell'immagine. In contrasto con un'immagine [JPEG](/it/image/jpeg/), che può visualizzare fino a 16 milioni di colori e tocca i limiti dell'occhio umano. Quando è emerso Internet, le GIF sono rimaste la scelta migliore perché richiedevano una larghezza di banda ridotta e compatibili per la grafica che consuma aree di colore solide. Una GIF animata combina numerose immagini o fotogrammi in un unico file e le visualizza in sequenza per generare una clip animata o un breve video. I limiti di colore sono fino a 256 per ogni fotogramma e sono probabilmente i meno adatti per riprodurre altre immagini e fotografie con gradiente di colore.

## Formato file GIF ##

Concettualmente, i file GIF hanno un'area grafica di dimensioni fisse riempita da zero o più immagini. Alcuni file GIF dividono l'area grafica oi blocchi di dimensioni fisse in immagini secondarie in grado di funzionare come frame animati in caso di GIF animate. Il formato GIF utilizza la profondità dei pixel da 1 a 8 bit per memorizzare i dati bitmap. I dati del modello di colore RGB e della tavolozza vengono sempre utilizzati per memorizzare le immagini. A seconda della versione, un'intestazione di lunghezza fissa ("GIF87a" o "GIF89a") definisce l'inizio di un tipico file GIF.

Attualmente sono disponibili due versioni di GIF: 87a e 89a. Il primo è il formato GIF originale mentre il secondo è il nuovo formato GIF. In questo formato di file, le caratteristiche dei blocchi e le dimensioni dei pixel sono menzionate in un Descrittore di schermo logico a lunghezza fissa. L'esistenza e la dimensione di una tabella dei colori globale possono essere specificate dal descrittore dello schermo, che tiene traccia di ulteriori dettagli se presenti. Il trailer è l'ultimo byte del file che contiene un singolo byte di un punto e virgola ASCII. Un tipico layout di file GIF87a è il seguente:

### Intestazione ###

L'intestazione contiene sei byte e viene utilizzata per specificare il tipo di file come GIF. Sebbene il Logical Screen Descriptor sia separato dall'intestazione effettiva, a volte viene considerato come la seconda intestazione. La stessa struttura utilizzata per memorizzare l'intestazione può memorizzare il Descrittore dello schermo logico. Tutti i file GIF iniziano con la firma a 3 byte e utilizzano i caratteri "GIF" come identificatore. Anche la versione ha una dimensione di tre byte e dichiara la versione del file GIF.

### Descrittore schermo logico ###

Un descrittore di immagine a lunghezza fissa specifica lo schermo e le informazioni sul colore necessarie per creare l'immagine GIF. I campi Altezza e Larghezza racchiudono il valore più piccolo della risoluzione dello schermo, obbligatorio per mostrare i dati dell'immagine. Se il dispositivo di visualizzazione non è in grado di visualizzare la risoluzione specificata, sarà necessario il ridimensionamento per visualizzare adeguatamente l'immagine. Le informazioni sullo schermo e sulla mappa dei colori vengono visualizzate dai quattro sottocampi della tabella seguente (mentre il bit 0 è il bit meno significativo):


|Bit|Sottocampi
---|---|
|0-2|Dimensioni della tabella dei colori globale
|3|Tabella dei colori Ordina bandiera
|4-6|Risoluzione colore
|7|Bandiera globale della tabella dei colori

#### Tabella colori globale ####

Una tabella dei colori globale opzionale viene posizionata subito dopo il Descrittore dello schermo logico. Questa tabella è stata mappata per indicizzare i dati sul colore dei pixel all'interno dei dati dell'immagine. In assenza di una tabella colori globale, ogni immagine nel file GIF utilizza il suo colore locale. È meglio fornire una tabella dei colori predefinita se mancano sia la tabella dei colori globale che quella locale. Una serie di triple di tre byte compone gli elementi della tavola dei colori. Ogni byte caratterizza un valore di colore RGB. I colori rosso, verde e blu vengono utilizzati come valori di ciascun elemento della tabella dei colori. Le voci nella Tabella dei colori globale raggiungono un massimo di 256 voci e rappresentano sempre una potenza di due.

#### Dati immagine ####

I dati dell'immagine memorizzano un byte di simboli non codificati seguito da un elenco collegato di sub- insieme ai dati codificati LZW.

#### Trailer ####

Trailer rappresenta un singolo byte di dati che è l'ultimo carattere nel file. Il valore di questo byte è permanentemente 3Bh e specifica la fine del flusso di dati. Ogni file GIF deve avere il trailer nell'ultimo di ogni file.

## Riferimenti ##

* [Formato file GIF](https://en.wikipedia.org/wiki/GIF)

