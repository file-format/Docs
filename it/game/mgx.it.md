{
  "date" : "2021-09-08",
  "keywords" :[ "file mgx", "formato file mgx", "cos'è un file mgx", "file", "esempio mgx", "estensione file mgx", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file MGX di Age of Empires 2 Expansion Replay e le API che possono creare e aprire file MGX.",
  "title" :"MGX - Riproduzione dell'espansione di Age of Empires 2",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Che cos'è un file MGX?

Un file con estensione .mgx è un file registrato per il gioco Age of Empires II: The Conquerors che può essere riprodotto all'interno del programma Age of Empires II. Contiene la registrazione completa della campagna giocata dall'utente. Può essere caricato e riprodotto all'interno del programma Age of Empires II. Una volta rigiocato, il gioco mostra tutti gli eventi e gli scenari che l'utente ha pianificato per la campagna e giocato.

## Formato file MGX - Ulteriori informazioni

Il formato del file interno del file MGX è stato elaborato e disponibile come informazione parzialmente convalidata su [Age of Empires 2: The Conquerors — Specifica del formato del file di Savegame](https://github.com/stefan-kolb/aoc-mgx- formato). Le specifiche delineano i dettagli nelle sezioni seguenti.

### Definizioni della struttura

Si ritiene che le definizioni della struttura del formato di file GPX siano basate sulle [dichiarazioni di BinData Ruby Gem](https://github.com/dmendel/bindata/wiki) che forniscono un modo per leggere e scrivere dati binari strutturati. Ciò consente al programmatore di specificare il formato dei dati binari che vengono quindi letti e scritti da BinData.

### Messaggistica MGX

La messaggistica MGX si basa su due tipi di messaggi.

* GAMESTART - specifica i comandi di inizio del gioco e non è convalidato fino ad oggi
* CHAT - descrive i messaggi di chat del gioco. Sia i giocatori che il gioco stesso (Gaia) possono emettere messaggi di gioco.

### AZIONI DI GIOCO

Ci sono diverse [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) che sono state recuperate e i cui dettagli sono disponibili.

## Riferimenti

* [Age of Empires 2: The Conquerors — Specifica del formato del file di salvataggio](https://github.com/stefan-kolb/aoc-mgx-format)

