{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "Bestand", "Extensie", "Bestandsindeling", "Bestandsextensie", "uitbreidbare html"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - Uitbreidbaar Hypertext Markup Language-bestandsformaat",
  "description":"Meer informatie over de XHTML-bestandsindeling en API's die XHTML-bestanden kunnen maken en openen.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een XHTML-bestand?

De XHTML is een op tekst gebaseerd bestandsformaat met opmaak in de XML, met behulp van een herformulering van HTML 4.0. Deze bestanden zijn zeer geschikt om te openen of te bekijken in een webbrowser. XHTML is ontworpen om meer gestructureerd, minder scripting, generiek te zijn; gebruikmakend van alle bestaande faciliteiten van XML en meer apparaatonafhankelijk. XHTML biedt een algemeen waardevolle set van elementen en attributen, met uitbreidingsopties in combinatie met stylesheets. De attributen worden gebruikt uit de verzameling metadata attributen. XHTML biedt flexibiliteit en toegankelijkheid door alle **[HTML](/nl/web/html/)** presentatie-elementen ondergeschikt te maken aan stylesheets. Style sheets zijn veelzijdiger dan deze presentatie-elementen. Specificaties voor HTML 4.01, HTML5 en XHTML worden dynamisch ontwikkeld door het World Wide Web Consortium (W3C).

## Korte geschiedenis van XHTML-bestandsindeling

De geschiedenis van XHTML begint met een conceptdocument dat in december 1998 werd vrijgegeven door het World Wide Web Consortium. Dit document verwijst naar de "Herformulering van HTML in XML", een specificatie genaamd XHTML 1.0. Deze nieuwe specificatie herformuleerde HTML in XML met gebruikmaking van de bestaande elementen of attributen. In mei 1999 verklaarde het W3 Consortium dat HTML 4.0 was omgevormd tot een XML-toepassing. oftewel XHTML. Op 26 januari 2000 werd de eerste specificatie die XHTML 1.0 definieert, vrijgegeven door W3C. Op 31 mei 2001 kondigde het W3C XHTML aan als een onafhankelijke taal en begon het te werken aan de ontwikkeling van HTML 5.0. In 2005 werd echter een werkgroep (WHATWG) gevormd die tot doel had gewone HTML onafhankelijk van XHTML te verbeteren. De WHATWG begon uiteindelijk parallel aan XHTML 2 aan HTML5 te werken.

## XHTML-bestandsindeling

XHTML is een formaat dat een verzameling is van verschillende documenttypes en modules die HTML 4 nabootsen, categoriseren en uitbreiden. De bestanden in XHTML zijn gebaseerd op XML en zijn bedoeld om te werken met user agents op basis van XML. XHTML-bestanden zijn XML-conform. Standaard XML-tools worden gebruikt om XHTML-bestanden te bekijken, te bewerken en te valideren. HTML Document Object Model of het XML Document Object Model [DOM]-afhankelijke applicaties kunnen werken via XHTML-documenten. Door vandaag voor XHTML te kiezen, kunnen inhoudontwikkelaars genieten van alle bijbehorende voordelen van XML zonder zich zorgen te hoeven maken over de voorwaartse of achterwaartse compatibiliteit van hun inhoud.

Een set gerelateerde elementen bouwt een module in XHTML. Een formulier- of tabelmodule kan verschillende formulier- of tabelelementen bevatten die op een webpagina kunnen worden weergegeven. De modularisatie was bedoeld om HTML-elementen te isoleren in sets van talrijke gekoppelde elementen. Zodat contentontwikkelaars kunnen profiteren van moduleselectie voor verschillende soorten apparaten. Bovendien stellen modules gebruikersagenten in staat om elementen te selecteren zonder de consistentie met de XHTML-standaard te verliezen. De parseervereisten van XHTML zijn hetzelfde als XML, terwijl HTML zijn eigen oefent.

### Documentconformiteit

XHTML2 biedt specificaties die voldoen aan XHTML 1.0-documenten, die gebruik maken van de namespaces-elementen en attributen uit de XML en XHTML 1.0. Documentconformiteit is van twee soorten.

Een strikt conform document is gebaseerd op XML en heeft alleen verplichte services nodig die in deze specificatie zijn gedefinieerd. Voor XHTML-bestanden moet aan de volgende criteria worden voldaan:

* Een bestand moet voldoen aan de beperkingen gedefinieerd in DTD's en in Bijlage B.
* Het basiselement van het bestand moet html zijn.
* Het basiselement van het bestand moet declaratie bevatten voor de XHTML-naamruimte en moet worden gedefinieerd als:

```
http://www.w3.org/1999/xhtml.
```

* Het basiselement kan worden geschreven als:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Eerder dan het basiselement moet een DOCTYPE worden gedeclareerd, waarvan de openbare identifier moet verwijzen naar een van de drie documenttypedefinities (DTD's). De systeem-ID kan worden gewijzigd om te voldoen aan de huidige systeemconventies.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

In XML-documenten is het niet nodig om XML-declaraties in alle documenten op te geven; inhoudontwikkelaars worden echter verleid om XML-declaraties in al hun XHTML-documenten te gebruiken. Deze declaraties zijn verplicht als de tekencodering van het document verschilt van UTF-8/16 of als er geen codering is gespecificeerd door een overkoepelend protocol. Het volgende voorbeeld van een XHTML-document definieert de XML-declaraties

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Een conforme user agent moet aan de volgende regels voldoen:

* Het ontleden en evalueren van het XHTML-document wordt gedaan door een user-agent die ervoor zorgt dat het consistent is met de XML 1.0-aanbeveling.
* In het geval van validerende user-agent, moet deze de geldigheid van de documenten controleren voor de DTD's waarnaar wordt verwezen volgens XML. Wanneer het XHTML-bestand door de user-agent wordt verwerkt als generieke XML, worden de kenmerken van het type ID erkend als fragment-ID's.

Als een user-agent een niet-herkend element tegenkomt, zijn de volgende verplichte criteria waaraan het moet voldoen:

* verwerk de inhoud van dat onbekende element
* negeer het attribuut en zijn waarde
* Gebruik de waarde van het opgegeven kenmerk als standaard.

Wanneer user agent een entiteitsreferentiedeclaratie tegenkomt die niet eerder is verwerkt, moet deze worden verwerkt als de tekens (beginnend met het "&"-teken en eindigend met de puntkomma). Tijdens de verwerking van inhoud kunnen karakters of karakterentiteitsreferenties die voorspelbaar zijn door de user-agent maar niet renderbaar zijn, elke alternatieve weergave gebruiken die dezelfde betekenis oplevert. In een dergelijk geval moet het document worden weergegeven op een manier die de gebruiker duidelijk maakt dat het weergaveproces niet normaal is geweest. Voor het verwerken van witruimte moet de user-agent de definitie van CSS-tekens [CSS2] bekijken.

## XHTML Achterwaartse compatibiliteit

De achterwaartse compatibiliteit van XHTML 1.-documenten is goed thuis in HTML 4 user agents, als de juiste regels worden gevolgd. XHTML 1.1 is volledig compatibel, behalve robijnrode annotaties, ook al worden ze over het algemeen genegeerd door de HTML 4-browsers. XHTML 2.0 is relatief minder compatibel, maar het probleem is tot op zekere hoogte verholpen door het gebruik van scripts.

## Referenties

* [Een geschiedenis van XHTML: van de jaren 1990 tot vandaag](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

