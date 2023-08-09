{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - File modello rapporto elisir",
  "description":"Ulteriori informazioni sul file RML e sulle API che possono creare e aprire file RML.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Che cos'è un file RML?

Un file RML è un file modello di report con il motore di report [Elixir Repertoire](https://elixirtech.com/repertoire-2/). Il file modello viene utilizzato per generare report con l'origine dati collegata all'Elixir FileSystem. I dati vengono letti e inseriti nel file modello RML e possono essere esportati in diversi formati di file come [PDF](/it/pdf/), [RTF](/it/elaborazione testi/rtf/) e foglio di calcolo [XLS](/it/foglio di calcolo/xls/). Il motore di reporting di Elixir Repertoire può essere collegato a un'ampia varietà di origini dati JDBC.

## Formato file RML

I dettagli della struttura dei file interni del formato file RML non sono disponibili pubblicamente. I file vengono generati e salvati internamente dall'applicazione Elixir Repertoire per generare report con i dati popolati dalle origini dati collegate. Il file modello RML contiene il layout generale e le informazioni sui segnaposto del report finale da generare dai dati.

## Come eseguire il file modello RML?

Per generare il modello RML in Elixir Repertoire, è possibile seguire i seguenti passaggi.

1. Collegare un'origine dati JDBC al file system.
1. Avviare la Creazione guidata modello di rapporto
1. Utilizzare il software per individuare il file .ds dell'origine dati
1. Scegli il rapporto tabulare come scelta di esportazione
1. Selezionare i campi da includere nel modello di rapporto
1. Infine, facendo clic sul pulsante Fine, First report.rml viene aggiunto al repository e aperto per mostrare la scheda Layout.

## Riferimenti

* [Repertorio elisir](https://elixirtech.com/repertoire-2/)

