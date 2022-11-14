{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file KIT e le API che possono creare e aprire file KIT.",
  "title" :"Formato file KIT - File CodeKit",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Che cos'è un file KIT?

Un file con estensione .kit è un file HTML creato con l'applicazione del linguaggio di programmazione [CodeKit](https://codekitapp.com/). Contiene "importazioni" e "variabili" oltre ai file [HTML](/it/web/html/) esistenti, il che lo rende ideale per i siti statici. CodeKit compila i file KIT in HTML che possono essere facilmente utilizzati come file di siti Web statici.

## Formato file KIT

I file KIT sono file HTML che includono anche importazioni e variabili. Questi vengono archiviati come file di testo normale e possono essere aperti con qualsiasi editor di testo o editor di file Web.

### Importazioni di file KIT

Quasi tutti i tipi di file possono essere importati in un file Kit. Di seguito è riportata la sintassi di importazione utilizzata per importare i file in un file .kit.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Quando un'importazione viene aggiunta a un file KIT e salvata, viene sostituita con il testo del file da importare. Puoi anche usare @include invece di @import.

### Importazioni multiple in un file KIT

Puoi anche importare più di un file alla volta utilizzando un elenco separato da virgole:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Riferimenti

* [Cos'è il kit?](https://codekitapp.com/help/kit/)

