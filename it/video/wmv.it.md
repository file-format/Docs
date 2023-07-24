{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file WMV",
  "description":"Scopri il formato di file WMV e le API che possono creare e aprire file WMV.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## Che cos'è un file WMV?

L'Advanced Systems Format (ASF) è un contenitore multimediale digitale progettato principalmente per archiviare e trasmettere flussi multimediali. Microsoft Windows Media Video (WMV) è il formato video compresso e Microsoft Windows Media Audio (WMA) è il formato audio compresso insieme a metadati aggiuntivi nel contenitore ASF sviluppato da Microsoft. Una volta che i file WMV o WMA sono stati codificati con i codec Windows Media Video e Windows Media Audio, vengono rappresentati con estensione .asf. WMV comprime file di grandi dimensioni per una migliore velocità di trasmissione su una rete mantenendo la qualità del video. WMV è progettato specificamente per essere eseguito su tutti i dispositivi Windows. Dopo la standardizzazione da parte della Society of Motion Picture and Television Engineers (SMPTE), WMV è ora considerato un formato standard aperto.

## Storia ##

Con l'aiuto dei codec proprietari di Microsoft, nel 1999 è stato sviluppato un nuovo formato video compresso noto come WMV7, basato su MPEG-4 Part 2. Sono stati aggiunti miglioramenti in altre due versioni, ad esempio WMV8 e 9. Microsoft ha presentato una versione 9^^^^ di WMV a SMPTE per la standardizzazione nel 2003 che è stato infine standardizzato nel 2006 come SMPTE 421M noto anche come VC-1. L'idea alla base del WMV era quella di sviluppare un formato multimediale che potesse essere supportato da tutto l'hardware e il software supportati da Microsoft. Inoltre, un altro scopo importante era trasmettere flussi video su Internet in uno scenario ottimale. Dopo la standardizzazione di SMPTE, WMV è diventato anche un formato video per dischi Blu-ray.

## Specifiche del formato file

### Contenitore

Generalmente, WMV è confezionato in un contenitore ASF ma in aggiunta, il contenitore Matroska o AVI può anche supportarlo con estensioni rispettivamente di .mkv e .avi.

### Windows Media Video 9

Sebbene ci siano vari codec audio e video disponibili nella serie Windows Media Video 9 per la creazione e la riproduzione di media digitali, il codec WMV-9 è il più recente e migliore codec video in quanto può ottenere la compressione ottimale da velocità in bit molto basse, ovvero 160 x Da 120 a 10 Kbps a 1920 x 1080 a 4-8 Mbps per una varietà di video HD.

### Struttura del codec

WMV-9 ha un formato colore interno 4:2:0 a 8 bit. Come tutti gli altri popolari standard di compressione video MPEG-1 e H.261, WMV-9 utilizza una compensazione del movimento basata su blocchi e uno schema di trasformazione spaziale. In generale, possiamo dire che questi standard eseguono la compensazione del movimento blocco per blocco dal precedente frame ricostruito con l'aiuto di una quantità 2-D chiamata vettore di movimento (MV) per segnalare lo spostamento spaziale. Il blocco corrente viene formato con l'aiuto della previsione dei valori della stessa dimensione del precedente frame ricostruito che viene spostato dalla posizione corrente dal vettore di movimento. Infine, l'errore residuo viene calcolato come differenza tra il blocco previsto con compensazione del movimento e il blocco effettivo. Questo errore residuo viene trasformato utilizzando una trasformata lineare di compattazione dell'energia, quindi quantizzato e codificato entropia.

I coefficienti di trasformata quantizzata vengono decodificati, dequantizzati e trasformati inversamente entropia per produrre un'approssimazione dell'errore residuo sul lato del decodificatore, che viene quindi aggiunto alla previsione compensata dal movimento per generare la ricostruzione. La descrizione di alto livello del codec è mostrata nell'immagine seguente.

Il resto della sezione discuterà i nuovi miglioramenti in WMV-9 che lo differenziano dal resto delle soluzioni di codifica video come gli standard MPEG. WMV-9 ha frame intra (I), previsti (P) e predetti bidirezionalmente (B). I frame intra sono quelli codificati in modo indipendente e non hanno dipendenza da altri frame. I frame previsti sono frame che dipendono da un frame nel passato. La decodifica di un frame previsto può avvenire solo dopo che tutti i frame di riferimento precedenti al frame corrente a partire dal frame più recente (I) sono stati decodificati. I frame B sono frame che hanno due riferimenti: uno nel passato temporale e uno nel futuro temporale. I frame B vengono trasmessi dopo i loro riferimenti, il che significa che i frame B vengono inviati fuori servizio per garantire che i loro riferimenti siano disponibili al momento della decodifica. I frame B in WMV-9 non vengono utilizzati come riferimento per i frame successivi. Ciò pone i fotogrammi B al di fuori del ciclo di decodifica, consentendo di prendere scorciatoie durante la decodifica dei fotogrammi B senza deriva o artefatti visivi a lungo termine. La definizione di cui sopra di fotogrammi I, P e B vale sia per le sequenze progressive che per quelle interlacciate.

Le prestazioni dei codec video vengono confrontate con il loro diagramma di distorsione della velocità (RD). È una curva 2D che mostra la distorsione prodotta dalla compressione a un certo bitrate.

WMV-9 ha affrontato questo problema con l'introduzione di una varietà di tecniche elencate di seguito:

1. Trasformazione adattiva della dimensione del blocco

2. Set di trasformazioni di precisione limitata

3. Compensazione del movimento

4. Quantizzazione e dequantizzazione

5. Codifica entropica avanzata

6. Filtraggio ad anello

7. Codifica avanzata del frame B

8. Codifica interlacciata

9. Levigatura della sovrapposizione

10. Strumenti a basso costo

11. Compensazione allo sbiadimento

## Riferimenti ##

* [https://bytescout.com/blog/2014/10/windows-media-video-format.html](https://bytescout.com/blog/2014/10/windows-media-video-format.html )
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


