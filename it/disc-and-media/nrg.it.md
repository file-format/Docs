{
  "date" : "2021-08-16",
  "keywords" :[ "file nrg", "formato file nrg", "cos'è un file nrg", "file", "esempio nrg", "estensione file nrg", "estensione", "formato", "piè di pagina nrg", "file formato di nrg", "Nero Burning Rom", "Nero AG" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Scopri il formato di file NRG e le API che possono creare e aprire file NRG.",
  "title" :"NRG - Formato file immagine disco",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## Che cos'è un file NRG?

Un formato di file immagine creato mediante l'uso di un disco ottico è considerato un formato di file NRG. Questo formato è stato creato specificamente da Nero per l'utilità di Nero Burning Rom. Per la memorizzazione di immagini disco, questo formato è considerato utilizzato in quanto appropriato per questi file specifici. Questi file possono avere la forma di una copia esatta di un CD o DVD o possono avere diversi file che possono essere montati come disco. Altri formati di file più popolari come i formati di file [ISO](/it/compression/iso/) sono quelli in cui questi file possono essere convertiti in alcune utilità di base. Per lo più, i file NRG vengono utilizzati per creare backup o copie di alcuni dati o dischi importanti.

## Formato file NRG ##

Questo formato di file è stato sviluppato da Nero AG come formato immagine disco. Aveva la proprietà specifica dell'utilità Nero Burning Rom poiché era stato sviluppato per archiviare le immagini del disco. La sua prima versione è stata specificata per memorizzare i valori come interi a 32 bit. Tuttavia, la sua seconda versione è stata lanciata e conteneva il supporto per numeri interi a 64 bit.

## Specifica tecnica ##

All'inizio del file, questo formato non memorizza i suoi dati come intestazione. Come un piè di pagina, è allegato alla fine del file. Sotto forma di blocchi di IFF, le informazioni dell'immagine vengono memorizzate. L'offset del primo blocco può essere ottenuto leggendo il footer NRG dagli ultimi 8 byte a 12 byte del file. In tutte le versioni del formato di file NRG, ci sono blocchi, DAOI, testo del CD, tipo di supporto per le informazioni sulla sessione, informazioni sul disco, Relo e fine della catena ad esso collegati. L'ordine dei byte è big-endian e tutti i valori interi non sono contrassegnati al momento dell'archiviazione.

### Pezzi principali ###

#### Foglio di spunto ####

Questo cue sheet è facilmente disponibile in tutte le versioni del formato di file NRG. Il pezzo di **CUEX** indica i blocchi di concatenazione di dimensioni fisse e ognuno di questi rappresenta il cue point.

#### Informazioni DAO ####

Questa informazione è presente anche in tutte le versioni del formato NRG. I blocchi di **DAOI** memorizzano le informazioni specifiche pertinenti in 2 parti. La sua prima parte è costituita solo dai dati specifici della sessione. La sua seconda parte ripete semplicemente le informazioni grigie relative al tracciamento ed è solo una volta per ogni traccia.

#### CD-testo ####

Questo è disponibile nella seconda versione di NRG. Il blocco di **CDTX** è costituito dalla concatenazione grezza del pacchetto di testo CD con 18 byte per ciascuno.

#### Informazioni estese sulla traccia ####

Questo è disponibile in ogni versione del formato file di NRG. Questi blocchi vengono utilizzati per memorizzare le informazioni di tracciamento per la traccia delle sessioni in una volta. Questi dati vengono ripetuti una sola volta per ogni traccia.

#### Informazioni sulla sessione ####

Questo è disponibile anche in ogni versione del formato file di NRG. Le informazioni dei blocchi di sessione devono essere utilizzate per scansionare rapidamente l'immagine della sessione e quindi tenere traccia del conteggio.

#### Fine della catena ####

Il pezzo di fine indica i segnali che ora non ci sono più blocchi che devono essere letti e questo è disponibile anche in tutte le versioni di NRG.


## Riferimenti ##

* [NRG - di Wikipedia](https://en.wikipedia.org/wiki/NRG_(file_format))


