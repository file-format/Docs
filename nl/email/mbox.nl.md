{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - Mailboxbestand voor e-mail",
  "description":"Meer informatie over MBOX-bestandsindeling en API's die MBOX-bestanden kunnen maken en openen.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een MBOX-bestand?

MBox-bestandsindeling is een algemene term die staat voor een container voor het verzamelen van elektronische mailberichten. De berichten worden samen met hun bijlagen in de container opgeslagen. Berichten uit een hele map worden opgeslagen in één databasebestand en nieuwe berichten worden aan het einde van het bestand toegevoegd. Talloze applicaties en API bieden ondersteuning voor MBox-bestandsindelingen zoals Apple Mail en Mozilla Thunderbird.

## MBOX-bestandsindeling ##

Het MBox-bestandsformaat bleef vrij lang niet-gestandaardiseerd tot 2005 toen de applicatie/mbox werd gestandaardiseerd als [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Berichten, in RFC 2822-formaat , worden de een na de ander aaneengeschakeld in de MBox-bestandsindeling. Elk bericht begint met een scheidingslijn die de afzender van het bericht identificeert, en identificeert ook de datum en tijd waarop het bericht is ontvangen door de uiteindelijke ontvanger (ofwel het laatste-hopsysteem in het overdrachtspad, ofwel het systeem dat dienst doet als de ontvanger van het bericht. mailwinkel). Elk bericht wordt meestal afgesloten met een lege regel. Het einde van de database wordt meestal herkend door ofwel de afwezigheid van aanvullende gegevens, ofwel door de aanwezigheid van een expliciete einde-van-bestand-markering.

## Een bericht lezen van MBox-bestand ##

Een lezer scant door een mbox-bestand op zoek naar From_-regels. Elke From_-regel markeert het begin van een bericht. De lezer moet niet proberen te profiteren van het feit dat elke regel From_ (voorbij het begin van het bestand) lege regel is. Zodra de lezer een bericht vindt, extraheert het een (mogelijk beschadigde) envelopafzender en bezorgdatum uit de From_-regel. Het leest dan tot de volgende From_-regel of het einde van het bestand, wat het eerst komt. Het verwijdert de laatste lege regel en verwijdert het citeren van >Van_ regels en >>Van_ regels enzovoort. Het resultaat is een RFC 822-bericht.

## Overwegingen bij codering ##

De inhoud van een MBox-bestand kan onomkeerbaar vermengd raken wanneer een ontvangen e-mail een Mbox-bestand als bijlage bevat en wordt opgeslagen in een ander Mbox-bestand. Om dit te voorkomen, moeten berichtensystemen een mbox-database coderen met niet-transparante overdrachtscodering (zoals BASE64 of Quoted-Printable) wanneer een dergelijk object wordt overgedragen via berichtenprotocollen. Implementers moeten ook voorbereid zijn om mbox-gegevens lokaal te coderen als niet-conforme gegevens worden ontvangen.

## Referenties ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)

