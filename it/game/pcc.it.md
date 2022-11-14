{
  "date" : "2021-09-08",
  "keywords" :[ "file pcc", "formato file pcc", "cos'è un file pcc", "file", "esempio pcc", "estensione file pcc", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Ulteriori informazioni sul formato di file PCC di Mass Effect e sulle API che possono creare e aprire file PCC.",
  "title" :"PCC - File del pacchetto Mass Effect",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Che cos'è un file PCC?

Un file con .pcc è un file [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) che contiene dati di gioco per modificare il contenuto del gioco come modelli, trame e camere. Mass Effect 2 e 3 sono i primi giochi sparatutto basati sul motore di gioco Unreal Engine 3. Il gioco è stato inizialmente sviluppato da [Bioware](https://www.bioware.com/about/) che ha mantenuto la maggior parte delle risorse di gioco nel proprio formato di file PCC proprietario. Bioware è stata acquisita da Electronic Arts, uno dei principali editori di intrattenimento interattivo a livello mondiale.

## Formato file PCC - Ulteriori informazioni

I file PCC contengono strutture compresse e/o non compresse che contribuiscono all'organizzazione generale dei file.

### Struttura PCC compressa

Un file PCC compresso comprende tabelle e dati segmentati in blocchi. Ogni blocco contiene un numero variabile di blocchi compressi.

* `Chunks Header` - Un'intestazione comune di 16 byte, contenente informazioni sui blocchi.
* `Chunk Header` - Un'intestazione di 16 byte contenente informazioni sui dati compressi grezzi contenuti nel modulo di blocco.

### Struttura PCC non compressa

I file PCC non compressi sono divisi nelle seguenti cinque parti.

* `Header` - contiene informazioni di base sulla struttura del file PCC.
* `Tabella dei nomi` - contiene il nome trovato all'interno del pacchetto, comprese le classi di importazione, le esportazioni e le proprietà di esportazione.
* `Importa tabella` - contiene tutte le classi e gli oggetti importati dal PCC.
* `Export Table` - contiene tutti gli oggetti archiviati nel pacchetto. Ogni esportazione può variare in termini di dimensioni.

## Riferimenti

* [Me3Explorer - Formato file PCC](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Gioco Mass Effect](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)

