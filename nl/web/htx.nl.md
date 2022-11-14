{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTX-bestand - HTML-extensiebestandsindeling",
  "description" :"Uw gids voor bestandsindelingen om te leren wat een HTX-bestand is en API's die HTX-bestanden kunnen maken en openen.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een HTX-bestand?

Een HTX-bestand is eigenlijk een HTML-bestand dat gegevensvariabelen bevat voor het weergeven van de resultaten van de databasequery als een webpagina. Meestal gemaakt met Microsoft FrontPage-webontwikkelingssoftware, worden HTX-bestanden opgeslagen om te worden opgeslagen in dezelfde map als het overeenkomstige Internet Database Connector-bestand (.IDC).

HTX-bestanden kunnen worden geopend met toepassingen zoals Microsoft FrontPage en elke teksteditor zoals Kladblok, Teksteditor of Atom.

## HTX-bestandsindeling

HTX-bestanden worden opgeslagen als tekstbestand met code voor het ophalen van gegevens uit een database en het opslaan van variabelen voor weergave.


### HTX-bestandsvoorbeeld

Een voorbeeld van een HTX-bestand is als volgt dat een paginakop definieert voor het weergeven van de querybeperking en de documenten die op de pagina worden weergegeven voor weergave aan de gebruiker.

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

De uitvoer van deze voorbeeldcode is als volgt.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Zoals te zien is, is het HTX-bestand een sjabloon die opmaakt hoe resultaten worden geretourneerd en weergegeven aan de eindgebruikers. Het is geschreven in HTML-formaat met enkele IIS-extensies en Indexing Service. Deze extensies bevatten namen van variabelen en andere codes voor het verwerken van resultaten.

## Referenties

* [De resultaten formatteren in .Htx-bestand](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

