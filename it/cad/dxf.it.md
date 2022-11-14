{
  "date" : "2020-03-16",
  "keywords" :[ "File DXF", "Formato file", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file DXF e le API che possono creare e aprire file DXF.",
  "title" :"Formato file DXF",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file DXF?

DXF, Drawing Interchange Format, o Drawing Exchange Format, è una rappresentazione di dati con tag del file di disegno di AutoCAD. Ogni elemento nel file ha un numero intero di prefisso chiamato codice di gruppo. Questo codice di gruppo rappresenta effettivamente l'elemento che segue e indica il significato di un elemento di dati per un determinato tipo di oggetto. DXF consente di rappresentare quasi tutte le informazioni specificate dall'utente in un file di disegno.

Il formato di file DXF è stato sviluppato da Autodesk come formato di file di dati CAD per l'interoperabilità dei dati tra AutoCAD e altre applicazioni. Pertanto, i dati possono essere importati da altri formati in DXF in AutoCAD secondo le specifiche di interoperabilità del formato di file DXF.

## Breve storia ##


La storia del formato di file DXF risale al 1982, quando fu introdotto come parte di AutoCAD 1.0. Le versioni iniziali di AutoCAD supportano solo il formato di file ASCII di DXF. Con la versione 10 di AutoCAD (e successive) nel 1988, in AutoCAD è stato introdotto il supporto sia per il formato di file ASCII che per quello binario DXF. Nelle fasi precedenti, Autodesk non condivideva alcuna specifica del formato di file e, per questo motivo, l'importazione corretta dei file DXF non era facile. Tuttavia, Autodesk ora pubblica le specifiche DXF e le rende disponibili al pubblico.

## Specifiche del formato file ##

Il formato file DXF utilizza il codice di gruppo e le coppie di valori per organizzare i contenuti in sezioni. Ogni sezione è composta da record in cui ogni record è costituito da un codice gruppo e da un elemento di dati. Ogni codice e valore di gruppo si trovano sulla propria riga nel file DXF. Ogni sezione inizia con un codice gruppo 0 seguito dalla stringa SECTION. Segue un codice gruppo 2 e una stringa che indica il nome della sezione (ad esempio SEZIONE1). Ogni sezione è composta da codici di gruppo e valori che ne definiscono gli elementi. Una sezione termina con uno 0 seguito dalla stringa ENDSEC.

Il formato file DXF considera gli oggetti diversi dalle entità. Gli oggetti non hanno una rappresentazione grafica qui, ma le entità ce l'hanno. Pertanto, le voci in DXF sono indicate come oggetti grafici mentre gli oggetti oggetti sono indicati come oggetti non grafici. Le sezioni BLOCCO ed ENTITÀ del file DXF contengono entità e l'uso dei codici di gruppo in queste due sezioni è identico. La fine di un'entità è indicata dal successivo gruppo 0, che inizia l'entità successiva o indica la fine della sezione.

### Struttura del file ###

Le sezioni in un file DXF sono disposte nel seguente ordine:

|Sezione|Descrizione di base
---|---|
|Intestazione|Questa sezione contiene informazioni generali sul disegno. È come la funzionalità Impostazioni nel telefono, che contiene le diverse variabili associate al disegno e ai valori associati. Ad esempio, la sezione Intestazione definirà quale versione di AutoCAD utilizza il file DXF (la variabile $ACADVER) o l'unità utilizzata per misurare gli angoli nel file (la variabile $AUNITS)
|Classes|La sezione CLASSES contiene le informazioni per le classi definite dall'applicazione le cui istanze appaiono nelle sezioni BLOCKS, ENTITIES e OBJECTS del database.
|Tabelle|Questa sezione contiene le definizioni per diverse tabelle, ognuna delle quali contiene un numero di voci di simboli differenti. Ad esempio il [tipo di riga](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2016/ENU/AutoCAD-Core/files/GUID-20B4D4B3-1220-426A- La tabella 847B-5BBE36EC6FDF-htm.html) (LTYPE) definisce il modello di trattini, punti, testo e simboli nel file DXF e come vengono ridimensionati. Ecco un elenco completo delle tabelle presenti in questa sezione:<ul><li> Tabella ID applicazione (APPID).</li><li> Tabella dei record di blocco (BLOCK_RECORD).</li><li> Tabella Stile quota (DIMSTYPE).</li><li> Tabella Layer (LAYER).</li><li> Tabella dei tipi di linea (LTYPE).</li><li> Tabella dello stile del testo (STYLE).</li><li> Tabella del sistema di coordinate utente (UCS).</li><li> Visualizza (VISUALIZZA) tabella</li><li> Tabella di configurazione della vista (VPORT).</li></ul>
|Blocchi|Questa sezione contiene gli oggetti grafici e le entità di disegno che costituiscono ogni riferimento di blocco nel disegno.
|Entità|Questa sezione contiene i dati degli oggetti effettivi e le entità grafiche del disegno. Ciò può includere dati grezzi, ad esempio un'entità cerchio è definita dal suo spessore, dal punto centrale, dal raggio e dalla direzione di estrusione.
|Oggetti|Qui troverai le parti non grafiche del disegno. Ad esempio, i dizionari AutoCAD sono archiviati qui.

## Riferimenti ##

* [Specifiche del file DXF](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF di Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)

