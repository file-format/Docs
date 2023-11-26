{
  "date" : "2023-06-14",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Informazioni sul formato file 4DL e sulle API in grado di creare e aprire file 4DL.",
  "title" :"4DL - File di registro del database di 4a dimensione",
  "linktitle" : "4DL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-06-14"
}

## Cos'è un file 4DL?

Un file di registro 4DL viene utilizzato per registrare le modifiche apportate a un file di database 4D (.4DD). Questo file viene archiviato insieme al file di database e condivide un nome file simile. Il suo scopo è tracciare e mantenere accuratamente un registro completo degli aggiornamenti implementati nel database. Un [file 4DD](/it/database/4dd/), rispetto al file 4DL, è principalmente associato alla Quarta Dimensione da parte della 4D Inc.

## Formato file 4DL: ulteriori informazioni

In genere, più file 4DL vengono archiviati insieme a un file 4DD. Pertanto la prima versione del file di registro potrebbe essere denominata 0001.4dl, ma le versioni laterali dei file di registro verranno salvate come 0002.4dl, 0003.4dl e così via. Ora, se il file di registro stesso viene sottoposto a 3 salvataggi successivi, verrà etichettato come "db1[0005-0003].4dl".

## Riferimenti

* [4DD - Wikipedia](https://en.m.wikipedia.org/wiki/4th_Dimension_(software))
