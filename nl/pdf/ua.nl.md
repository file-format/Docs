{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/UA-bestandsindeling",
  "description":"Meer informatie over PDF/UA-bestandsindelingen en API's die PDF/UA-bestanden kunnen maken en openen.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Wat is een PDF/UA-bestand? #

PDF/UA werd in augustus 2012 gepubliceerd als [ISO Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) en is verreweg de eerste volledige definitie van een reeks vereisten voor universeel toegankelijke PDF-documenten. De term "algemeen toegankelijk" verwijst naar het begrip dat de informatie in een [PDF](/nl/pdf/)-document gelijkelijk en onafhankelijk toegankelijk moet zijn voor iedereen in het algemeen en voor mensen met een handicap in het bijzonder. De introductie van de PDF/UA-standaard kan worden beschouwd als een belangrijke stap voor het maken van tools en toepassingen om PDF-inhoud te maken en te lezen.

## Vereisten voor bestandsindeling ##

De PDF/UA heeft een aantal duidelijke vereisten aan de basis die de essentie van deze standaard vormen. Deze zijn in wezen gebaseerd op het taggen van PDF's, wat betekent dat alle PDF/UA-documenten correct moeten worden getagd. Het vereist ook dat de tags semantisch passend en in logische volgorde zijn. Dit zorgt ervoor dat het einddocument dat is gemaakt met de PDF/UA-specificatie betrouwbaarder en toegankelijker is. Dit kan ertoe leiden dat PDF-auteurs zich afvragen of ze alles over al deze vereisten moeten weten? Gelukkig is het niet zo, aangezien de PDF/UA-conformiteitstools de verantwoordelijkheid nemen voor het toevoegen en behouden van de toegankelijkheid van de PDF.

De vereisten voor bestandsindelingen voor PDF/UA zijn als volgt.

* Inhoud wordt op twee manieren gecategoriseerd: zinvolle inhoud en artefacten zoals decoratieve pagina-elementen. Alle zinvolle inhoud moet worden getagd en geïntegreerd in de structuurstructuur van alle tags in een document. Artefacten daarentegen hoeven alleen als zodanig te worden gemarkeerd.
* Betekenisvolle inhoud moet worden gemarkeerd met tags en samen met de andere tags in het document een volledige structuurstructuur creëren.
* Betekenisvolle inhoud moet worden gemarkeerd met de juiste semantische tags.
* De structuurstructuur die door de documenttags wordt gemaakt, moet de logische leesvolgorde van het document weerspiegelen.
* Alleen de standaard tags gedefinieerd in PDF 1.7 mogen worden gebruikt; als er andere tags worden gebruikt, moet een roltoewijzingsitem vastleggen welke standaardtag elk vertegenwoordigt.
* Informatie mag niet alleen met visuele middelen worden overgebracht (bijv. contrast, kleur of positie op de pagina).
* Flikkerende, knipperende of knipperende inhoud is niet toegestaan, hetzij als effecten die worden beheerd door JavaScript of als onderdeel van video's die zijn ingesloten in de PDF.
* Er moet een documenttitel worden opgegeven en het document moet zo worden ingesteld dat de titel (in plaats van de bestandsnaam) in de venstertitel verschijnt.
* De taal van alle inhoud moet worden vermeld en taalveranderingen moeten expliciet als zodanig worden gemarkeerd.

## PDF/UA-conformiteit ##

De PDF/UA-standaard definieert specificaties voor inhoud, lezers en ondersteunende technologie. Deze drie aspecten zijn met elkaar verbonden op basis van de inhoud van het document. De conformiteitsvereisten voor elk van deze zijn zoals hieronder vermeld.

## Conforme bestanden ##

Bestanden die voldoen aan de PDF/UA-standaard moeten functies bevatten die geldig zijn volgens de [PDF 1.7-specificaties](http://www.adobe.com/go/pdfreference). Functies die specifiek door PDF/UA zijn verboden, moeten echter worden uitgesloten.

## Conforme Lezers ##

Een conforme lezer moet zich houden aan de regels die zijn gespeld in de specificaties van PDF 1.7. In het bijzonder moet het ondersteunen:

* alle tags, attributen en sleutelwaarden die zijn gespecificeerd voor toegankelijkheid. Het moet ook de mogelijkheid hebben om digitale handtekeningen, annotaties en optionele inhoud te verwerken en weer te geven.
* digitale handtekeningen, annotaties en optionele inhoud verwerken en weergeven
* op verschillende manieren door het document navigeren

## Conform ondersteunende technologie ##

Er is een conforme ondersteunende technologie nodig om de PDF/UA-functies te ondersteunen. Deze omvatten bijvoorbeeld kenmerken van de inhoud en de lezer, en moeten navigatie op paginalabels, documentstructuur of de omtrek mogelijk maken. Het zou de gebruiker ook de standaardnavigatiezoom moeten laten overschrijven.

## Referenties ##

* [PDF/UA - Door Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA in een notendop](http://www.pdfa.org/publication/pdfua-in-a-nutshell/)

