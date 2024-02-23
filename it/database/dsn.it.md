{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Scopri il formato file DSN e le API che possono creare e aprire file DSN.",
  "title" : "Formato file DSN: file del nome di origine del database",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-it",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Cos'è un file DSN?

DSN sta per Nome origine dati ed è un formato di file utilizzato per memorizzare le informazioni di connessione al database. I file DSN vengono generalmente utilizzati insieme a ODBC (Open Database Connectivity) e consentono un facile accesso a un database specifico fornendo le informazioni necessarie per connettersi ad esso, come il nome del server, il nome utente e la password. Il file è solitamente in testo semplice e può essere creato e modificato utilizzando un editor di testo. Può essere utilizzato su vari sistemi operativi come Windows, Linux e Mac.

## Come creare un file DSN?

Il metodo per creare un file DSN può variare in base al sistema operativo e agli strumenti disponibili. I seguenti passaggi forniscono una panoramica generale del processo per la creazione di un file DSN su un sistema Windows.

1. Apri l'Amministratore origine dati ODBC cercando Origini dati ODBC nel menu Start.
2. Selezionare la scheda DSN di sistema e fare clic sul pulsante Aggiungi.
3. Seleziona il driver appropriato per il database a cui desideri connetterti e fai clic su Fine.
4. Inserisci le informazioni necessarie per connetterti al database, come il nome del server, il nome utente e la password.
5. Fare clic su OK per salvare il file DSN.

In alternativa, puoi creare manualmente un file DSN creando un file di testo semplice con estensione .dsn e inserendo le informazioni di connessione necessarie nel formato:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

È quindi possibile utilizzare il percorso di questo file come DSN nel codice/script per connettersi al database.

## Programmi che aprono il file DSN

Un file DSN è un file di testo semplice che memorizza le informazioni utilizzate per connettersi a un database, come il nome del server, il nome utente e la password. Viene generalmente utilizzato insieme a ODBC (Open Database Connectivity) per fornire un facile accesso a un database specifico.

Per aprire e visualizzare il contenuto di un file DSN, puoi utilizzare qualsiasi editor di testo come Blocco note, Sublime Text, Atom, ecc. Questi programmi ti permetteranno di aprire il file DSN e visualizzare le informazioni di connessione memorizzate al suo interno.

Tuttavia, per utilizzare il file DSN per connettersi a un database ed eseguire operazioni come SELECT, INSERT, UPDATE, DELETE ecc., è necessario un programma con supporto ODBC, come un linguaggio di programmazione come Python, Java, C# o uno strumento di gestione di database come Microsoft Access , è richiesto SQL Server Management Studio. Questi programmi possono utilizzare le informazioni nel file DSN per connettersi al database ed eseguire l'operazione desiderata.

## Riferimenti

* [Che cos'è un DSN (nome origine dati)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



