{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file TEX",
  "description":"Scopri il formato di file TEX e le API che possono creare e aprire file TEX.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file TEX? ##

**TeX** è un linguaggio che comprende funzioni di programmazione e di markup, utilizzate per comporre i documenti. Donald Knuth della Stanford University, è il creatore di questo ingegnoso sistema di composizione. In tutto il mondo, TeX è la scelta definitiva di autori ed editori per produrre documenti tecnici di alta qualità. TeX esegue un lavoro eccezionale nella formattazione di espressioni matematiche complesse. In combinazione con una fotocomposizione di alta qualità, TeX compete i risultati generati dai migliori sistemi di composizione tradizionali. Pertanto considerato come il più classico dei sistemi tipografici digitali.

I file di input TeX sono basati su codice ASCII, consentendo così la condivisione del manoscritto tra scrittori, editori e critici. Un'ampia varietà di ambienti informatici, quasi tutte le piattaforme moderne e molte piattaforme meno recenti supportano TeX. Inoltre, TeX è un software gratuito, disponibile per un'ampia gamma di consumatori. Molte installazioni UNIX utilizzano sia UNIX troff che TeX come sistema di formattazione per scopi diversi. Altre attività di composizione vengono eseguite in modo straordinario sotto forma di LaTeX, ConTeXt e altri pacchetti di macro.

## Breve storia ##

TeX è stato progettato e scritto da Donald Knuth nel 1978. Guy Steele del Massachusetts Institute of Technology ha rivisto l'input/output di TeX per farlo funzionare con il sistema operativo incompatibile come Timeshaing System (ITS). La prima versione di TeX è stata sviluppata con il sistema operativo WAITS di Stanford nel linguaggio di programmazione (SAIL) e testata per funzionare su un PDP-10. Knuth ha introdotto l'idea di una programmazione alfabetizzata per le versioni avanzate. La programmazione alfabetizzata è un modo per generare codice sorgente compilabile e comporre (in TeX) per la documentazione con collegamenti incrociati utilizzando il file originale. Il linguaggio utilizzato per sviluppare queste versioni avanzate di TeX si chiama WEB, una combinazione di programmi DEC PDP-10 Pascal per garantire la portabilità.

Una nuova versione rivista di TeX pubblicata nel 1982 e si chiamava TeX82. Il cambiamento principale è la sostituzione dell'algoritmo di sillabazione originale con l'algoritmo appena scritto da Frank Liang. Per garantire la portabilità su piattaforme diverse, invece di utilizzare la virgola mobile, TeX82 utilizza l'aritmetica a virgola fissa insieme a un vero e proprio linguaggio di programmazione completo. Nel 1989 è stata rilasciata una nuova versione di TeX e Metafont. Quindi la versione 3.0 di TeX facilita gli input a 8 bit, consentendo 256 caratteri diversi nel testo. Dopo la versione 3, gli aggiornamenti sono indicati aggiungendo una cifra in più alla fine del decimale, ad esempio la versione corrente di TeX è indicata come 3.14159265. Questa versione è stata aggiornata l'ultima volta il 12-1-2014.

## TeX Input ##

Un file di input in TEX può essere preparato con un editor di testo utilizzando testo normale. A differenza di un tipico elaboratore di testi, questo file di input non consente alcun carattere di controllo invisibile. Un file può essere incorporato in un altro file, contenente definizioni di macro e definizioni ausiliarie che migliorano le capacità di TeX. Se un'installazione di TeX viene fornita con qualsiasi file di macro, le informazioni locali su TeX dimostrano l'utilizzo di file di macro. La forma standard di TeX integra una combinazione di macro e altre definizioni note come TEX semplice.

Sulla base della conoscenza precisa delle dimensioni di tutti i caratteri e simboli, calcola l'organizzazione ottimale delle lettere per riga e delle righe per pagina. Al momento dell'elaborazione del documento, viene prodotto un file .dvi, dove "dvi" sta per "indipendente dal dispositivo". I programmi del driver di dispositivo sono necessari per stampare o visualizzare in anteprima il documento con estensione dvi. Al giorno d'oggi, la generazione dvi è bypassata da un pdf-TeX comunemente usato. Non è disponibile alcuna conoscenza preliminare dei caratteri all'interno dell'installazione di TeX, quindi i file dei caratteri esterni, che fanno parte dell'ambiente TeX locale, vengono utilizzati per ottenere informazioni per il documento.

## Sistema di composizione ##

Circa 300 primitive (comandi) possono essere comprese dal sistema TeX di base. I primitivi sono comandi di basso livello, quindi un utente comune li usa raramente direttamente e la maggior parte delle funzionalità viene eseguita da file di formato. Questi file di formato sono immagini di memoria precaricate di TeX, seguite dal caricamento di grandi raccolte di macro. Il formato predefinito originale della lingua, ad esempio TeX semplice, aggiunge circa 600 comandi.

Una barra rovesciata raggruppata tra parentesi graffe denota l'inizio dei comandi TeX. Poiché TeX è un linguaggio basato su macro e token, quasi tutte le caratteristiche sintattiche di TeX possono essere modificate in fase di esecuzione, comprese quelle definite dall'utente, ad eccezione dei token non espandibili che vengono quindi eseguiti. L'espansione stessa è praticamente priva di problemi. Alcuni comandi devono venire dopo un argomento che aiuta a spiegare la funzione di un comando. Ad esempio, il comando \vskip indica a TEX di saltare/saltare la pagina seguito da un argomento che determina quanto spazio saltare.

## Versioni ##

LaTeX è il formato più utilizzato originariamente sviluppato da Leslie Lambport. LaTeX integra diversi stili di documento per file, lettere, libri e diapositive e offre riferimenti e numerazione automatica per diverse sezioni ed espressioni matematiche. AMS-TeX è un altro formato popolare, sviluppato dall'American Mathematical Society.

AMS-TeX offre comandi molto più intuitivi, che possono essere ridefiniti dai journal per adattarsi al loro stile locale. LaTeX può sfruttare i vantaggi di AMS-TeX utilizzando i "pacchetti" AMS che vengono quindi definiti come AMS-LaTeX. ConTeXt è un altro formato scritto da Hans Hagen utilizzato principalmente per il desktop publishing.

Il software TeX offre diverse funzionalità che non erano disponibili, o di qualità inferiore, in altri sistemi di composizione al momento della sua creazione. Alcune delle caratteristiche innovative di questo linguaggio si basano su interessanti algoritmi derivati dalle tesi degli studenti di Knuth. Mentre altri programmi di composizione stanno ora incorporando utili funzioni di TeX nei loro programmi.

## Riferimenti ##

* [Sistema di composizione di TeX](https://en.wikipedia.org/wiki/TeX)

