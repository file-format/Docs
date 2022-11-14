{
  "date" : "2021-02-15",
  "keywords" :[ "file vp6", "formato file vp6", "cos'è un file vp6", "file", "esempio vp6", "estensione file vp6", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - File video TrueMotion",
  "description":"Scopri il formato di file VP6 e le API che possono creare e aprire file VP6.",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Che cos'è un file VP6?

VP6 è un formato video con compressione con perdita di dati introdotto dalle tecnologie On2 nel maggio 2003. Fa parte di una serie di codec video sviluppati da TrueMotion, inclusi V3, V4 e V5. Il formato è stato utilizzato a breve nel campo della trasmissione, ad esempio con i rapporti della BBC e il software QuickLink. VP6 è stato sostituito da VP7 Codec nel gennaio 2005 con una migliore compatibilità di compressione.

## Formato file VP6

Le specifiche complete per i file V6 non sono disponibili pubblicamente. On2 inizialmente rese pubbliche le specifiche, ma presto queste furono rese non disponibili per gli utenti generici. Una documentazione non ufficiale del formato di file VP6 è disponibile su [wiki multimediale](https://wiki.multimedia.cx/index.php?title=On2_VP6) a cui si può fare riferimento come riferimento per gli sviluppatori.

### Macroblocchi (MB)

Simile a MPEG-2, MPEG-4 parti 2 e 10, ogni fotogramma video di un file VP6 è composto da un array di 16x16 macroblocchi (MB). Ogni MB può essere in una delle seguenti modalità:

* Intra MB
* Inter MB, MV nullo, riferimento frame precedente
* Inter MB, differenziale MV, riferimento telaio precedente
* Inter MB, quattro MV, riferimento quadro precedente
* Inter MB, MV 1, riferimento quadro precedente
* Inter MB, MV 2, riferimento quadro precedente
* Inter MB, MV nullo, riferimento di frame con segnalibro
* Inter MB, differenziale MV, riferimento di frame con segnalibro
* Inter MB, MV 1, riferimento di frame con segnalibro
* Inter MB, MV 2, riferimento di frame con segnalibro

### Intestazione frame

L'intestazione del frame di un VP6 è come mostrato di seguito e segue l'imballaggio del bit big-endian.

|Sintassi|Numero di bit|Tipo|Symantec|
---|---|---|---|
|frame_mode|1|Enum|0x0 indica un intra frame|
|qp |6 |Unsigned |Intervallo valido parametro di quantizzazione 0..63|
|marcatore| 1| costante| 0=VP61/62, 1=VP60|
|if (modalità_frame == 0) { | 0 | |uguale a INTRA_FRAME|
|versione |5| costante| 6=VP60/61, 7=VP60(Arti Elettroniche), 8=VP62|
|versione2 |2| Costante |0=VP60, 3=VP61/62|
|intrecciare |1| Booleano |true (1) significa che verrà utilizzato l'interlacciato|
|if (marcatore==1 o versione2==0) {||||
|offset |16 |Senza segno| offset del buffer secondario (byte relativi all'inizio del buffer)|
|}||||
|dim_y |8| Non firmato| Altezza del macroblocco del video|
|dim_x |8| Non firmato| Larghezza macroblocco del video|
|render_y |8 |Non firmato |Visualizza altezza del video|
|render_x |8 |Non firmato |Visualizza larghezza del video|
|}altrimenti{||||
|if (marcatore==1 o versione2==0) {||||
|offset |16 |Unsigned |Offset buffer secondario (byte relativi all'inizio del buffer)|
|}||||
|}||||

## Riferimenti

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

