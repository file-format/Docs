{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "File BIF - Formato immagine diapositiva intera Ventana",
  "description":"Scopri il formato file BIF e le API che possono creare e aprire file BIF.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif-it",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Cos'è un file BIF?

Un file BIF è un file di immagine raster che contiene l'immagine del campione del vetrino. È costituito da più immagini TIFF combinate dalle applicazioni di visualizzazione delle diapositive in un'unica immagine composita. I file BIF sono creati dallo scanner di diapositive digitali dei sistemi Ventana Medical e sono pienamente conformi alla variante BigTIFF della definizione [TIFF](/image/tiff/) v 6.0.

## Formato file BIF

Un file BIF viene salvato come file immagine binario ed è composto da un massimo di 200.000 x 200.000 pixel. Ciò può portare a file di grandi dimensioni, superando il limite di dimensione di 4 GB imposto dai puntatori di file a 32 bit definiti dallo standard TIF. Con i puntatori di file a 64 bit, tuttavia, questa barriera relativa alla dimensione del file viene superata dalla variante BigTIFF dello standard TIFF.

### Chi utilizza il file BIF?

I file BIF vengono utilizzati dagli scanner per diapositive digitali per scansionare e creare copie digitali di campioni di diapositive. Se sei un patologo, puoi aprire questi file BIF nelle applicazioni di visualizzazione delle diapositive. Con un elevato livello di dettaglio e dati ad alta risoluzione, è possibile ingrandire e rimpicciolire l'immagine di una diapositiva per visualizzare le sezioni del campione più o meno dettagliate. Il file di metadati [XML](/web/xml/) presente in questi file definisce come devono essere combinate le immagini e l'immagine che deve essere utilizzata come miniatura del file.

## Come aprire il file BIF?

Puoi aprire file BIF con:

 * OpenSlide (multipiattaforma)
 * ImageJ (multipiattaforma)
 * Visualizzatore NetScope (Windows)

## Riferimenti ##

 * [Whitepaper BIF di Roche Digital Pathology](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

