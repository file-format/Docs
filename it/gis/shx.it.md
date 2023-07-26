{
  "date" : "2021-07-29",
  "keywords" :[ "file shx", "formato file shx", "cos'è un file shx", "file", "esempio shx", "estensione file shx", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - Formato dell'indice di forma dello shapefile",
  "description":"Scopri il formato di file SHX e le API che possono creare e aprire file SHX.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Che cos'è un file SHX?
Il file SHX appartiene al formato dell'indice di forma che è un indice di posizione della geometria della caratteristica per consentire la ricerca rapida in avanti e indietro. SHX è un file di offset ad accesso diretto. Non ci sono dati in questo file, solo una copia duplicata dei primi cento byte, numero di record e offset al byte iniziale di quel record nello shp. Si noti che il file con estensione .shx non lega [SHP](/it/gis/shp/) e [DBF](/it/database/dbf).

## Formato file SHX
Il formato SHX contiene l'indice di posizione della geometria dell'elemento e un'intestazione di 100 byte simile al file SHP, seguito da un numero qualsiasi di record a lunghezza fissa da 8 byte che contengono i due campi seguenti:
| byte | Digitare | Endianità | Utilizzo |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | grande | Scostamento record (in parole a 16 bit) |
| 4–7 | int32 | grande | Lunghezza del record (in parole a 16 bit) |

Questo indice consente di cercare all'indietro nello shapefile, prima cercando all'indietro nell'indice di forma e quindi leggendo l'offset del record. Tale offset può essere utilizzato per cercare la posizione corretta nel file SHP. Puoi anche cercare in avanti; un numero arbitrario di record utilizzando lo stesso metodo. Tuttavia, è possibile generare un indice completo insieme a un file SHP, ma può aumentare le possibilità di corrompere rapidamente il file SHP.


## Riferimenti

* [Shapefile - di Wikipedia)](https://en.wikipedia.org/wiki/Shapefile)


