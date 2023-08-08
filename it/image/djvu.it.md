{
  "date" : "2019-10-11",
  "keywords" :[ "file djvu", "formato file djvu", "cos'è un file djvu", "file", "esempio djvu", "estensione file djvu", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file DJVU",
  "description":"Scopri il formato di file DJVU e le API che possono creare e aprire file DJVU.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file DJVU?

DjVu, pronunciato come "déjà vu", è un formato di file grafico destinato a documenti e libri scansionati, in particolare quelli che contengono la combinazione di testo, disegni, immagini e fotografie. È stato sviluppato da AT&T Labs. Utilizza più tecniche come la separazione del livello dell'immagine del testo e delle immagini di sfondo, il caricamento progressivo, la codifica aritmetica e la compressione con perdita di immagini bitonali. Poiché il file DJVU può contenere immagini a colori, fotografie, testo e disegni compressi ma di alta qualità e può essere salvato in meno spazio, quindi viene utilizzato sul Web come eBook, manuali, giornali, documenti antichi, ecc.

DjVu può essere considerato un'alternativa superiore a [PDF](/it/pdf/). Le estensioni dei file associate a DjVu sono .DJVU o .DJV. DjVu può ottenere rapporti di compressione di circa 5 – 10 migliori rispetto ai metodi esistenti come [JPEG](/it/image/jpeg/) e [GIF](/it/image/gif/) per documenti a colori e 3 – 8 volte migliori di [TIFF]( /image/tiff/) nei documenti in bianco e nero. I documenti scansionati a 300 DPI con colori fino a 25 MB possono essere compressi da 30 a 100 KB. Allo stesso modo, i documenti in bianco e nero possono essere compressi fino a 5-30 KB. La pagina HTML media può arrivare fino a 50 KB, quindi questi documenti possono essere caricati in rete senza alcun problema.

## Breve storia ##

La tecnologia DjVu è stata sviluppata nei laboratori AT&T da [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner e Paul G dal 1996 al 2001. Il formato del file DjVu ha subito varie revisioni, la più recente è del 2005.


|Versione|Data di rilascio|Note
---|---|---|
|1–19|1996–1999|Queste sono le versioni di sviluppo.
|20|Aprile 1999|La singola pagina è stata modificata in formato multipagina.
|23|luglio 2002|CID pezzo
|24|Febbraio 2003|LTAnno pezzo
|21|Settembre 1999|Formato di archiviazione indiretta sostituito. È stato aggiunto il livello di ricerca del testo.
|22|Aprile 2001|Orientamento della pagina, colore JB2
|25|Maggio 2003|Pezzo NAVM. È stato aggiunto il supporto per i segnalibri DjVu.
|26|Aprile 2005|Annotazioni di testo/riga

## Formato file DjVu ##

I documenti DjVu sono file IFF85. La struttura fornisce una gerarchia di contenitori che contengono informazioni in un file DjVu. Questi contenitori sono anche chiamati "pezzi". Il tipo di blocco e l'ID blocco descrivono come viene utilizzato il blocco. C'è un'intestazione di 4 byte seguita da una struttura IFF. I primi quattro byte di un file DjVu sono 0x41 0x54 0x26 0x54. Questa sezione discute i vari tipi di documenti DjVu e le parti corrispondenti di cui sono costituiti.


|ID blocco|Utilizzo
---|---|
|FORM|Il blocco composto con i primi quattro byte di dati del blocco FORM che sono identificatori secondari.
|FORM:DJVM|Un documento DjVu multipagina. Blocco composito che contiene il blocco DIRM.
|FORM:DJVU|Documento DjVu a pagina singola. Pezzo composito che contiene i frammenti che compongono una pagina in un documento djvu.
|FORM:DJVI|Un file DjVu "condiviso" incluso tramite il blocco INCL. Annotazioni condivise e dizionario delle forme.
|FORM:THUM|Pezzo composito che contiene i blocchi TH44 che sono le miniature incorporate.
|DIRM|Informazioni sul nome della pagina per documenti a più pagine.
|NAVM|Informazioni sui segnalibri
|ANTa, ANTz|Annotazioni che includono sia le impostazioni della vista iniziale che i collegamenti ipertestuali sovrapposti, le caselle di testo, ecc.
|TXTa, TXtz|Unicode Informazioni su testo e layout.
|Djbz|Tabella di forma condivisa.
|Sjbz|Dati bitonali JB2 compressi BZZ utilizzati per memorizzare la maschera.
|FG44|Dati IW44 utilizzati per memorizzare in primo piano
|BG44|Dati IW44 utilizzati per memorizzare lo sfondo
|TH44|Dati IW44 utilizzati per memorizzare le immagini di anteprima incorporate
|WMRM|Dati JB2 necessari per rimuovere una filigrana
|FGbz|Dati colore JB2. Fornisce un colore per ciascuno (blit o forma?) nel blocco Sjbz corrispondente.
|INFO|Informazioni sulla pagina a DjVu
|INCL|L'ID di un blocco FORM:DJVI incluso.
|BGjp|Sfondo codificato JPEG
|FGjp|Primo piano codificato JPEG
|Smmr|Maschera codificata G4

### Compressione DJVU

La singola immagine è divisa in molte immagini diverse, quindi ogni immagine viene compressa separatamente. Per la creazione di un file DjVu l'immagine viene prima divisa in tre immagini, una di sfondo, un primo piano e un'immagine di maschera. In genere le immagini di sfondo e in primo piano sono immagini a colori a risoluzione inferiore; ma l'immagine della maschera è un'immagine a risoluzione più alta e in genere il testo viene archiviato lì. Dopo la separazione, le immagini di primo piano e di sfondo vengono compresse tramite un algoritmo di compressione basato su wavelet IW44, mentre l'immagine della maschera viene compressa utilizzando un altro metodo chiamato JB2.

Il metodo di codifica JB2 elimina gran parte della ridondanza nell'immagine del testo identificando forme identiche sulla pagina, ad esempio più occorrenze di un carattere in un particolare font. JB2 codifica innanzitutto la bitmap di ogni forma univoca sfruttando la ridondanza tra forme simili. Quindi codifica le posizioni in cui ciascuna forma appare sulla pagina. Sia JB2 che IW44 si basano su un nuovo tipo di codificatore aritmetico binario adattivo chiamato ZP-coder che elimina qualsiasi ridondanza rimanente entro una piccola percentuale del limite di Shannon. Il codificatore ZP è adattivo e più veloce di altri codificatori aritmetici binari approssimativi.

## Riferimenti ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [Formato file DjVu](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

