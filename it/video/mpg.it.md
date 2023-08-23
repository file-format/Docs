{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file MPG",
  "keywords" :[ "MPG", "file", "estensione", "formato", "formato video", "che cos'è un formato file mpg", "formato file mpg", "lettore file mpg", "compressione mpeg", "video ", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"Scopri il formato di file MPG e le API che possono creare e mostrare come aprire i file MPG.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## Che cos'è un formato di file MPG? ##

Il file con estensione .mpg appartiene al gruppo di estensioni di file per la compressione audio e video MPEG-1 o MPEG-2. Il video MPEG-1 Part 2 non è facilmente disponibile e questa estensione (formato file MPG) punta tipicamente a un flusso di programma MPEG definito in MPEG-1 e MPEG-2, o un flusso di trasporto MPEG definito in MPEG-2 . Esistono anche altre estensioni come .m2ts che specificano il contenitore accurato, in questo caso MPEG-2 TS, ma questo ha poca attinenza con il supporto MPEG-1. [.mp3](/audio/mp3/) è l'estensione più comune per i file contenenti audio MP3. Un file MP3 è un tipico flusso di audio grezzo; il modo tradizionale per contrassegnare i file MP3 è scrivere i dati del flusso in segmenti "spazzatura" di ciascun fotogramma, che salvano le informazioni multimediali ma vengono scartate dal **lettore di file mpg**. Questa è una tecnica simile usata per etichettare i file AAC, ma al giorno d'oggi meno supportata.

## Compressione MPEG ##

Il nome MPEG sta per Moving Pictures Experts Group. MPEG è uno strumento per la compressione video, che prevede la compressione di immagini e suoni, nonché la sincronizzazione dei due.
Attualmente esistono diversi standard MPEG.

- MPEG-1 è proposto per velocità dati intermedie, dell'ordine di 1,5 Mbit/sec.
- MPEG-2 è proposto per velocità di trasmissione dati elevate di almeno 10 Mbit/sec.
- MPEG-3 è stato proposto per la compressione HDTV ma è risultato ridondante ed è stato fuso con MPEG-2.
- MPEG-4 è proposto per velocità dati molto basse, inferiori a 64 Kbit/sec.


## Flusso di programma del formato file MPG ##

Il flusso del programma è un contenitore per il multiplexing di audio digitale, video e altro. Il formato Program Stream è specificato nella prima parte di MPEG-1 (ISO/IEC 11172-1) e nella prima parte di MPEG-2, Systems (ISO/IEC standard 13818-1/ITU-T H.222.0). MPEG-2 Program Stream è basato su analogico e simile al livello di sistema ISO/IEC 11172 e compatibile con le versioni successive.

### Dettagli di codifica ###

Di seguito sono riportati i dettagli di codifica del formato di intestazione parziale del pacchetto Program Stream MPEG-2:

| Nome | Numero di bit | Descrizione |
---|---|---|
| byte di sincronizzazione | 32 | 0x000001BA |
| bit marker | 2 | 01b per la versione MPEG-2. I bit marker per la versione MPEG-1 sono 4 bit con valore 0010b. |
| Orologio di sistema [32..30] | 3 | Bit di riferimento dell'orologio di sistema (SCR) da 32 a 30 |
| punta dell'indicatore | 1 | 1 bit sempre impostato. |
| Orologio di sistema [29..15] | 15 | Bit dell'orologio di sistema da 29 a 15 |
| punta dell'indicatore | 1 | 1 bit sempre impostato. |
| Orologio di sistema [14..0] | 15 | Bit dell'orologio di sistema da 14 a 0 |
| punta dell'indicatore | 1 | 1 bit sempre impostato. |
| Estensione SCR | 9 | |
| punta dell'indicatore | 1 | 1 bit sempre impostato. |
| bit rate | 22 | In unità di 50 byte al secondo. |
| marcatori | 2 | 11 bit sempre impostati. |
| riservato | 5 | riservato per usi futuri |
| lunghezza del ripieno | 3 | |
| byte di riempimento | 8*lunghezza imbottitura | |
| intestazione di sistema (opzionale) | 0 o più | se segue il codice di avvio dell'intestazione di sistema: 0x000001BB |

La tabella seguente mostra il formato dell'intestazione del sistema parziale:

| Nome | Numero di byte | Descrizione |
---|---|---|
| byte di sincronizzazione | 4 | 0x000001BB |
| lunghezza dell'intestazione | 2 | |
| bit rate bound e marker | 3 | |
| rilegatura audio e bandiere | 1 | |
| flag, bit di indicatore e collegamento video | 1 | |
| Limitazione della velocità del pacchetto e byte riservato | 1 | |


## Riferimenti ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



