{
  "date" : "2021-07-08",
  "keywords" :["HAR", "File", "Estensione", "Formato file", "Estensione file", "JSON", "File archivio"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - Formato file di archivio HTTP",
  "description" :"La tua guida al formato di file per sapere cos'è un file HAR e le API in grado di creare e aprire file HAR.",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## Che cos'è un file HAR?

Un file con .har ([HTTP](/it/web/http/) Archive) è un file di archivio HTTP che memorizza i dati della sessione che vengono trasferiti su molti browser (come Chrome, Safari, IE, Firefox, ecc.) in [JSON](/it/web/json/) formato di file. I dati trasferiti su Internet tra il server e il client (in questo caso il browser dell'utente) contengono richieste HTTP e intestazioni di risposta memorizzate nel file HAR. Contiene inoltre informazioni dettagliate sui dati sulle prestazioni delle pagine Web caricate nel browser. I file HAR possono essere aperti in qualsiasi editor di testo come Blocco note su Microsoft Windows OS e TextEdit su Apple MacOS.

## Formato file HAR - Ulteriori informazioni

I file HAR memorizzano le informazioni sulla sessione in file di testo normale utilizzando il popolare formato JSON. Le specifiche per il formato di file HAR sono state prodotte dal Web Performance Group del World Web Consortium (W3C) ma non possono essere pubblicate. Tuttavia, ha definito correttamente un formato di archiviazione per le transazioni HTTP.

Oltre a monitorare il trasferimento delle informazioni di richiesta e risposta, i file HAR vengono utilizzati dagli sviluppatori per registrare le prestazioni del browser Web in termini di velocità di caricamento della pagina, durata del caricamento del contenuto, caricamento del contenuto, query eseguite per ottenere la risposta dal browser e molti altri .

## Perché usare i file HAR?

I file HAR possono essere utili per migliorare le prestazioni di un sito Web valutando lunghi tempi di caricamento, tempi di rendering della pagina e tempi di risposta. I file HAR possono essere analizzati per trovare tali problemi e risolvere eventuali problemi con il sito Web per migliorare le prestazioni.

## Come generare un file HAR?

Quindi, come generare un file HAR? Bene, questo dipende dal tipo di browser che stai utilizzando per generare un file HAR. In questa guida, elenchiamo i passaggi per il browser Google Chrome. I metodi per generare file HAR utilizzando Safari, Firefox, ecc. possono essere facilmente ricercati su Internet e seguiti.

### Passaggi per generare file HAR utilizzando Google Chrome

I seguenti passaggi possono essere eseguiti su una pagina Web in cui vengono affrontati problemi.

1. Apri la pagina web in Google Chrome dove si è verificato il problema.
1. Aprire lo strumento di sviluppo (ispeziona elemento).
1. Vai a sinistra del pannello per avviare la registrazione del file. C'è un piccolo pulsante rosso rotondo in questa sezione.
1. Fare clic su "Cancella icona" per eliminare tutti i record di registro conservati nel browser.
1. Per salvare il contenuto desiderato come mostrato sopra, fare clic con il pulsante destro del mouse e fare clic su "Salva come file HAR"

## Riferimenti

* [Formato file HAR - Wikipedia](https://en.wikipedia.org/wiki/HAR_(formato_file))

