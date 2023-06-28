{
  "date" : "2019-10-11",
  "keywords" :[ "file jp2", "formato file jp2", "cos'è un file jp2", "file", "esempio jp2", "estensione file jp2", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Formato file immagine",
  "description":"Scopri il formato di file JP2 e le API che possono creare e aprire file JP2.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## Che cos'è un file JP2? ##

JPEG 2000 (**JP2**) è un sistema di codifica delle immagini e uno standard di compressione delle immagini all'avanguardia. Utilizza la tecnologia wavelet per codificare contemporaneamente contenuti lossless di qualsiasi qualità. Inoltre, senza alcuna penalizzazione sostanziale nell'efficienza della codifica, JPEG 2000 ha la capacità di accedere e decodificare lo stesso contenuto in modo efficace in una varietà di altre risoluzioni e qualità. I flussi di codice in JPEG 2000 sono significativamente scalabili con regioni di interesse che forniscono la struttura per l'accesso casuale spaziale.

JPEG 2000 si distingue per essere uno degli standard più scalabili. Diverse parti di un'immagine possono essere memorizzate utilizzando diverse qualità. È possibile ottenere un'escalation degna di nota delle prestazioni ordinando il flusso di codice in vari modi. Tuttavia, JP2 richiede codificatori/decodificatori complessi e computazionalmente impegnativi, come risultato di questa flessibilità. Rispetto a JPEG, JPEG 2000 produce solo artefatti di squillo che creano anelli vicino al bordo dell'immagine e possono essere sfocati, mentre JPEG utilizza blocchi di artefatti visivi 8 × 8 che possono essere sia artefatti di squillo che di blocco. Possedendo fino a 16384 diversi componenti con le dimensioni in terapixel e una precisione che può arrivare fino a 38 bit/campione.

## Storia ##

Nel 2000, il comitato del Joint Photographic Experts Group ha progettato JP2 con l'obiettivo di migliorare il proprio standard JPEG basato sulla trasformata del coseno discreto con questo nuovo metodo basato su wavelet. Il comitato JPEG mirava a fornire i propri metodi di base senza costi di licenza. Nella licenza JP2 guadagnando concorrenza tra 20 aziende, hanno vinto per un soffio. JPEG 2000 è stato dichiarato standard ISO, sebbene la maggior parte dei browser Web non sia pronta a dare una mano a JPEG 2000 dal 2017.

## Parti del sistema di codifica delle immagini JPEG 2000 ##

Di seguito sono elencate le parti principali che costituiscono la suite completa di standard per JPEG 2000.


|Parte|Titolo|Descrizione|Numero
---|---|---|---|
|Parte 1|Sistema di codifica principale| Definisce la sintassi del flusso di codice. Diverse fasi coinvolte nella decodifica di immagini JPEG 2000. Spiega il formato file di base JP2, i metadati e i diritti IP da fornire.|ISO/IEC 15444-1
|Parte 2|Estensioni|Definisce le estensioni per il flusso di codice del formato file e consente dimostrazioni di campioni HDR, specifiche dello spazio colore, ritaglio, trasformazioni geometriche; animazioni, metadati e flussi di codice multipli.|ISO/IEC 15444-2
|Parte 3|Motion JPEG 2000 (MJ2 o MJP2)|Introdurre un formato file per sequenze di movimento, codificando le immagini in un flusso di codice indipendente.|ISO/IEC 15444-3
|Parte 4|Conformità|Indica le tecniche di test per la codifica e la decodifica e controlla i file sia per i flussi di codice nudo che per i file JP2.|ISO/IEC 15444-4
|Parte 5|Software di riferimento|Comprende due pacchetti di codice sorgente (Java, C) che implementano il sistema di codifica Core e sono disponibili con licenze open source.|ISO/IEC 15444-5
|Parte 6|Formato file immagine composto|Definisce il formato file JPM e consente l'imaging di documenti multipagina per applicazioni simili a fax. Supporta l'uso di JBIG2 e JPEG.|ISO/IEC 15444-6
|Parte 8|JPEG 2000 Secured (JPSEC)|Garantisce la sicurezza di transazioni, contenuti e tecnologie e consente flussi JPEG a 2000 bit protetti.|ISO/IEC 15444-8
|Parte 9|JPIP|Definisce gli strumenti in un ambiente di rete per accedere a metadati e immagini e indica protocolli interattivi ed efficienti|ISO/IEC 15444-9
|Parte 10|JP3D|Estensione volumetrica della Parte 1 e introduce la dimensione Z. Estende il concetto di riquadri, blocchi di codice, aree recintate e funzionalità di accessibilità 3D della regione di interesse.|ISO/IEC 15444-10
|Parte 11|JPWL|Si occupa di una trasmissione ben organizzata su una rete wireless soggetta a errori. Questa estensione è compatibile con i decoder|ISO/IEC 15444-11
|Parte 13|Codificatore entry-level|Definisce un'implementazione encoder entry level del sistema di codifica Core.|ISO/IEC 15444-13
|Parte 14|JPXML|Una rappresentazione in XML e spiega i segmenti di marker e i metodi per accedere ai dati interni delle immagini.|ISO/IEC 15444-14
|Parte 15|HTJ2K (in fase di sviluppo)|Specifica un algoritmo di codifica a blocchi alternativo. L'algoritmo offre un throughput dieci volte maggiore e una codifica/decodifica senza perdita di dati.|

## Formato file JP2 ##

JPEG 2000 definisce il formato del file e il flusso di codice allo stesso modo di JPEG-1. Sebbene i campioni di immagini siano descritti esclusivamente da JPEG 2000, tuttavia JPEG-1 include altre informazioni aggiuntive sullo spazio colore e sulla risoluzione essenziali per codificare l'immagine. Se un'immagine è archiviata come file JPEG 2000, come estensione viene utilizzato **.jp2**. Questo formato di file è ulteriormente migliorato dall'estensione JPEG 2000 part-2, che definisce i meccanismi di animazione e la configurazione di numerosi flussi di codice in un'unica immagine. L'estensione **.jpx** viene utilizzata quando le immagini vengono salvate utilizzando questo formato di file esteso. Poiché i dati del flusso di codice non sono considerati salvati principalmente nei file, non viene definita alcuna estensione standard per questo scopo. Anche se a scopo di test, ottiene spesso l'estensione **.jpc** o **.j2k**. Contrariamente a JPEG-1, JPEG 2000 sceglie un modo diverso di codificare i metadati in formato XML. Lo standard 12234-1.4 (dal comitato ISO TC42) viene utilizzato come riferimento tra i tag Exif e i componenti XML. JPEG 2000 può contenere uno standard ISO, XMP all'interno.

### Pezzi ###
I file JPEG 2000 sono costituiti da blocchi consecutivi. Ogni blocco ha un'intestazione di 8 byte: dimensione del blocco di 4 byte (big-endian, byte alto prima) e tipo di blocco di 4 byte - una delle firme predefinite: "jP" o "jP2".

Il secondo pezzo deve essere di tipo "ftyp" e ha un sottotipo all'offset 8. JPEG 2000 definito dal sottotipo che deve essere uno dei valori: "jp2 "(tipo di file \*.JP2), "jp20" (file digitare \*.JPA), "jpm " (tipo di file \*.JPM), "jpx " (tipo di file \*.JPX).

Iterando i blocchi, finché non viene rilevato un tipo sconosciuto, componiamo il file immagine/video JPEG 2000.

### Trasformazione del colore ###

Inizialmente, è richiesta la trasformazione delle immagini dallo spazio colore RGB a un altro spazio colore. A tale scopo, ci sono due modi: Irreversible Color Transform (ICT) e Reversible Color Transform (RCT). Il primo utilizza lo spazio colore YC,,B,,C,,R, e deve essere implementato in virgola fissa/mobile, mentre in seguito uno spazio colore YUV modificato e reversibile in natura.// //Non limitato al modello RGB, JPEG Il linguaggio 2000 utilizza la trasformazione di più componenti.

### Affiancamento ###

Al termine della trasformazione del colore, l'immagine viene convertita in regioni rettangolari chiamate tessere che possono essere trasformate e codificate separatamente. Le dimensioni di tutte le tessere avranno le stesse o l'intera immagine può essere considerata come una singola tessera. Il decodificatore sfrutta il vantaggio della piastrellatura e consuma meno memoria o può codificare parzialmente alcune tessere. Sebbene questa tecnica abbia uno svantaggio di degrado della qualità dell'immagine.

### Trasformazione Wavelet ###

L'immagine dopo la piastrellatura viene trasformata in wavelet che può essere irreversibile o reversibile e implementata utilizzando lo schema di convoluzione o sollevamento.

### Rapporto di compressione ###

A seconda delle caratteristiche fisiche di un'immagine, si ottiene un guadagno di compressione del 20% La previsione della ridondanza spaziale di JPEG 2000 gioca un ruolo fondamentale nel processo di compressione e le immagini ad alta risoluzione tendono a trarre il massimo vantaggio.

## Applicazioni servite dallo standard ##

* Registrazione, modifica e archiviazione di video HD basati su frame
* Immagini mediche e biometria
* immagini satellitari, telerilevamento e rilevamento del movimento
* Comunicazione client/server, distribuzione e archiviazione di rete.
* Cinema digitale, contributo di feed HDTV in diretta, materiale audiovisivo digitalizzato

## Riferimenti ##

* [Panoramica di JPEG 2000](https://jpeg.org/jpeg2000/)
* [Sistema di codifica delle immagini JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

