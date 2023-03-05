{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Formato file", "Apri", "Leggi", "Crea", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file DWF e le API che possono creare e aprire file DWF.",
  "title" :"Formato file DWF",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file DWF?

Design Web Format (DWF) rappresenta il disegno 2D/3D in formato compresso per la visualizzazione, la revisione o la stampa di file di progettazione. Contiene grafica e testo come parte dei dati di progettazione e riduce le dimensioni del file grazie al suo formato compresso. Le dimensioni ridotte del file rendono efficiente la distribuzione e la comunicazione di dati di progettazione avanzati. DWF non richiede al destinatario di conoscere l'utilizzo del software CAD che ha creato il disegno originale. Il contenuto del formato file DWF può essere semplice e includere solo un singolo foglio o abbastanza complesso da contenere caratteri, colori e immagini.

## Breve storia ##

Autodesk ha introdotto il formato di file DWF nel 1995 come parte del plug-in Netscape Navigation, WHIP. Il formato si è evoluto dal formato solo 2D per includere contenuti 3D con il passare del tempo. Anche molte applicazioni di terze parti utilizzano questo formato.

## Formato file DWF ##

DWF è un formato aperto e sicuro progettato specificamente per la condivisione di dati di progettazione ingegneristici avanzati. È indipendente dal software applicativo originale, dall'hardware e dal sistema operativo utilizzati per creare i dati di progettazione. Ciò consente ai membri del team che non utilizzano applicazioni CAD di partecipare ai processi digitali visualizzando edifici, GIS o progetti di prodotti. Un archivio di file DWF è costituito da diversi file XML e binari che sono impacchettati insieme in un archivio compresso creato con la compressione [ZIP](/it/compression/zip/). È possibile rinominare un'estensione di file DWF in ZIP e visualizzare il contenuto del file. Il pacchetto DWF può contenere molti tipi di dati di progettazione come grafica 2D, grafica 3D, metadati di pacchetti e sezioni e altri file di risorse.

**File di metadati DWF**: file XML che contengono informazioni relative ai metadati e alla struttura (autore, titolo, ora di creazione, dipendenze delle sezioni, ordinamento delle sezioni, descrizioni dei file di risorse, ruoli, tipi MIME, ecc.) e relative alla sezione (pagina informazioni, metadati di progettazione, ecc.). I metadati strutturali vengono utilizzati per creare oggetti logici (raccolte di file per rappresentare una parte o una pagina, ecc.).

**File di risorse** – file multimediali o altri file di contenuto a cui si fa riferimento dai metadati del pacchetto/sezione e di solito sono presentazioni di dati di progettazione in vari formati (ZGL, W2D, [JPG](/it/image/jpeg/), [PNG](/it/image/png/), AVI, XML, [TXT](/it/elaborazione testi/txt/), [DOC](/it/elaborazione testi/doc/), ecc.)

### Dettagli formato file ###

I file DWF sono organizzati in tre sezioni principali come mostrato di seguito.

* Intestazione di identificazione del file
* File di blocco dati
* Trailer di terminazione file

#### Intestazione identificatore file ####

L'intestazione dell'identificatore di file consente l'identificazione dei file DWF da parte delle applicazioni. Identifica inoltre quale versione delle specifiche DWF è stata utilizzata per la codifica del file. È un'intestazione di 12 byte che è organizzata come segue:


|Byte|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Carattere|(|D|W|F|(spazio)|V|0|0|.|3|0|)

Ecco un riassunto di questa tabella:

* I primi sei byte dell'intestazione rappresentano sempre caratteri ASCII "(DWF V"
* I seguenti 5 byte contengono informazioni sul numero di versione, ad es. "00.30" con il valore della versione principale e secondaria del formato

Le applicazioni che creano un file DWF devono specificare il numero di versione più basso possibile che un'applicazione di lettura deve supportare per utilizzare correttamente i dati.

#### Blocco dati file ####

Il blocco dati del file inizia dal 13° byte di un file DWF ed è una serie di coppie di codice operativo e operandi, come nella tabella seguente.

|Campo 1|Campo 2|Campo 3|Campo 4|Campo 5|Campo 5
--- | --- |--- | --- |--- | --- |
|codice operativo|operando|codice operativo|operando|codice operativo|operando

Un file DWF può contenere coppie opcode-operando come ASCII leggibile così come codice binario o una combinazione di entrambi. Tutte le operazioni DWF hanno una forma leggibile di codice operativo/operando ASCII e la maggior parte delle operazioni ha anche una forma codice operativo/operando binario codificato. I codici operativi sono in un singolo byte consentendo oltre 200 operazioni. ASCII esteso e binario esteso sono casi eccezionali. I valori di Opcodes possono variare da 0 a 255 con alcune eccezioni. Fatta eccezione per i due tipi speciali di codici operativi ASCII estesi e binari estesi, un lettore di file deve sapere come calcolare la lunghezza dell'operando.

##### Codici operativi proibiti #####

Le rappresentazioni ASCII per quanto segue non possono essere utilizzate come codici operativi:

Le seguenti rappresentazioni ASCII non possono essere utilizzate come codici operativi:

* Spazio (0x20)
* Scheda (0x09)
* Trattino (0x2D)
* Cifre ASCII 0-9 (0x30 - 0x39)
* Ritorno in carrozza (0x0D)
* Alimentazione di linea (0x0A)
* Virgolette singole (0x27)
* Virgolette doppie (0x22)
* Periodo (0x2E)
* Parentesi (0x28 e 0x29)
* Parentesi graffe (0x7B e 0x7D)
* Parentesi quadre (0x5B e 0x5D)
* Barra all'indietro (0x5C)

#### Trailer di interruzione del file ####

Il trailer di terminazione del file per DWF è semplicemente un codice operativo speciale che indica la fine del file. Alcune applicazioni possono memorizzare dati non DWF seguendo il codice operativo di terminazione. Il trailer è come mostrato di seguito:


|Byte|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Carattere|(|E|n|d|0|f|D|W|F|)

## Riferimenti ##

* [DWF - Di Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)
* [Formato dati WHIP](http://paulbourke.net/dataformats/whip/)
* [http://blogs.msdn.com/opc/archive/2009/05/18/adventures-in-packaging-episode-1.aspx](http://blogs.msdn.com/opc/archive/2009 /05/18/adventures-in-packaging-episode-1.aspx)

