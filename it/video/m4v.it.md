{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "file", "estensione", "formato", "MPEG-4", "Gestione dei diritti digitali", "DRM", "Apple", "video"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"Scopri il formato di file M4V e le API che possono creare e aprire file M4V.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## Che cos'è un file M4V?

Il formato file **M4V**, sviluppato da Apple, è un contenitore video protetto opzionalmente con la protezione dalla copia DRM (Digital Rights Management) per proteggere la privacy o la copia. I video e le tracce audio sono avvolti da file contenitore per l'indicizzazione e l'organizzazione dei flussi di riproduzione. Inoltre, i contenitori forniscono anche la funzione di capitoli simili a quelli dei DVD. Apple utilizza M4V per codificare i video nel suo iTunes Store. Protegge la riproduzione non autorizzata tramite la protezione dalla copia FairPlay di Apple consentendo la riproduzione di file M4V solo su computer autorizzati con account utilizzati per acquistare il video. Tuttavia, se la protezione DRM viene rimossa dai file M4V, questi file possono essere riprodotti in altri lettori video modificando l'estensione da .m4v a .mp4, motivo per cui i file M4V sono associati a MPEG-4. M4V utilizza H.264 per il video e **[AAC](/it/audio/aac/)** e Dolby Digital per la codifica e la decodifica audio.

## Struttura del file M4V ##

I file M4V hanno blocchi continui con intestazione di 8 byte, dimensione del blocco di 4 byte e tipo di blocco di 4 byte in ogni blocco. Il primo pezzo è "ftype" e ha un sottotipo all'offset 8. M4V definito dal sottotipo che deve essere "M4V_". Ulteriori tipi di blocchi sono firme predefinite: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide" , "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " PICT". Iterando i blocchi, finché non viene rilevato un tipo sconosciuto, componiamo il file M4V.

Ecco un esame di un campione: i dati binari di un file m4v di esempio vengono ispezionati tramite Hex Viewer e si può osservare che inizia con una firma **ftyp** (hex: 66 74 79 70) all'offset 4, che definisce QuickTime Tipo di file contenitore. Il sottotipo di file è **M4V_** (esadecimale: 4D 34 56 20) che punta al tipo di file M4V (MPEG-4). La dimensione del primo blocco è 32 (hex: 00 00 00 20, big-endian, high byte prima), la dimensione si trova all'offset 0. All'offset 32 (hex: 20) si trova il secondo blocco, che ha una dimensione di 30.322 (hex : 00 00 76 72, big-endian, prima il byte inferiore) e digitare **moov** (esadecimale: 6D 6F 6F 76). Il blocco successivo si trova all'offset 32+30,322#30,354 (hex: 00 00 76 92) e ha una dimensione 8 (hex: 00 00 00 08) e tipo **free** (hex: 66 72 65 65).
### Codec utilizzati in M4V ###

#### Codec video H.264 ####

H.264 è uno standard di compressione video che converte il video digitale in un formato che richiede meno spazio quando è richiesta la trasmissione o l'archiviazione. M4V utilizza H.264 per la compressione video. La sua applicazione spazia da DVD, TV, videoconferenze e streaming video su Internet. H.264 è costituito da due parti principali: Encoder – che comprime il video, Decoder – che decomprime il video compresso. Nella figura seguente sono evidenziati i processi di codifica e decodifica e altri processi sono trattati nello standard H.264.

##### Processo di codifica e decodifica video in H.264 #####

Per il flusso di bit H.264 compresso, il codificatore video esegue il processo di previsione, trasformazione e codifica. Allo stesso tempo, il decodificatore esegue il processo inverso di decodifica, trasformazione inversa e ricostruzione per produrre il file video. H.264 occupa la metà delle dimensioni dell'MPEG.

#### Codec audio ####

Advanced Audio Coding (AAC) è un codec audio per la compressione audio digitale con perdita e viene utilizzato in un contenitore M4V. AAC è il successore del formato [MP3](/it/audio/mp3/) e raggiunge una qualità migliore rispetto a MP3 con lo stesso bitrate. Il formato AAC elimina alcune informazioni durante il processo di compressione, che è di minore importanza. AAC è un codec basato su blocchi a velocità di trasmissione variabile (VBR) in cui ogni blocco decodifica in 1024 campioni nel dominio del tempo.

### Riferimenti ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipedia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

