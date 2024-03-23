{
  "date" : "2019-10-11",
  "keywords" :[ "file rtf", "formato file rtf", "cos'è un file rtf", "file", "esempio rtf", "estensione file rtf", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF - Rich Text Format",
  "description":"Scopri il formato di file RTF e le API che possono creare e aprire file RTF.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file RTF?

Introdotto e documentato da Microsoft, il Rich Text Format (**RTF**) rappresenta un metodo di codifica di testo e grafica formattati da utilizzare all'interno delle applicazioni. Il formato facilita lo scambio di documenti multipiattaforma con altri prodotti Microsoft, servendo così lo scopo dell'interoperabilità. Questa capacità lo rende uno standard per il trasferimento di dati tra software di elaborazione testi e, quindi, i contenuti possono essere trasferiti da un sistema operativo all'altro senza perdere la formattazione del documento. Le specifiche del formato file sono disponibili da Microsoft per il download pubblico e possono essere richiamate dal punto di vista dello sviluppatore.

## Breve storia del formato file RTF ##

Il formato del file RTF ha subito diverse revisioni dalla sua pubblicazione. La sua versione ufficiale per lettura/scrittura è stata pubblicata come parte di Microsoft Word 3.0 per Macintosh con le specifiche della versione 1.0. La versione finale delle specifiche, 1.9.1, è stata pubblicata da Microsoft nel marzo 2008. Successivamente non vengono apportati ulteriori miglioramenti alle specifiche. Al momento, quasi tutti i sistemi operativi hanno applicazioni più ricche di funzionalità che hanno ridotto al minimo/eliminato l'uso del formato file RTF.

## Specifiche del formato file RTF ##

RTF funge da standard per il trasferimento di dati tra il software di elaborazione testi e il trasferimento di contenuto da un sistema operativo all'altro. Ciò si ottiene utilizzando parole di controllo introdotte da Microsoft Office Word fino al 2007. Un file RTF standard è costituito da ASCII per rappresentare il testo RTF e con caratteri non ASCII che vengono convertiti in valori di codice appropriati. Le versioni più recenti di Word possono leggere i file RTF generati con le versioni precedenti, mentre le versioni precedenti ignorano le parole di controllo e i gruppi che non comprendono.

### Comprendere i fondamenti di RTF ###

I file RTF utilizzano testo normale ASCII a 7 bit, composto da:

* parole di controllo
* simboli di controllo e
* gruppi.

Questi fungono da elementi costitutivi per la rappresentazione dei dati RTF come testo comprensibile e codifica dei caratteri.

#### Parola di controllo ####

Questi rappresentano un comando formattato in modo speciale utilizzato per contrassegnare i caratteri per la visualizzazione e non possono essere più lunghi di 32 lettere. Una parola di controllo è definita da:

\<ASCII Letter Sequence> //<//Delimiter//> //

Ogni parola di controllo fa distinzione tra maiuscole e minuscole e inizia con una barra rovesciata. La sequenza di lettere ASCII può contenere alfabeti ASCII (dalla a alla ze dalla A alla Z). Il<Delimite> segna la fine del nome della parola di controllo e può essere una delle seguenti:

* Uno spazio. Questo serve solo a delimitare una parola di controllo e viene ignorato nell'elaborazione successiva.
* Una cifra numerica o un segno meno ASCII, che indica che un parametro numerico è associato alla parola di controllo. La successiva sequenza digitale viene quindi delimitata da qualsiasi carattere diverso da una cifra ASCII (comunemente un'altra parola di controllo che inizia con una barra rovesciata). Il parametro può essere un numero decimale positivo o negativo. L'intervallo dei valori per il numero è nominalmente compreso tra –32768 e 32767, ovvero un intero a 16 bit con segno. Un piccolo numero di parole di controllo assume valori nell'intervallo‌ da −2.147.483.648 a 2.147.483.647 (intero con segno a 32 bit). Queste parole di controllo includono **\binN**, **\revdttmN//**, **\rsidN** parole di controllo correlate e alcune proprietà dell'immagine come **\bliptagN**. Qui **N** sta per il parametro numerico. Un parser RTF deve consentire fino a 10 cifre precedute facoltativamente da un segno meno. Se il delimitatore è uno spazio, viene scartato, ovvero non viene incluso nell'elaborazione successiva.
* Qualsiasi carattere diverso da una lettera o una cifra. In questo caso, il carattere di delimitazione termina la parola di controllo e non fa parte della parola di controllo. Ad esempio una barra rovesciata "\", che significa che segue una nuova parola di controllo o un simbolo di controllo.

#### Simbolo di controllo ####

Un simbolo di controllo rappresenta un'occorrenza speciale che ha un significato specifico a seconda del suo contenuto. Consiste in una barra rovesciata seguita da un carattere speciale (carattere non alfabetico) e non ha delimitatori.

#### Gruppo ####

Un gruppo può essere costituito da testo, parole di controllo o simboli di controllo racchiusi tra parentesi graffe (**{ }**). La parentesi graffa di apertura (**{** ) indica l'inizio del gruppo e la parentesi graffa di chiusura ( **}**) indica la fine del gruppo. Ciascun gruppo specifica il testo interessato dal gruppo e i diversi attributi di quel testo.

### Struttura del file RTF ###

Un file RTF ha la seguente sintassi Standard:

Introdotto e documentato da Microsoft, il Rich Text Format (**RTF**) rappresenta un metodo di codifica di testo e grafica formattati da utilizzare all'interno delle applicazioni. Il formato facilita lo scambio di documenti multipiattaforma con altri prodotti Microsoft, servendo così lo scopo dell'interoperabilità. Questa capacità lo rende uno standard per il trasferimento di dati tra software di elaborazione testi e, quindi, i contenuti possono essere trasferiti da un sistema operativo all'altro senza perdere la formattazione del documento. Le specifiche del formato file sono disponibili da Microsoft per il download pubblico e possono essere richiamate dal punto di vista dello sviluppatore.

#### Intestazione RTF ####

Un'intestazione RTF ha la seguente rappresentazione.

|Campo|Descrizione
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Le tabelle di intestazione devono essere visualizzate in questo ordine se esistono. Il file RTF può includere gruppi per caratteri, stili, colore dello schermo, immagini, note a piè di pagina, commenti (annotazioni), intestazioni e piè di pagina, informazioni di riepilogo, campi, segnalibri, proprietà di formattazione di documenti, sezioni, paragrafi e caratteri, matematica, immagini e oggetti. Se il tipo di carattere, il file, lo stile, il colore, il segno di revisione ei gruppi di informazioni di riepilogo e le proprietà di formattazione del documento sono inclusi nel file, devono apparire nell'intestazione RTF, che precede il corpo dell'RTF. Se il contenuto di un gruppo non viene utilizzato, il gruppo può essere omesso. Qualsiasi gruppo che utilizza le proprietà definite in un altro gruppo deve essere visualizzato dopo il gruppo che definisce tali proprietà. Ad esempio, le proprietà del colore e del carattere devono precedere il gruppo di stili.

#### Versione RTF ####

Un documento RTF deve iniziare con questi sei caratteri:

```
{\rtf1
```
dove 1 mostra il numero di versione RTF.

#### Set di caratteri ####

Dopo {\rtf1, il documento dovrebbe dichiarare quale set di caratteri utilizza. Il modo per dichiarare un set di caratteri è con uno di questi comandi:

`\ansi` - Il documento si trova nel set di caratteri ANSI, noto anche come Code Page 1252, il solito set di caratteri di MSWindows.

`\mac` - Il documento si trova nel set di caratteri MacAscii, il solito set di caratteri nelle versioni precedenti (pre-10) di Mac OS.

`\pc` - Il documento è in DOS Code Page 437, il set di caratteri predefinito per MS-DOS. I dattilografi con una buona memoria muscolare noteranno che questo è il set di caratteri che viene ancora utilizzato per interpretare i codici "Alt numerici", ovvero, quando si tiene premuto Alt e si digita "130" sul tastierino numerico, viene prodotto un é, perché il carattere 130 in CP437 è un é. Questo è l'unico utilizzo che vede il CP437 in questi giorni.

`\pca` - Il documento è in DOS Code Page 850, noto anche come MS-DOS Multilingual Code Page.

#### Comando dei caratteri ####

La definizione del set di caratteri è seguita dal comando `\deffN`. Ciò definisce che il carattere numero N è il carattere predefinito per questo documento. Il numero del carattere N è riferito dalla tabella dei caratteri. Il comando `\deffN` è tecnicamente opzionale, ma dovrebbe essere lì per essere al sicuro come un prologo comune come il seguente seleziona il carattere 0 come carattere predefinito.

`{\rtf1\ansi\deff0`

#### Tabella dei caratteri ####

Tutti i caratteri che possono essere utilizzati in un documento sono elencati in una tabella dei caratteri in cui ogni carattere è rappresentato da un numero di carattere. Il documento deve avere una tabella dei caratteri anche se alcuni programmi funzioneranno anche senza.

La sintassi per una tabella di caratteri è {\fonttbl //...dichiarazioni//...}, in cui ogni dichiarazione ha questa sintassi di base:

`{\fnumber\familycommand Fontname;}`

Una tabella dei caratteri con quattro dichiarazioni è la seguente:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

In un documento con quella tabella dei caratteri, `{\f2 stuff}` stamperebbe "stuff" in Courier New. Un carattere non può essere utilizzato in un documento finché non viene elencato nella tabella dei caratteri.

### Fine del documento ###

Ogni documento RTF deve terminare con un }, per chiudere il gruppo aperto da { che è il primo carattere del documento. Nulla può seguire la finale }, tranne forse una nuova riga.

## Riferimenti ##

* [Rich_Text_Format](https://en.wikipedia.org/wiki/Rich_Text_Format)
