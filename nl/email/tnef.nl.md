{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"Meer informatie over de TNEF-bestandsindeling en API's die TNEF-bestanden kunnen maken en openen.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een TNEF-bestand?

Transport Neutral Encapsulation Format (TNEF) is eigendom van Microsoft, voor het inkapselen van e-mailbijlagen op basis van Messaging Application Programming Interface (**MAPI**). Microsoft Outlook en Microsoft Exchange Server ondersteunen TNEF volledig, terwijl later TNEF wordt gedecodeerd in MAPI en de geformatteerde e-mails worden weergegeven. Een e-mailbijlage met TNEF-codering heeft een MIME-type MS-TNEF en wordt opgeslagen als winmail/win.dat. De bijlage in winmail .dat bevat de volgende informatie:


|Bericht|OLE-objecten|Outlook-functies
---|---|---|
|<ul><li> Originele berichtbijlagen</li><li> Origineel geformatteerde versie</li><li> lettertypen, tekstgroottes en tekstkleuren</li></ul> |<ul><li> ingesloten afbeeldingen</li><li> ingesloten Office-documenten</li></ul> |<ul><li> aangepaste formulieren</li><li> stemknoppen</li><li> vergaderverzoeken</li></ul>


Andere e-maildiensten die TNEF niet ondersteunen, presenteren platte tekst voor TNEF-geformatteerde berichten. Outlook sluit een uitgebreide indeling van het bericht in TNEF-bestanden (OLE) of bepaalde Outlook-functies (formulieren, polling-knoppen en vergaderverzoeken) in. Het is niet mogelijk expliciete TNEF-codering binnen de e-mailclient van Outlook te bestraffen, maar het kiezen van het RTF-formaat voor het verzenden van een e-mail vereenvoudigt impliciet TNEF-codering.

## TNEF-bestandsindeling

Het TNEF-gegevensalgoritme brengt een afgeplatte structuur tot stand op basis van rijke hiërarchische berichteigenschappen. Deze afgeplatte structuren worden vervolgens gebruikt om een seriële gegevensstroom weer te geven die is samengesteld uit bepaalde eigenschappen.

In sommige situaties, waar eigenschappen voorkomen in groepen of meerdere waarden hebben, kan de stream tellingen en opvullingen bevatten om een specifieke gegevensuitlijning af te dwingen. Een onderscheidende situatie waarin het gebruik van dit algoritme voordelig is, is in een niet-ondersteunende berichtenomgeving. In dergelijke omgevingen wordt een rich message-eigenschap gecodeerd in een seriële gegevensstroom door een TNEF-schrijver. Verder kunnen de eigenschappen die niet tot de onderliggende TNEF behoren worden ingekapseld tijdens transmissie. Deze ingekapselde eigenschappen worden vervolgens beschikbaar gemaakt door te decoderen via een TNEF om de beschikbaarheid van alle eigenschappen van het oorspronkelijke bericht voor de clienttoepassing te garanderen.

In TNEF zijn alle numerieke gegevenstypen little-endian en zijn ze groter dan één byte. Om deze numerieke waarden op niet-little-endian-platforms te verwerken, moeten de juiste transformaties worden uitgevoerd om de juiste waarden te krijgen. Stringwaarden worden weergegeven in Augmented Backus-Naur Form (ABNF)-formaat volgens [RFC5234]-specificaties. Wanneer de string eindigt met een null-teken, wordt deze ook opgenomen; bijvoorbeeld `"worker@specimen.com" %x00`.

{{< figure src="../TNEF.png" alt="TNEF-bestandsindeling" >}}

## TNEF-kenmerken en verwerkingsregels ##

De gegevensstroom in TNEF begint met een oud versienummer, een handtekening, een primitieve sleutelwaarde en een attribuut dat een codepagina voorstelt. Deze codetabel wordt gegenereerd wanneer de encoder ANSI-kenmerken en -eigenschappen registreert. Daarna werd de stream een reeks attributen waarin eerst de berichtattributen stonden en daarna de bijlageattributen. Verschillende kenmerken van berichten en bijlagen zijn opgenomen in speciale kenmerken zoals attMsgProps, attAttachment en attRecipTable. De attributen die in de TNEF-stream verschijnen, bevatten de structuur, berichteigenschappen en conversies die nodig zijn om ze te betrekken bij berichteigenschappen. Elk attribuut bestaat uit een ID, grootte en gegevens van het attribuut, een controlesom en een niveau volgens de toepassing ervan.

## Relatie met protocollen en andere algoritmen ##

De systemen met een slecht mechanisme om een rijk berichtformaat weer te geven, hebben native een TNEF-gegevensalgoritme nodig voor transport. Bij gebruik van het mediatype ms-TNEF bestaat de uitvoer van het algoritme uit een bijlagebestand (winmail.dat) en een lichaamsdeel van MIME gespecificeerd in [RFC2045]. De berichttekst zonder opmaak wordt verzonden met UUENCODE volgens de [MSDN-UAF]-specificatie en deze berichttekst of gelijkwaardige methode wordt gedecodeerd aan de kant van de ontvanger. Bovendien kan TNEF berichtgegevens verzenden met behulp van verschillende internetprotocollen zoals SMTP, POP3, IMAP4 en degenen die MIME integreren volgens de RFC2045-standaard.

## Toepasselijkheidsverklaring ##

Naast eenvoudige berichtoverdracht, zou de oorspronkelijke toepassing van TNEF worden gemaakt om berichtklassen te gebruiken en extra functies te ondersteunen die geen originele ondersteuning in het transportprotocol hebben. Deze applicatie is verder verfijnd voor het verzenden van uitgebreide berichteigenschappen en benoemde eigenschappen die moderne berichtenclients tegenwoordig gebruiken. Om te voldoen aan de oorspronkelijke implementatie, wordt de oorspronkelijke attribuutsyntaxis behouden en een speciaal attribuut houdt de nieuwe berichteigenschappen afzonderlijk vast.

## Referenties

* [Transport Neutral Encapsulation Format](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [E-mailadressen en adresboeken in Exchange Server](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# ruilserver-2019)
* [[MS-OXTNEF]: TNEF-gegevensalgoritme (Transport Neutral Encapsulation Format)](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

