{
  "date" : "2019-10-11",
  "keywords" :[ "file u3d", "formato file u3d", "cos'è un file u3d", "file", "esempio u3d", "estensione file u3d", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - Formato file 3D universale",
  "description":"Scopri il formato di file U3D e le API che possono aprire e creare file U3D.",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file U3D?

**U3D** (Universal 3D) è un formato di file compresso e una struttura dati per la computer grafica 3D. Contiene informazioni sul modello 3D come mesh triangolari, illuminazione, ombreggiatura, dati di movimento, linee e punti con colore e struttura. Il formato è stato accettato come standard [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) nell'agosto 2005. I documenti 3D [PDF](/it/pdf/) supportano U3D incorporamento di oggetti e può essere visualizzato in Adobe Reader (versione 7 e successive).

Il formato U3D è stato sviluppato tenendo in considerazione l'obiettivo di stabilire uno standard universale per l'archiviazione e lo scambio di dati tridimensionali. Tuttavia, il formato trova il suo principale utilizzo nella codifica di PDF 3D piuttosto che essere utilizzato come formato di interscambio. Acrobat 3D converte un tipo di file 3D supportato in U3D o PRC dopo la conversione in PDF.

## Formato file U3D

I file U3D sono in formato file binario che ha subito quattro edizioni come descritto dal documento di riferimento [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/), con conseguente aggiornamento delle specifiche con ogni edizione. Lo standard di file PDF ISO-32000 accetta U3D come annotazione consentita e tipo multimediale.

La prima edizione di U3D era incentrata sulle rappresentazioni chiave delle proprietà grafiche 3D come la geometria, il colore, le trame, l'illuminazione, le ossa e l'animazione basata sulla trasformazione. La seconda e la terza edizione hanno corretto alcuni errata nella prima edizione, con la terza versione che era il tipo più comunemente usato nel software industriale. La quarta edizione fornisce definizioni per primitive di ordine superiore (superfici curve). [Specifiche U3D](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) sono disponibili online come riferimento per l'utente sul sito web ECMA.

### Tipi di dati nei file U3D

Il file binario conterrà i seguenti tipi: U8, U16, U32, U64, I16, I32, F32, F64 e String.

* U8 : un intero a 8 bit senza segno
* U16 : un intero a 16 bit senza segno
* U32 : un intero a 32 bit senza segno
* U64: un intero a 64 bit senza segno
* I16 : Un intero con segno a 16 bit
* F32: un float IEEE a precisione singola.
* F64: un float IEEE a doppia precisione.
* Stringa: le stringhe in un file U3D iniziano con un intero a 16 bit senza segno che definisce la lunghezza totale dei caratteri nella stringa. Le stringhe vengono sempre elaborate con distinzione tra maiuscole e minuscole.

## Struttura del file U3D

Un file U3D contiene una sequenza di blocchi. Ci sono 3 diversi tipi di blocco in ogni file U3D.

* Blocco intestazione file
* Blocco dichiarazione
* Blocco di continuazione

Il caricatore determina la fine di un blocco se i dati in quel blocco non sono richiesti o se non è disponibile un decoder per quel tipo di blocco.

{{< figure src="../u3d.png" alt="Formato file U3D" >}}

### Blocco intestazione file
Un blocco di intestazione di file contiene informazioni sul file che vengono utilizzate dal file caricato per determinare come leggere il file.

### Blocco dichiarazione

I blocchi di dichiarazione contengono informazioni sugli oggetti nel file. Gli oggetti in un blocco di dichiarazione devono essere definiti.

### Blocco di continuazione

Ulteriori informazioni per gli oggetti dichiarati in un blocco di dichiarazione sono fornite nel blocco successivo. Ogni Blocco di Continuazione deve essere associato ad un Blocco di Dichiarazione.


## Riferimenti ##

* [Formato file U3D - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [Specifiche del formato file ECMA U3D](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)