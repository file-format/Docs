{
"data": "20-04-2023",
  "keywords": [
"file ldb",
"cos'è un file ldb",
"quali informazioni contiene ldb",
"qual è lo scopo del file ldb",
"estensione ldb",
"file",
"estensione"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file LDB - File di blocco di Microsoft Access",
  "description":"Scopri il formato LDB e quali informazioni contiene.",
"linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
"parent" : "misc"
}
},
"lastmod": "2023-04-20"
}

## Cos'è un file LDB?

Un file LDB è un file di blocco utilizzato da Microsoft Access per impedire a più utenti di modificare contemporaneamente lo stesso database. Quando l'utente apre un database di Access, Access crea un file LDB corrispondente nella stessa directory del database. Questo file contiene informazioni su chi sta attualmente utilizzando il database e quali record stanno modificando.

Il file LDB viene creato automaticamente da Microsoft Access all'apertura del database e viene eliminato alla chiusura del database. È importante notare che il file LDB non dovrebbe mai essere eliminato manualmente perché ciò potrebbe causare problemi con il database.

Se riscontri problemi con il database di Microsoft Access, una potenziale soluzione è provare a eliminare il file LDB associato a quel database. Ciò rilascerà eventuali blocchi che potrebbero impedirti di accedere al database. Tuttavia, assicurati di eseguire un backup del database prima di tentare questa operazione, poiché l'eliminazione del file LDB può causare la perdita o il danneggiamento dei dati se eseguita in modo improprio.

## Formato file LDB: ulteriori informazioni

Un file LDB in Microsoft Access contiene informazioni sugli utenti che stanno attualmente accedendo al database come nome utente, nome computer e ora di accesso. Il file LDB contiene anche informazioni su eventuali blocchi applicati al database, ad esempio quali record vengono modificati da quale utente.

Ecco un elenco più dettagliato dei tipi di informazioni che possono essere trovate in un file LDB:

- **Nome utente** - il nome dell'utente che sta attualmente accedendo al database
- **Nome computer** - il nome del computer da cui l'utente accede al database
- **Ora di accesso**: l'ora in cui l'utente ha aperto per la prima volta il database
- **Blocchi dei record**: informazioni su quali record sono attualmente modificati da quale utente
- **Blocchi oggetto**: informazioni su quali oggetti del database (come tabelle, moduli o report) sono attualmente modificati da quale utente
- **Informazioni sulla connessione**: informazioni su come l'utente è connesso al database (ad esempio, se utilizza una connessione locale o di rete)

Le informazioni nel file LDB vengono utilizzate da Microsoft Access per impedire a più utenti di apportare modifiche in conflitto allo stesso database contemporaneamente. Quando l'utente tenta di modificare un record o un oggetto già bloccato da un altro utente, Microsoft Access visualizzerà un messaggio che indica che l'oggetto è già in uso. Il file LDB viene aggiornato man mano che gli utenti aprono e chiudono il database e apportano modifiche agli oggetti bloccati.

## Riferimenti
* [Cos'è un file LDB?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

