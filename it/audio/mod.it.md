{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "file", "estensione", "format", "cos'è il formato file mod", "music", "formato file mod", "mod vs MP3", "specifica del formato file mod "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file MOD e le API che possono creare, convertire e aprire file MOD.",
  "title" :"MOD - File del modulo musicale",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## Che cos'è un file MOD?
Un file con estensione .mod è un file di modulo musicale creato utilizzando il formato del modulo musicale standard, basato sul **formato del modulo Amiga** sviluppato da Karsten Obarski e rilasciato con il software **Ultimate Soundtracker** per Commodore Sistema Amiga. Simile a un file [MIDI](/it/audio/mid/), è costituito da pattern di note e campioni di suoni, che rappresentano diversi strumenti che vengono riprodotti in base alle note. I file MOD sono particolarmente utilizzati nei videogiochi come musica di sottofondo e nella sottocultura della computer art **demoscene**.

## Formato file MOD

Il MOD è un formato di file per computer utilizzato la sua funzione di base è rappresentare la musica ed è stato il primo formato di file del modulo. I file MOD utilizzano l'estensione del file .mod, ad eccezione di **Amiga** che legge l'intestazione di un file per determinare il tipo di file, quindi non si basa sulle estensioni dei nomi dei file. Un file MOD è costituito da un insieme di vari strumenti sotto forma di campioni, un numero di pattern che specificano come e quando i campioni devono essere riprodotti e un elenco di quali pattern suonare in quale ordine.

### Specifiche del formato file MOD

Un modello di file MOD è effettivamente progettato in un'interfaccia utente del sequencer come una tabella con una colonna per canale, quindi questa tabella ha quattro colonne (una per ogni canale hardware Amiga. Ogni colonna ha 64 righe).

Una cella nella tabella può far sì che una delle seguenti azioni avvenga sul canale della sua colonna quando viene raggiunta l'ora della sua riga:

- Avvia uno strumento suonando una nuova nota in questo canale a un determinato volume, possibilmente con un effetto speciale applicato su di esso
- Modifica il volume o l'effetto speciale applicato alla nota corrente
- Cambiare il flusso del modello; saltare a una posizione specifica di un brano o di un pattern o eseguire un loop all'interno di un pattern
- Fare niente; qualsiasi nota esistente in riproduzione in questo canale continuerà a essere riprodotta

Uno strumento è un singolo campione insieme a una specifica opzionale di quale parte del campione può essere ripetuta per contenere una nota solida.

### Tempi
L'intervallo di tempo minimo era di 0,02 secondi nel file MOD originale, o un intervallo di "soppressione verticale" (VSync), perché il software originale utilizzava la temporizzazione VSync del monitor in esecuzione a 50 Hz (per PAL) o 60 Hz (per NTSC) per tempismo.

## Riferimenti

* [MOD (formato file) - Di Wikipedia](https://en.wikipedia.org/wiki/MOD_(file_format))

