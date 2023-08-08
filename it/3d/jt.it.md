{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "file", "estensione", "formato", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file JT e le API che possono creare e aprire file JT.",
  "title" :"JT - Formato file di tassellazione di Giove",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file JT?

**JT** (Jupiter Tessellation) è un formato di dati 3D standardizzato ISO efficiente, orientato al settore e flessibile sviluppato da Siemens PLM Software. I domini CAD meccanici dell'industria aerospaziale, automobilistica e delle attrezzature pesanti utilizzano JT come formato di visualizzazione 3D più importante.

Il formato JT è un grafico di scena che supporta gli attributi e i nodi specifici del CAD. Sofisticate tecniche di compressione vengono utilizzate per archiviare i dati dei facet (triangoli). Questo formato è strutturato per supportare attributi visivi, informazioni sul prodotto e sulla produzione (PMI) e metadati. C'è un buon supporto per lo streaming asincrono di contenuti. Nell'industria meccanica pesante, i professionisti utilizzano il file JT nelle loro soluzioni CAD e nei programmi software di gestione del ciclo di vita del prodotto (PLM) per esaminare la geometria di merci complicate.

Poiché JT supporta quasi tutti i formati CAD 3D importanti, il suo assemblaggio può gestire una varietà di combinazioni note come "multi-CAD". Questo assemblaggio multi-CAD è sempre ben gestito e aggiornato perché la sincronizzazione tra i file di descrizione del prodotto CAD nativi con i file JT associati avviene automaticamente. I file JT sono originariamente leggeri, quindi considerati adatti per le collaborazioni su Internet. Le aziende collaborano inviando visualizzazioni 3D sui media molto più facilmente rispetto ai file CAD originali "pesanti". Inoltre, i file JT garantiscono molte funzionalità di sicurezza che rendono più sicura la condivisione della proprietà intellettuale.

## Breve storia del formato di file JT

Engineering Animation, Inc. e Hewlett Packard sono stati i designer originali di JT, che hanno sviluppato quel formato come toolkit Direct Model. Dopo che EAI è stata acquisita da UGS Corp., JT è diventata parte della suite di UGS. All'inizio del 2007, UGS ha annunciato JT come formato 3D principale. Nello stesso anno, Siemens AG acquistò UGS e si rivelò essere Siemens PLM Software. Siemens utilizza JT come formato di interoperabilità e formato di archiviazione dati comune. Nel 2009, ISO ha accettato la specifica JT per la pubblicazione come ISO Publicly Available Specification (PAS). A metà del 2010, ProSTEP iViP ha annunciato che a livello industriale, JT e STEP AP 242 XML possono essere utilizzati insieme per ottenere il massimo vantaggio nei dati scenari di scambio. Nel 2012, JT è stato ufficialmente dichiarato formato di visualizzazione 3D standardizzato ISO (ISO 14306:2012 (ISO JT V1)).

## Formato file JT ##

Tutti gli oggetti nel formato JT sono rappresentati tramite un identificatore di oggetto e i riferimenti tra gli oggetti vengono gestiti tramite l'identificatore di oggetto referenziato. L'integrità di questi riferimenti a oggetti può essere mantenuta tramite i puntatori unswizzling/swizzling.

Un file JT è organizzato come una serie di blocchi e il blocco di intestazione è sempre il primo blocco di dati nel file. Una serie di segmenti di dati e un segmento TOC seguono immediatamente il blocco di intestazione. L'unico segmento di dati (6 segmenti LSG) possiede un file JT conforme al riferimento esiste sempre. Segmento TOC contiene le informazioni sulla posizione di tutti gli altri segmenti di dati di quel file.

{{< figure src="../JT-1.png" alt="Formato file JT" >}}

### Intestazione del file ###

File Header è il primo blocco nella gerarchia dei dati del file JT. Le informazioni sulla versione e le informazioni sulla posizione TOC sono racchiuse nell'intestazione che facilita i caricatori nella lettura dei file. Il contenuto dell'intestazione del file è organizzato come segue.

### Segmento sommario ###

Il segmento TOC deve esistere all'interno di un file e contiene informazioni di identificazione e posizione di tutti gli altri segmenti di dati. La posizione effettiva del segmento TOC è specificata dal campo Offset TOC dell'intestazione del file. Ciascun segmento di dati indirizzabile individualmente è rappresentato da una voce TOC in un segmento TOC.

### Segmento di dati ###

Il file JT definisce tutti i dati memorizzati all'interno di un segmento di dati. Alcuni segmenti di dati possono comprimere tutti i byte di dati di informazioni rimasti all'interno del segmento. I segmenti di dati hanno la seguente struttura:

![alt text](../JT-2.png "JT Data Segment")

La tabella seguente descrive diversi tipi di segmenti di dati:

|Nome|Descrizione
---|---|
|Segmento LSG|Comprende una raccolta di oggetti collegati tramite riferimenti diretti per formare LSG (struttura del grafico aciclico diretto)
|Shape LOD segment|contiene i dati che definiscono le forme geometriche (es. vertici, normali, poligoni, ecc.)
|Segmento JT B-Rep|Avere un elemento per i dati per rappresentare il confine geometrico preciso per una singola porzione in formato JT B-Rep.
|Segmento XT B-Rep|Avere un elemento per i dati per rappresentare il confine geometrico preciso per una singola porzione nel formato di rappresentazione del confine
|Segmento wireframe|I dati rappresentano un wireframe 3D preciso per una porzione particolare è definita da un elemento contenuto in questo segmento.
|Segmento di metadati|Consente di memorizzare i metadati in segmenti indirizzabili distinti.
|Segmento JT ULP|Avere un elemento per i dati per rappresentare il confine geometrico semi-preciso per una singola porzione in formato JT ULP.
|Segmento JT LWPA|Contiene un elemento che definisce i dati analitici per una parte particolare. LWPA racchiude la raccolta di superfici analitiche nella definizione b-rep della parte.

## Compressione ##

I requisiti di trasmissione e archiviazione dei modelli 3D sono più esigenti, quindi i file JT possono trarre vantaggio dalla compressione. Un modello di dati JT può essere composto da file diversi che utilizzano una tecnica di compressione diversa, ma il processo di compressione è trasparente per l'utente dei dati JT.

Finora, JT Open Toolkit (come standard) e la compressione avanzata sono due tecniche di compressione utilizzate dai file JT. JT Open Toolkit utilizza un algoritmo di compressione semplice e senza perdite, mentre la compressione avanzata impiega una tecnica di compressione più raffinata e specifica del dominio porta alla compressione della geometria con perdita. Le applicazioni client preferiscono la compressione avanzata piuttosto che utilizzare la compressione standard, poiché la compressione avanzata produce rapporti di compressione piuttosto elevati. La compatibilità con le versioni precedenti con le normali applicazioni di visualizzazione di file JT viene mantenuta grazie alla compressione standard. Il modulo di compressione deve essere compatibile con la versione del formato di file JT che può essere visualizzata quando un file JT viene aperto utilizzando un editor di testo e racchiuso tra le informazioni di intestazione ASCII.

## Riferimenti ##

* [Riferimento formato file JT](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (formato di visualizzazione)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)

