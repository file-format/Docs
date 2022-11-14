{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - Layout pagina report",
  "keywords" :[ "rpl", "Layout pagina report", "XSD", "SQL Server", "report"],
  "description":"Ulteriori informazioni sul formato del flusso RPL, che è un formato binario interno utilizzato da Microsoft SQL Server Reporting Services quando si contattano i controlli del visualizzatore.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Che cos'è un file RPL? ##

Il formato di flusso RPL (Report Page Layout) è un formato binario interno utilizzato da MS SQL Server Reporting Services quando si contattano i controlli del visualizzatore per ridurre parte del lavoro di rendering dal server al controllo del visualizzatore client. Gli sviluppatori possono creare progettisti di report personalizzati utilizzando RPL, che genererà RPL e renderer di report personalizzati che elaborano e visualizzano il file RPL per visualizzare i report.

## Strutture RPL

Un flusso RPL include la struttura del flusso, la struttura del report, le proprietà del report e le enumerazioni. Ogni struttura include quanto segue:

- Una definizione della struttura.

- La grammatica Augmented Backus-Naur Form (ABNF) per la struttura.

- Un po' di diagramma della struttura.

- Definizioni di tutti i campi contenuti all'interno della struttura.

Di seguito sono riportate brevi note su alcune delle Strutture RPL:

### Struttura del flusso
La struttura del flusso consiste in una serie di record. Un record contiene zero o più campi strutturati che contengono il layout del report.

#### Flusso RPL
Il flusso RPL deve avere un solo record Report e il flusso deve essere una serie di record binari che mantengono la gerarchia del report.

#### Disco
Il record è un elemento costitutivo di base utilizzato per conservare le informazioni su un report. Un record è costituito da una sequenza di byte di lunghezza variabile. Un record è composto da due componenti:
- Un tipo di record
- I dati del record specifici per quel tipo di record.
Il tipo di record è un byte che definisce quale tipo di informazioni è specificato dal record e come è ordinata e strutturata la struttura dei dati del record relativi al record. Il valore del record dipende dal tipo di dati specifici di quel record.

#### Strutture di tipi di dati semplici

La tabella seguente definisce i tipi di dati in un flusso RPL.

|Descrizione| formato|
---|---|
|Char|Rappresenta un valore numerico (ordinale) a 16 bit (2 byte).|
|Byte|Rappresenta un intero senza segno a 8 bit (1 byte).|
|Int16|Rappresenta un intero con segno a 16 bit (2 byte).|
|Single|Rappresenta un valore in virgola mobile a precisione singola a 32 bit (4 byte).|
|Decimale|Rappresenta un tipo di dati a 128 bit (16 byte).|
|DateTime|Rappresenta una codifica a 64 bit (8 byte) di un valore di data e ora.|
|Int64|Rappresenta un intero con segno a 64 bit (8 byte).|
|Int32|Rappresenta un intero con segno a 32 bit (4 byte).|
|Float|Rappresenta un valore in virgola mobile a precisione singola a 32 bit (4 byte).|
|Booleano|Rappresenta un valore di tipo booleano logico a 8 bit (1 byte). I valori validi sono true (1) e false (0).|
|Long|Rappresenta un intero con segno a 64 bit (8 byte).|
|Stringa|Tutti i valori di stringa all'interno del protocollo DEVONO essere UNICODE UTF-16. Per impostazione predefinita, tutti i valori String iniziano con un numero intero che definisce la lunghezza della String. I valori di stringa sono rappresentati nel protocollo come una matrice di byte; il numero di byte DEVE essere uguale al numero di caratteri nella stringa moltiplicato per due.|

### Strutture dei rapporti
Le strutture del report includono le definizioni e le dimensioni delle loro strutture ed elementi rilevanti.

L'elenco seguente specifica le strutture del report:

- Rapporto
- Versione
- Proprietà del rapporto
- Elemento array offset
- Contenuto della pagina
- Pagina
- Proprietà della pagina
- Layout di pagina
- Sezione
- Sezione semplice
- Sezione Mista
- Proprietà della sezione
- Elemento Area Corporea
- Elemento di intestazione della pagina
- Elemento piè di pagina
- Elemento del corpo
- Proprietà dell'elemento
- Proprietà degli elementi condivisi
- Usa le proprietà degli elementi condivisi
- InlineSharedElementProperties
-Proprietà dell'elemento non condiviso
- Stile
- Proprietà di stile condiviso
- Proprietà di stile non condivise
- Informazioni sull'azione
-AzioneInfoContenuto
- Azione
-AzioneImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- Scostamento di consolidamento dell'immagine
- Segnala Item
- Linea
- Immagine
- Proprietà dei dati di immagine
- Usa SharedImageDataProperties
- InlineSharedImageDataProperties
- Non SharedImageDataProperties
- Dati immagine
- ImageMapAreas
- ImageMapArea
- Grafico
- Pannello di misurazione
- Carta geografica
- Rettangolo
- Sottorelazione
- RichTextBox
- ParagrafoContenuto
- TextRun
- Paragrafo
- Struttura RichTextBox
- Tablix
- Contenuto Tablix
- Struttura Tablix
- Misure Tablix
- Larghezza colonne
- Informazioni sulla colonna
- Altezza riga
- Informazioni riga
- Tablix Riga
- TablixRowCell
- Tablix Angolo
- Intestazione colonna Tablix
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Misure
- Misurazione
- ReportElementEnd

### Proprietà
Di seguito è riportato l'elenco delle proprietà che possono essere utilizzate in un flusso RPL:

- ID
- Conteggio colonne
- Spaziatura colonne
- Nome unico
- Nome
- Etichetta
- Segnalibro
- Suggerimento
- Attiva/disattiva oggetto
- Descrizione
- Posizione
- ConsumaContainerWhiteSpace (RPL 10.6)
- Lingua
- Tempo di esecuzione
- Autore
- Auto aggiornamento
- Nome rapporto
- Altezza pagina
- Larghezza pagina
- Margine superiore
- Margine Sinistro
- MargineDestra
- Margine in basso
- Colonne
- NomePagina (RPL 10.6)
- Inclinato
- Può crescere
- Può restringersi
- Valore
- Attiva/disattiva stato
- CanSort
- Stato di ordinamento
- Formula
- ÈToggleParent
- TipoCodice
- Valore originale
- È semplice
- Content Offset
- Nome flusso
- Dimensionamento
- LinkToChild
- Stampa sulla prima pagina
- Stampa tra sezioni (RPL 10.4)
- FormattedValueExpressionBased
- Elaborato con errore
- Tipo di immagineMIME
- Nomeimmagine
- Larghezza
- Altezza
- Risoluzione orizzontale
- Risoluzione verticale
- Formato grezzo
- Collegamento ipertestuale
- Collegamento ai segnalibri
- DrillthroughId
- DrillthroughUrl
- Colore del bordo
- Colore bordoSinistra
- BorderColorDestra
- BorderColorTop
- BorderColorBottom
- Stile del bordo
- Stile bordo a sinistra
- Stile bordo destro
- Stile bordo superiore
- Bordo stile bordo inferiore
- Larghezza del bordo
- Larghezza del bordo a sinistra
- Confine Larghezza Destra
- Larghezza bordo superiore
-BordiLarghezzaBasso
- Imbottitura Sinistra
- ImbottituraDestra
- Imbottitura Top
- Fondo imbottito
- Stile carattere
- Famiglia di font
- Dimensione del font
- FontWeight
- Formato
- Decorazione del testo
- Allineamento testo
- Allineamento verticale
- Colore
- Altezza della linea
- Direzione
- Modalità scrittura
- UnicodeBiDi
- Immagine di sfondo
- Colore di sfondo
- SfondoRipeti
- Linguaggio numerico
- Variante numerica
- Calendario
- ColumnHeaderRighe
- Colonne RowHeader
- ColsBeforeRowHeader
- LayoutDirection
- Definizione Percorso
- Livello
- MemberCellIndex
- CellItemOffset
- ColSpan
- RowSpan
- Definisci indice
-ColonnaIndice
- Indice di riga
- Etichetta di gruppo
- Livello di commutazione ricorsivo
- Stile elenco
- Livello elenco
- Numero di paragrafo
- Rientro destro
- Rientro sinistro
- Rientro sospeso
- Spazio prima
- SpaceAfter
- Prima linea
- Marcatura
- ContentTop
- Contenuto a sinistra
- Larghezza contenuto
- Altezza del contenuto
- Stato
- CellItemState
- MemberDefStato

### Enumerazioni
L'elenco seguente mostra le enumerazioni che possono essere utilizzate nel flusso RPL:

- Opzioni di ordinamento
- Taglie
- Tipo di forma
- ImageRawFormat
- Stili di carattere
- FontWeights
- Decorazioni di testo
- Allineamenti del testo
- Allineamenti verticali
- Indicazioni
- Modalità di scrittura
-Tipi UnicodeBiDi
- Calendari
- Stili di confine
- Tipi di ripetizione di sfondo
- ListStyles
- Stili di markup
- TipoCodice
- valori di stato
- TablixMemberStateValues
- TablixMemberDefStateValues
- Dimensione RPL





## Riferimenti ##

- [Formato di flusso binario del layout di pagina del report (RPL)](https://docs.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

