{
  "date" : "2020-03-16",
  "keywords" :[ "File IGES", "Formato file", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file IGES e le API che possono creare e aprire file IGES.",
  "title" :"Formato file IGES",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Che cos'è un file IGES?

Un file con estensione .iges viene utilizzato per scambiare informazioni di progettazione tra applicazioni CAD (Computer Aided Design). IGES sta per Initial Graphics Exchange Specifications. Le informazioni scambiate utilizzando IGES includono schemi circuitali, wireframe, superfici a forma libera o rappresentazioni di modellazione solida. IGES trova le sue applicazioni nei tradizionali disegni tecnici, analisi dei modelli e funzioni di produzione. Il formato può scambiare informazioni di progettazione 2D o 3D tra programmi CAD. I file IGES possono essere aperti con diverse applicazioni CAD come Autodesk e CADSoftTools ABViewer. Sono inoltre disponibili diverse API per aprire e convertire i file IGES a livello di codice.

## Formato file IGES

I file IGES sono in formato di testo ASCII e possono essere aperti in qualsiasi editor di testo per visualizzare il contenuto del file. Le informazioni testuali in un file IGES sono rappresentate in formato "Hollerith". Un file IGES comune può contenere migliaia di righe per rappresentare le informazioni 2D o 3D che possono essere scambiate secondo questo formato. Un file IGES è suddiviso in cinque sezioni, denotate dalla specifica lettera maiuscola nella 73a colonna. Queste sezioni sono le sezioni "Inizio" (S), "Globale" (G), "Inserimento dati" (D), "Dati parametro" (P) e "Termina" (T). Le sezioni Data Entry e Parameter Data sono comunemente abbreviate rispettivamente DE e PD.

### Intestazione del file IGES

Le sezioni Start e Global contengono informazioni di base su:
* Nome del file e la sua origine
* Delimitatori per la sezione Dati parametro
* Autore del file e altre informazioni generali.

Le sezioni Start e Global del documento di esempio su Wikipedia sono le seguenti.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Come si può vedere, il campo iniziale contiene descrizioni del file leggibili dall'uomo e il mio ha caratteri nelle colonne 1-72, con la riga che termina con l'intestazione della sezione e il numero di riga della sezione. Ci deve essere almeno 1 riga della sezione Start. La sezione globale contiene i dati del preprocessore. Inoltre deve essere presente nel file e terminare con il formato G000000#.

### Sezione immissione dati (DE) e dati parametro (PD).

#### Sezione immissione dati
Un file IGES è costituito da diverse entità che contengono le informazioni sui dati di base del formato di file IGES. Un'entità contiene informazioni su diversi elementi di un formato dati IGES e viene utilizzata per il disegno. Le entità più comunemente utilizzate includono:
* Arco circolare
* Curva composita
* Arco conico
* Aereo
* Linea

Questi sono solo alcuni e ci sono circa 150 entità diverse in IGES. Ogni entità è identificata da un numero di Tipo come:
* ARCO CIRCOLARE (Tipo 100)
* LINEA (Tipo 110)

##### Proprietà dell'entità

Ogni entità dichiarata ha le seguenti proprietà.

|Nome campo|Descrizione|
---|---|
|Tipo entità |Questo è il tipo di entità descritto. Ad esempio, 116 descrive un'entità Punto.|
|Puntatore PD |Questo fornisce la posizione per questi dati di entità nella sezione Dati parametro. Questa posizione è semplicemente il numero di riga all'interno della sezione PD che contiene la prima riga di questi dati di entità.|
|Struttura |Zero o puntatore all'entità di definizione. Non applicabile per la maggior parte delle entità|
|Modello carattere linea| Numero o puntatore all'entità del modello di carattere linea. Il numero significa: * 0 Nessun motivo specificato (predefinito) * 1 Solido * 2 Tratteggiato * 3 Fantasma * 4 Linea centrale * 5 Puntinato|
|Livello| Specifica i livelli da associare a questa entità. Consente all'entità di apparire su più di un livello|
|Visualizza| Specifica le opzioni di visualizzazione. Questi sono: 0 Indica visibilità e caratteristiche uguali in tutte le viste. Puntatore predefinito all'entità View (Tipo 410) che può essere visualizzata da Fare riferimento a un'entità View Visible Associativity (Tipo 402, Modulo 3)
|Puntatore matrice di trasformazione| Fa riferimento a un'entità matrice di trasformazione (Tipo 124) o è zero per impostazione predefinita (nessuna trasformazione)|
|Associatività visualizzazione etichette| Fa riferimento a un'associatività di visualizzazione dell'etichetta (tipo 402, modulo 5) che definisce come appare l'etichetta dell'entità.|
|Numero di stato| Contiene quattro sezioni di due numeri. 1-2: stato vuoto. O 00 per normale o 01 per oscurato. 3-4: Commutazione entità subordinata: è 00 per indipendente, 01 per dipendente fisicamente, 02 per dipendente logicamente e 03 per entrambi. 5-6: Entity Use flag: è 00 per Geometry, 01 per Annotation, 02 per Definition, 03 per Other, 04 per Logical, 05 per 2D parametric e 06 per Construction geometry. Infine, 7-8 è la gerarchia, dove 00 indica globale dall'alto verso il basso (usa le caratteristiche di questa entità), 01 è il differimento globale (non utilizzare le caratteristiche di questa entità) e 02 è la proprietà della gerarchia di utilizzo (usa l'entità gerarchia (tipo 406, modulo 10)determinare le caratteristiche del raggruppamento gerarchico).|
|Numero di sequenza| Specificato da D#, dove # è il numero di riga per questa sezione (non dall'inizio del file). Viene utilizzato anche per puntare a questa entità di immissione dati.|
|Tipo di entità| è specificato due volte per elenco di entità|
|Numero di peso della linea| Specifica lo spessore durante la visualizzazione dell'entità. Il più piccolo è 1, 0 è il valore predefinito|
|Numero colore| Specifica il colore dell'entità. I valori interi consentiti sono: 0 Nessun colore (predefinito) 1 Nero 2 Rosso 3 Verde 4 Blu 5 Giallo 6 Magenta 7 Ciano 8 Bianco|
|Numero conteggio righe parametro| Specifica il numero di righe occupate da questa entità nella sezione dati parametro|
|Numero modulo| Indica la forma, o la rappresentazione di questa entità. Modifica la modalità di interpretazione dei dati dei parametri. Il valore predefinito è 0|
|Campo riservato| Non utilizzato|
|Campo riservato| Non utilizzato|
|Etichetta entità| Identificatore specificato per l'applicazione - giustificato a destra|
|Numero pedice| Qualificatore numerico per l'etichetta dell'entità. Entrambi insieme formano un identificatore univoco per l'entità|
|Numero di sequenza Vedi sopra. |Questo sarà D#+1, poiché ogni entità è specificata su due righe.|

#### Sezione dati parametro
La sezione Inserimento dati è seguita dalla sezione Dati parametro. Elenca i dati per ogni rispettiva voce ed elenca i parametri per l'entità in base ai delimitatori specificati nella sezione Globale (di solito virgole per separare i parametri e un punto e virgola per terminare l'elenco).


## Riferimenti
* [IGES di WikiPedia](https://en.wikipedia.org/wiki/IGES)

