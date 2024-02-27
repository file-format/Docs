{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTX-fil - HTML-udvidelsesfilformat",
  "description": "Din filformatguide for at lære, hvad der er en HTX-fil og API'er, der kan oprette og åbne HTX-fil.",
  "linktitle": "HTX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ht-dax"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en HTX fil?

En HTX-fil er faktisk en HTML-fil, der indeholder datavariabler til visning af databaseforespørgselsresultaterne som en webside. For det meste oprettet med Microsoft FrontPage-webudviklingssoftware, gemmes HTX-filer for at blive gemt i samme mappe som den tilsvarende Internet Database Connector-fil (.IDC).

HTX-filer kan åbnes med programmer som Microsoft FrontPage og enhver teksteditor som Notepad, TextEdit eller Atom.

## HTX filformat

HTX-filer gemmes som almindelig tekstfil med kode til at hente data fra en database og gemme i variabler til visning.


### HTX-fileksempel

Et eksempel på HTX-fil er som følger, der definerer en sidehoved til visning af forespørgselsbegrænsningen og de dokumenter, der vises på siden til visning for brugeren.

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

Outputtet af denne eksempelkode er som følger.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Som det kan ses, er HTX-filen en skabelon, der formaterer, hvordan resultater returneres og vises til slutbrugerne. Det er skrevet i HTML-formatet med nogle IIS-udvidelser og indekseringstjeneste. Disse udvidelser inkluderer variabelnavne og andre koder til behandling af resultater.

## Referencer

* [Formatere resultaterne i .Htx-fil](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)


