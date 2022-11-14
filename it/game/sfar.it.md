{
  "date" : "2021-10-20",
  "keywords" :[ "file sfar", "formato file sfar", "cos'è un file sfar", "file", "esempio sfar", "estensione file DLC Mass Effect 3", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file SFAR di Mass Effect 3 e le API che possono creare e aprire file SFAR.",
  "title" :"SFAR - File DLC di Mass Effect 3",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Che cos'è un file SFAR?

Un file con estensione .sfar è un file di dati di gioco utilizzato da Mass Effect 3 per archiviare il suo DLC (contenuto scaricabile) in un archivio compresso e proprietario. Mass Effect 3 è un gioco creato da Electronic Arts, una delle principali società di sviluppo di giochi. Il contenuto DLC archiviato in un file SFAR viene utilizzato per estendere il gioco con contenuti e funzionalità aggiuntivi.

## Formato file SFAR - Ulteriori informazioni

I file SFAR vengono archiviati/salvati come file di archivio compressi in formato binario. Questi utilizzano algoritmi di compressione LZX e LZMA per comprimere i contenuti. I file SFAR possono essere aperti utilizzando l'editor DLC fornito con ME3 Explorer. Oltre a SFAR, DLC Editor può estrarre altri file di gioco come [PCC](/it/game/pcc/).

## Specifiche del formato file SFAR

Un file SFAR è diviso nei seguenti quattro blocchi principali.

### Intestazione SFAR

L'intestazione SFF contiene informazioni sui vari blocchi che compongono il file.

### Tabella file SFAR

La tabella dei file SFAR contiene un elenco di voci di file in cui ciascuna voce è lunga 30 byte.

### Tabella delle dimensioni del blocco

Block-Size contiene più voci, in cui ciascuna voce è lunga 2 bye. Questo valore specifica la dimensione del blocco corrispondente a una voce nella tabella file.

### Blocchi

I blocchi in un file SFAR contengono i dati all'interno del file SFAR.

## Riferimenti

* [Formato file SFAR DLC - Ricerca](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

