{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - iCalendar-bestandsindeling",
  "description":"Meer informatie over ICS-bestandsindelingen en API's die ICS-bestanden kunnen maken en openen.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een ICS-bestand?

De Internet Calendaring and Scheduling Core Object Specification (iCalendar) is een internetstandaard (RFC 2445) voor het uitwisselen en implementeren van agenda-evenementen en planning. Het iCalendar-formaat is interoperabel, waardoor de uitwisseling van agenda-informatie tussen de gebruikers met verschillende e-mailtoepassingen wordt gegarandeerd. iCalendar formatteert de invoergegevens als Multipurpose Internet Mail Extensions (MIME) en faciliteert de uitwisseling van objecten via verschillende transportprotocollen. Deze transportprotocollen kunnen SMTP, HTTP, point-to-point asynchrone communicatie en op fysieke media gebaseerd netwerktransport zijn.

iCalendar stelt gebruikers in staat om gebeurtenissen, datum/tijd-afhankelijke taken en beschikbaar/bezet-informatie via e-mail te delen met andere gebruikers die kunnen reageren. iCalendar-bestanden worden opgeslagen met de achtervoegsels ".ics" ".iCalendar" of ".ifb" met een MIME-type van "text/calendar". iCalendar wordt gehouden om zelfredzaam te zijn zonder enige afhankelijkheid van het transportprotocol. Webservers (met HTTP-protocol) kunnen iCalendar-informatie transporteren en webpagina's kunnen iCalendar-gegevens in ingebedde vorm bevatten met behulp van iCalendar.

## Korte geschiedenis van het ICS-bestandsformaat

In 1998 definieerde de Internet Engineering Task Force (IETF) iCalendar als een standaard (RFC 2445). De standaard is gedocumenteerd door Frank Dawson (Lotus Notes Corporation) en Derik Stenerson (Microsoft). In 2009 werd de standaard opnieuw verfijnd door Bernard Desruisseaux (Oracle) als RFC 5545. Deze keer werden enkele nieuwe functies toegevoegd en werden enkele verouderde functies afgeschaft. In 2016 werd RFC 7986 uitgebracht en aangevuld met de originele iCalendar RFC. RFC 7986 voegde nieuwe kenmerken toe aan het belangrijkste VCALENDAR-object en er werden ook nieuwe ondersteunende functies geïntroduceerd voor vergadersystemen.

## ICS-bestandsindeling ##

Het MIME-type dat wordt gebruikt door de gegevens van iCalendar is “tekst/kalender”. De standaardtekenset voor iCalendar is UTF-8, maar door parameters in MIME op te geven, kan een andere tekenset worden gebruikt. Een iCalendar-bestand bevat secties, onder deze secties is "VCALENDAR" de algemene sectie die alle andere secties omvat. De sectie VEVENT definieert gebeurtenissen, VTODO somt alle taken op, VJOURNAL bevat journaalboekingen en VTIMEZONE specificeert informatie over de tijdzone. meerdere secties van vergelijkbare categorie zijn toegestaan. Voor tal van evenementen kunnen meerdere VEVENT-secties aanwezig zijn in een iCalendar-bestand.

### Inhoudsregels ###

De iCalendar-objecten zijn gerangschikt in afzonderlijke tekstregels "inhoudsregels". In dit bestandsformaat beëindigt de CRLF-reeks een regel, terwijl de lengte van de regel beperkt is tot 75 octetten, exclusief het regeleinde. Een lang gegevensitem kan tot vele regels worden overspannen.

### Lijst- en veldscheidingstekens ###

Eigenschappen en parameters specificeren een lijst met waarden die worden gescheiden door een komma-teken. Tekenreeksen tussen aanhalingstekens worden gebruikt voor op URI gebaseerde parameterwaarden. Lijst met parameters kan worden geconstrueerd door de eigenschapswaarde. Elke eigenschapsparameter in deze lijst moet worden gescheiden door een puntkomma.

In een waardenlijst isoleert een puntkomma eigenschapsparameters en een komma afzonderlijke eigenschapswaarden. Voorbeeld wordt hieronder gegeven:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Meerdere waarden

Sommige eigenschappen kunnen meerdere waarden hebben. Het eenvoudig genereren van een nieuwe inhoudsregel met de eigenschapsnaam is de basisregel voor eigenschappen met meerdere waarden. Voor een enkele waarde met meerdere taalvariaties mogen echter geen eigenschappen met meerdere waarden worden gebruikt.

### Binaire inhoud

Binnen een iCalendar-object kan de eigenschapswaarde verwijzen naar binaire inhoudsgegevens die in een externe MIME-entiteit zijn geplaatst met behulp van een URI. Inline binaire inhoud kan in speciale situaties worden gebruikt met de parameter "ENCODING", waarbij de toepassing een iCalendar-object als enige entiteit moet uitdrukken. In het volgende voorbeeld wordt een eigenschap "ATTACH" met een URI-verwijzing uitgelegd:

BIJSLUITEN: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Karakterset

Hoewel het standaard tekensetschema voor een iCalendar UTF-8 is, is er geen eigenschapsparameter opgegeven om de tekenset van een eigenschapswaarde te definiëren. in MIME-overdrachten MOET de parameter "charset" worden gebruikt voor bestaande tekenset.

## Referenties

* [Internet Calendaring and Scheduling Core Object Specificatie](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

