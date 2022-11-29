{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTX-fil - HTML-tilläggsfilformat",
  "description" :"Din filformatsguide för att lära dig vad en HTX-fil och API:er är som kan skapa och öppna HTX-fil.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en HTX fil?

En HTX-fil är egentligen en HTML-fil som innehåller datavariabler för att visa databasfrågeresultaten som en webbsida. Oftast skapade med Microsoft FrontPage webbutvecklingsprogram, HTX-filer sparas för att sparas i samma mapp som motsvarande Internet Database Connector-fil (.IDC).

HTX-filer kan öppnas med applikationer som Microsoft FrontPage och vilken textredigerare som helst som Notepad, TextEdit eller Atom.

## HTX filformat

HTX-filer sparas som vanlig textfil med kod för att hämta data från en databas och spara i variabler för visning.


### Exempel på HTX-fil

Ett exempel på HTX-fil är som följer som definierar en sidhuvud för att visa frågebegränsningen och dokumenten som visas på sidan för visning för användaren.

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

Utdata från denna exempelkod är som följer.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Som kan ses är HTX-filen en mall som formaterar hur resultat returneras och visas för slutanvändarna. Det är skrivet i HTML-format med vissa IIS-tillägg och indexeringstjänst. Dessa tillägg inkluderar variabelnamn och andra koder för bearbetning av resultat.

## Referenser

* [Formatera resultaten i .Htx-fil](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

