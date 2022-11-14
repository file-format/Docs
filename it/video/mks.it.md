{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file MKS",
  "keywords" :[ "mks", "matroska video", "mkv format", "file", "format", "video"],
  "description":"Scopri il formato di file MKS per i sottotitoli creati solo da Matroska e le API che possono creare e aprire file MKS.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## Che cos'è un file MKS?

I file MKS sono generalmente conosciuti come file Matroska contenenti solo i sottotitoli. Sebbene Matroska sia un contenitore di file generico, evita di conservare le informazioni di formati specifici. Poiché i sottotitoli vengono utilizzati in alcuni contenitori audio o video, Matroska sta prestando attenzione a memorizzare alcuni formati di sottotitoli comuni. Aiuta Matroska a essere coerente con il tasso di crescita. È necessario seguire i punti indicati di seguito per memorizzare i sottotitoli in Matroska:

- I ".mks". l'estensione sarà utilizzata dal file Matroska (contenente solo i sottotitoli).
- **CodecPrivate** viene utilizzato per archiviare tutte le informazioni relative ai codec globali per un intero flusso.
- Rimuovere i timestamp di inizio e fine utilizzati in un formato di archiviazione nativo di timestamp. Invece, usa il timestamp e la durata dei blocchi.
- Puoi usare qualsiasi cosa con un livello trasparente, incluso un video.

## Formati di sottotitoli comuni

Ecco alcune brevi note sui formati di sottotitoli più comuni archiviati in Matroska:

### Immagini Sottotitoli
Il formato dei sottotitoli VobSub è il primo formato dei sottotitoli delle immagini da importare in Matroska. Questo formato viene generato esportando i sottotitoli da un DVD. Le tracce devono essere separate durante la memorizzazione in Matroska se il VobSub è costituito da un insieme di più flussi.

### Sottotitoli SRT
L'SRT è il più semplice e basilare di tutti i formati di sottotitoli. Si compone di quattro parti come di seguito indicato:
 



1. Un numero che indica la sequenza del sottotitolo.
2. I sottotitoli appaiono e scompaiono sullo schermo.
3. Il sottotitolo stesso.
4. Una riga vuota per indicare l'inizio del sottotitolo successivo.
 



### Sottotitoli SSA/ASS
Sub Station Alpha (SSA) è un formato di file utilizzato dal popolare editor di sottotitoli SubStation Alpha. I sottotitoli SSA sono ampiamente utilizzati dai fan. Ha la capacità di visualizzare funzionalità moderne, ad esempio karaoke, posizionamento, styling, ecc.
 



### Sottotitoli WebVTT
Il World Wide Web Consortium (W3C) ha sviluppato il WebVTT, abbreviato in "Web Video Text Tracks Format". Questo formato viene utilizzato per contrassegnare le risorse di tracce di testo esterne in relazione all'elemento HTML.

### Sottotitoli grafici di presentazione HDMV
Il formato dei sottotitoli della grafica di presentazione HDMV (HDMV PGS) è una serie di bitmap e non possiamo dirlo affatto come testo. In altre parole, si può dire che si tratta solo di una sequenza temporizzata di immagini grafiche. Per estrarre le informazioni, convertire PGS in SRT è un processo necessario.

### Sottotitoli di testo HDMV
Il testo HDMV è noto come il formato dei sottotitoli testuali utilizzato sui Blu-ray. Matroska consente solo il set di caratteri UTF-8 Quando memorizza i sottotitoli TextST.

### Sottotitoli Digital Video Broadcasting (DVB).
È stato introdotto il formato dei sottotitoli DVB per regolare la trasmissione e la visualizzazione dei sottotitoli in più lingue sui segnali TV. Un tipico formato di sottotitolaggio consentirebbe anche a qualsiasi spettatore di guardare le trasmissioni sottotitolate DVB, indipendentemente dal produttore dei sistemi di trasmissione.


## Riferimenti ##

- [Sottotitoli Matroska](https://www.matroska.org/technical/subtitles.html)

