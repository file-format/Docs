{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CON File - Concept Application Source File Format",
  "description" :"Meer informatie over wat een CON-bestand is en API's die CON-bestanden kunnen maken en openen.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## Wat is een CON-bestand?

Een CON-bestand is een broncodebestand voor een applicatie die is ontwikkeld voor de **Concept Application Server**. Het wordt gebruikt voor het schrijven van toepassingen voor gegevensuitwisseling tussen de server en de gebruiker. CON-bestanden die op de server worden gehost, zijn toegankelijk met een webbrowser, op voorwaarde dat de Concept Client aan de kant van de gebruiker is geïnstalleerd. Concept Applicatieserver is een webserver met kleinschalige programmeertaal die een [SQL](/nl/database/sql/) subset database-engine (TinDB) kan hebben.

CON-bestanden kunnen worden geopend/uitgevoerd met RadGs Concept Application Server.

## CON-bestandsindeling - Meer informatie

CON-bestanden worden gehost op de server en zijn toegankelijk via een webbrowser op de gebruikerscomputer. Concept [URL's](/nl/web/url/) zijn anders dan normale HTTP-urls en beginnen met **concept://**.

### CON Bestands-URL Voorbeeld

Een CON-bestand dat op de Concept Application Server wordt gehost, is toegankelijk via een webbrowser met behulp van URL's zoals:

```
concept://domain.server.com/web_application/main.con.
```
## Referenties

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

