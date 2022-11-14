{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "estensione", "file", "formato", "sistema", "file LNK", "link", "file LNK", "documenti LNK", "applicazione", "programmi" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Formato file di collegamento",
  "description":"Scopri il formato di file LNK e le API che possono creare e aprire file LNK.",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Che cos'è un file LNK? ##

Un file LNK, analogo a un'identità sul sistema Mac, è un'alternativa o "collegamento" di Windows che funge da connessione a una cartella o programma di un documento immagine originale. Contiene il tipo, la posizione e il nome file della destinazione del collegamento, nonché l'applicazione che apre il documento di destinazione e un tasto di scelta rapida aggiuntivo.

In Windows, seleziona un file, una cartella o un programma eseguibile e scegli Crea collegamento. La posizione del formato del file e la directory "Inizio" sono due caratteristiche di base dei file LNK. Il formato dei file LNK è mascherato e una freccia curva indica che si tratta di scorciatoie.

## Formato file LNK ##

I formati di file LNK di solito hanno la stessa icona dei file di destinazione, ma con l'aggiunta di una piccola freccia arricciata per mostrare che il file punta a una posizione diversa. Quando si fa doppio clic sul collegamento, si comporta come se l'utente avesse fatto doppio clic sul file effettivo.

I file LNK contenenti collegamenti alle applicazioni possono avere proprietà che influiscono sull'esecuzione del programma. Per modificare gli attributi, fai clic con il pulsante destro del mouse sul file di collegamento e scegli **Proprietà**, quindi modifica il campo Destinazione.

Invece di essere estensioni di file, i file LNK sono estensioni di Windows Explorer. Come estensione del terminale, i documenti .lnk possono essere utilizzati solo in Esplora risorse per sostituire un file e hanno altri scopi in Esplora risorse oltre a fungere da collegamento a un documento locale. Anche questi file iniziano con la lettera "L".

Sebbene i collegamenti si colleghino a file e directory specifici quando vengono creati, potrebbero diventare inutilizzabili se la destinazione viene modificata in una posizione diversa. Explorer inizierà a riparare una cartella di collegamento che punta a una destinazione morta quando viene aperta.


## Specifiche tecniche ##

Solo quando l'impostazione di visualizzazione della cartella "Nascondi estensioni per tipi di file riconosciuti" è deselezionata, Windows non mostra l'estensione del documento .lnk per i collegamenti ai documenti. Sebbene non sia consigliabile, è possibile abilitare la visualizzazione dell'estensione del file rimuovendo la proprietà "NeverShowExt" dall'elemento del registro di Windows del file HKEY_CLASSES_ROOT\lnk.

Per farlo, segui questi passaggi:

* Apri "Editor registrazione" inserendo "Regedit" nel campo di ricerca della barra delle applicazioni e scegliendo il programma
* Nell'applicazione, vai alla posizione del file Computer\HKEY HKEY_CLASSES_ROOT\lnk
* Esegui un backup dell'elemento facendo clic con il pulsante destro del mouse e scegliendo Esporta
* Seleziona ed elimina l'attributo "NeverShowExt".
* Windows dovrebbe essere riavviato


## Riferimento ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
