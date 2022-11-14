{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "extensie", "cdb-bestand", "cdb-bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "wat is een cdb-bestand"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over CDB-bestandsindelingen en API's die CDB-bestanden kunnen maken en openen.",
  "title" :"CDB - Constant databasebestand",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## Wat is een CDB-bestand?
De CDB-bestanden worden gebruikt in bedrijfskritieke toepassingen zoals e-mail. De CDB staat voor "constant database", een snel, betrouwbaar en eenvoudig pakket voor het maken of uitlezen van constante databases. Databasevervanging is veilig tegen systeemcrashes. Gebruikers hoeven niet te pauzeren tijdens het herschrijven. CDB werkt als een associatieve array (op schijf), wijst sleutels toe aan waarden en maakt het mogelijk om meerdere waarden in één enkele sleutel op te slaan.

## CDB-bestandsindeling
Het CDB-bestandsformaat slaat getallen, offsets, lengtes en hash-waarden op in little endian-formaat als niet-ondertekende 32-bits gehele getallen. Sleutels en gegevens worden beschouwd als ondoorzichtige bytestrings zonder speciale behandeling. Aan het begin van de database vertegenwoordigt de header met een vaste grootte 256 hash-tabellen door hun positie in het bestand en hun lengte in slots op te sommen. Gewoonlijk worden de gegevens opgeslagen als een reeks records, elk record slaat sleutellengte, gegevenslengte, sleutel en gegevens op. Er zijn geen sorteer- of uitlijningsregels. De records worden gevolgd door een set van 256 hashtabellen van verschillende lengtes. Aangezien nul een geldige lengte is, kunnen er minder dan 256 hashtabellen fysiek in de database zijn opgeslagen, maar niets wordt beschouwd als 256 tabellen. Hash-tabellen bestaan uit een reeks slots, die elk een hash-waarde en een record-offset bevatten. "Lege slots" hebben een offset van nul.

### Structuur
CDB-database bestaat uit een volledige dataset in een enkel computerbestand. Het bevat drie delen:
- Een kop met een vast formaat
- Gegevens
- Een set hashtabellen.

Zoekopdrachten zijn alleen beschikbaar voor exacte sleutels. Lookups werken met behulp van het volgende algoritme:

- Hash de sleutel.
- Bepaal bij welke hashtafel en slot dit record moet komen te staan.
- Test het aangegeven slot in de hashtabel.

Voor het opzoeken van sleutels met meer dan één waarde, kunnen extra waarden worden gevonden door eenvoudigweg de zoekopdracht te hervatten bij het volgende slot.

#### Functies

De CDB-databasestructuur biedt verschillende functies:

##### Snel opzoeken
Een succesvolle lookup in een enorme database kost normaal gesproken slechts twee schijftoegangen en een mislukte lookup duurt slechts één.
##### Lage overhead
Een database gebruikt 2048 bytes, 24 bytes per record en de ruimte voor sleutels en gegevens.
##### Geen willekeurige limieten
CDB kan elke database tot 4 gigabyte beheren. Aangezien er geen andere beperkingen zijn, hoeven de records niet eens in het geheugen te passen. Databases worden opgeslagen in een machine-onafhankelijk formaat.
##### Snelle vervanging van atomaire database
Het commando **cdbmake** kan een hele database herschrijven in twee ordes van grootte, sneller dan andere hashing-pakketten.
##### Snelle database-dumps
**cdbdump** kan de inhoud van een database afdrukken in een cdbmake-compatibel formaat.


## Referenties ##

* [cdb (software) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(software))
* [CDB-specificatie](http://cr.yp.to/cdb.html)

