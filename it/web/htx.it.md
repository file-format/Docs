{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File HTX - Formato file estensione HTML",
  "description" :"La tua guida al formato file per sapere cos'è un file HTX e le API in grado di creare e aprire file HTX.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file HTX?

Un file HTX è in realtà un file HTML che contiene variabili di dati per visualizzare i risultati della query del database come pagina Web. Per lo più creati con il software di sviluppo Web Microsoft FrontPage, i file HTX vengono salvati per essere salvati nella stessa cartella del corrispondente file Internet Database Connector (.IDC).

I file HTX possono essere aperti con applicazioni come Microsoft FrontPage e qualsiasi editor di testo come Blocco note, TextEdit o Atom.

## Formato file HTX

I file HTX vengono salvati come file di testo normale con il codice per recuperare i dati da un database e salvare le variabili per la visualizzazione.


### Esempio di file HTX

Un esempio di file HTX è il seguente che definisce un'intestazione di pagina per visualizzare la restrizione della query e i documenti visualizzati sulla pagina per la visualizzazione all'utente.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

L'output di questo codice di esempio è il seguente.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Come si può vedere, il file HTX è un modello che formatta il modo in cui i risultati vengono restituiti e visualizzati agli utenti finali. È scritto nel formato HTML con alcune estensioni IIS e il servizio di indicizzazione. Queste estensioni includono nomi di variabili e altri codici per l'elaborazione dei risultati.

## Riferimenti

* [Formattazione dei risultati nel file .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

