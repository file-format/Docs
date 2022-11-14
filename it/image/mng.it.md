{
  "date" : "2019-10-11",
  "keywords" :[ "file mng", "formato file mng", "cos'è un file mng", "file", "esempio mng", "estensione file mng", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file MNG - Formato file grafico di rete a più immagini",
  "description":"Scopri il formato di file MNG e le API che possono creare e aprire file MNG.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file MNG?

Un file con estensione .mng è un formato di file di grafica di rete a più immagini simile al formato immagine [PNG](/it/image/png/) ma supporta le immagini animate. È stato sviluppato per evitare di sovraccaricare il formato PNG con funzionalità aggiuntive di animazioni. MNG è anche simile ai file [GIF](/it/image/gif/) ma utilizza una maggiore compressione e supporta la funzionalità alfa completa. Il tipo di supporto MIME non ufficiale per i file MNG è video/x-mng. I file MNG possono essere aperti in applicazioni come ImageMagik e IrfanView.

## Formato file MNG

Il formato del file MNG è simile a quello di PNG e utilizza la stessa struttura a blocchi definita nelle specifiche PNG. Un decodificatore MNG deve essere in grado di decodificare i flussi di dati PNG senza specificare alcun flag speciale per le istruzioni di decodifica. MNG raggruppa più immagini insieme in una "cornice", con alcune immagini utilizzate come sprite per spostarsi da una posizione all'altra. Il meccanismo consente di riutilizzare i dati dell'immagine senza ritrasmetterli. È possibile fare riferimento alle [specifiche MNG](http://www.libpng.org/pub/mng/spec/) come riferimento per gli sviluppatori.

### Firma MNG

Il flusso di dati MNG inizia con una firma di 8 byte contenente:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

È simile a quella della firma PNG ma contiene MNG anziché PNG.

### Cornice MNG

Un frame MNG è costituito da un'immagine bidimensionale di immagini più piccole. È possibile accedere a ciascuna piccola immagine utilizzando la combinazione di indice di riga e di colonna. Il formato è in grado di memorizzare dati "voxel" tridimensionali disposti su una serie di piani bidimensionali. Ogni aereo è rappresentato da un flusso di dati PNG o Delta-PNG. Ciascun flusso di dati Delta-PNG definisce un'immagine come le differenze rispetto all'immagine PNG principale. Ciò fornisce un modo molto più compatto di rappresentare le immagini successive rispetto all'utilizzo di un flusso di dati PNG completo per ciascuna.

## Riferimenti ##

* [MNG](http://www.libpng.org/pub/mng/)
* [Formato MNG v 1.0](http://www.libpng.org/pub/mng/spec/)

