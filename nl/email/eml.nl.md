{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - e-mailbericht",
  "description":"Meer informatie over EML-bestandsindeling en API's die EML-bestanden kunnen maken en openen.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## Wat is een EML-bestand?

EML-bestandsindeling vertegenwoordigt e-mailberichten die zijn opgeslagen met Outlook en andere relevante toepassingen. Bijna alle e-mailclients ondersteunen dit bestandsformaat omdat het voldoet aan de RFC-822 Internet Message Format Standard. Microsoft Outlook is de standaardsoftware voor het openen van EML-berichttypen. EML-bestanden kunnen worden gebruikt om op schijf op te slaan en om naar ontvangers te verzenden met behulp van communicatieprotocollen.

## Korte geschiedenis van EML

EML-bestandsformaatspecificaties zijn beschikbaar volgens [RFC 822](http://www.ietf.org/rfc/rfc0822.txt) Standard Format. Voorafgaand aan RFC-822, beheerste RFC-733 de regels van de uitwisseling van netwerkberichten tot in 1982, de eerste werd gecreëerd als een verbetering van lateraal door ARPA-normen vast te stellen. Tegelijkertijd creëerde Microsoft zijn eigen COM-modules voor de ontwikkeling van zijn eigen e-mailclient, namelijk Outlook Express. RFC-822 nam het pad om te worden gevestigd als een eigen formaat toen Microsoft afweek van de open standaard en creëerde het [PST](/nl/email/pst/) bestandsformaat waarin e-mails worden opgeslagen in een zeer gestructureerde database-indeling. Dit resulteerde in problemen voor gebruikers van niet-Microsoft e-mailclients wanneer e-mails werden doorgestuurd vanuit Microsoft Outlook.

Het was in 2001 toen de 822-standaard werd verbeterd tot 2822 - Internet Message Format dat momenteel wordt gebruikt voor het maken, lezen en verzenden van EML-berichten in MIME RFC-822-formaat.

## Specificaties EML-bestandsindeling

EML-bestanden bestaan uit twee onderscheiden secties:

* Headers - Bevat informatie over de berichtkop
* Berichttekst - Bevat een reeks informatie die berichtinhoud, ingesloten afbeeldingen en bijlagen kan bevatten

### Koptekstinformatie ###

Een EML-bestand bestaat uit Headers-informatie en optioneel berichttekst. Elke kopregel in de EML bestaat uit twee delen gescheiden door een dubbele punt ":". De eerste heet Header Name en die na de dubbele punt is de header body. Dergelijke koppen omvatten bijvoorbeeld:

* E-mailadres afzender
* Emailadres van ontvanger
* Onderwerp van e-mail
* Tijd- en datumstempel van bericht

**Voorbeeldkop**

Van:<John@bmw.eml.light.com>

Tot:<Andy@fileformat.com>

Datum: do, 8 maart 2018 10:43:37 +0100

Onderwerp: BMW eml licht

### Bericht lichaam ###

EML-berichttekst bevat de primaire informatie van e-mail in de vorm van tekst, hyperlinks en bijlagen. De hoofdtekst van de e-mail kan leesbare tekst bevatten, maar dat is niet nodig. In dit geval kan de berichttekst leeg zijn of gecodeerde bijlagegegevens bevatten.

De inhoud van de berichttekst wordt beschreven door het inhoudstype dat de leestoepassingen in staat stelt de informatie in respectieve formaten te lezen. Het vertegenwoordigt eigenlijk de aard en het formaat van een document. De structuur van een MIME-type of content-type is heel eenvoudig; het bestaat uit een type en een subtype, twee strings, gescheiden door een '/'. Er is geen ruimte toegestaan. Het `type` vertegenwoordigt de categorie en kan een afzonderlijk of een meerdelig type zijn. Het `subtype` is specifiek voor elk type. De lijst met typen die in de categorie Inhoudstype vallen, is lang, maar enkele belangrijke inhoudstypen zijn als volgt:


|**Type**|**Beschrijving**|**Voorbeeld van subtypen**
---|---|---|
|text|Vertegenwoordigt formaat dat voor mensen leesbaar is|text/plain, text/html, text/css, text/javascript
|image|Vertegenwoordigt elk type afbeelding met uitzondering van video's|afbeelding/bmp, afbeelding/png, afbeelding/jpg, afbeelding/gif
|audio|Vertegenwoordigt elk audiobestandsformaat|audio/mdi, audio/wav
|application|Vertegenwoordigt alle soorten binaire gegevens|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Weergave van bijlage in EML-hoofdtekst ###

EML-body bevat grenzen voor elk inhoudstype dat het bevat. Bijlage in de berichttekst wordt geïdentificeerd door het Content-Type en Content-Disposition, zoals weergegeven in het volgende voorbeeld:

Inhoudstype: tekst/plat; charset#"windows-1252"; naam#"apple app store.txt"
Content-Disposition: bijlage; bestandsnaam#"apple app store.txt"
Inhoud-overdracht-codering: base64
X-bijlage-ID: f_jkhztmd02

Zoals te zien is, stelt de Content-Disposition ingesteld op bijlage de leesapplicaties in staat om bijlage-informatie op te halen, zoals de bestandsnaam van de bijlage en de overdrachtscodering. De koptekstinformatie van de bijlage wordt gevolgd door de gecodeerde inhoud van de bijlage die moet worden gelezen.

#### Voorbeeld van spreadsheet als bijlage ####

Inhoudstype: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; naam#"english_spodr.xlsx"
Content-Disposition: bijlage; bestandsnaam#"english_spodr.xlsx"
Inhoud-overdracht-codering: base64
X-bijlage-ID: f_jkhztmd43

## Referenties

* [RFC 822](http://www.ietf.org/rfc/rfc0822.txt)

