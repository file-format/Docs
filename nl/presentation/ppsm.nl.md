{
  "date" : "2019-10-11",
  "keywords" :[ "ppsm-bestand", "ppsm-bestandsindeling", "wat is een ppsm-bestand", "bestand", "ppsm-voorbeeld", "ppsm-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM - Macro-enabled PowerPoint-presentatiebestand",
  "description":"Meer informatie over PPSM-bestandsindeling en API's die PPSM-bestanden kunnen maken en openen.",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een PPSM-bestand?

Bestanden met de extensie PPSM vertegenwoordigen de bestandsindeling voor diavoorstellingen met macro's die is gemaakt met Microsoft PowerPoint 2007 of hoger. Een ander vergelijkbaar bestandsformaat is [PPTM](/nl/presentation/pptm/) dat verschilt in het openen met Microsoft PowerPoint in bewerkbare indeling in plaats van als diavoorstelling. Wanneer het als diavoorstelling wordt uitgevoerd, toont het PPSM-bestand de presentatiedia's met intacte inhoud in de diavoorstelling en is standaard in de modus alleen-lezen. PPSM-bestanden kunnen nog steeds worden bewerkt in Microsoft PowerPoint door deze in PowerPoint te openen.

## Bestandsformaat ##

Het PPSM-bestandsformaat is geïntroduceerd met PowerPoint 2007 en is gebaseerd op het OpenXML-bestandsformaat dat een combinatie van XML en [ZIP](/nl/compression/zip/) gebruikt om de inhoud op te slaan. Bestanden die zijn gegenereerd met Office Open XML-bestandsindeling is een verzameling XML-bestanden samen met andere bestanden die koppelingen bieden tussen alle samenstellende bestanden. Deze verzameling is eigenlijk een gecomprimeerd archief dat kan worden uitgepakt om de inhoud ervan te bekijken. Om dit te doen, hernoemt u de PPSM-bestandsextensie met zip en extraheert u deze om de inhoud te bekijken.

De volgende paragrafen werpen enig licht op elk van deze.

### [Content_Types].xml ###

Dit is het enige bestand dat op het basisniveau wordt gevonden wanneer de zip wordt uitgepakt. Het vermeldt de inhoudstypen voor onderdelen in het pakket. Alle verwijzingen naar de XML-bestanden die in het pakket zijn opgenomen, worden in dit XML-bestand verwezen. Hieronder volgt een inhoudstype voor een diagedeelte:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Als er nieuwe onderdelen aan het pakket moeten worden toegevoegd, kan dit worden gedaan door het nieuwe onderdeel toe te voegen en eventuele relaties binnen de .rels-bestanden bij te werken. Houd er rekening mee dat voor een dergelijke wijziging ook de Content_Types.xml moet worden bijgewerkt.

### \_rels (map) ###

Relaties tussen de andere onderdelen en resources buiten het pakket worden onderhouden door het relatiegedeelte. De map Relaties bevat één XML-bestand waarin de relaties op pakketniveau zijn opgeslagen. Links naar de belangrijkste onderdelen van de presentatiebestanden zijn als URI's in dit bestand opgenomen. Deze URI's identificeren het type relatie van elk belangrijk onderdeel met het pakket. Dit omvat de relatie met het primaire kantoordocument dat zich bevindt als ppt/presentation.xml en andere delen binnen docProps als kern- en uitgebreide eigenschappen.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Elk deel van het document dat de bron is van een of meer relaties heeft zijn eigen relatiedeel waarbij elk van deze relatiedelen wordt gevonden in een \_rels-submap van het deel en wordt genoemd door '.rels' toe te voegen aan de naam van het een deel. Het hoofdinhoudsgedeelte (presentation.xml) heeft een eigen relatiegedeelte (presentation.xml.rels). Het bevat relaties met andere andere delen van de inhoud, zoals slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, evenals de URI's voor externe links.

#### Expliciete relatie ####

Voor een expliciete relatie wordt naar een resource verwezen met behulp van het Id-attribuut van a<Relationship> element. Dat wil zeggen, de Id in de bron verwijst rechtstreeks naar een Id van een relatie-item, met een expliciete verwijzing naar het doel.

Een dia kan bijvoorbeeld een hyperlink bevatten zoals deze:
```
<a:hlinkClick r:id#"rId2">
```
De r:id#"rId2" verwijst naar de volgende relatie binnen het relatiegedeelte voor de dia (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Impliciete relatie ####

Voor een impliciete relatie is er geen directe verwijzing naar een `<Relationship> Id'. In plaats daarvan wordt de verwijzing begrepen.

### ppt-map ###

Dit is de hoofdmap die alle details over de inhoud van de presentatie bevat. Standaard heeft het de volgende mappen:

* \_rels
* thema
* dia's
* dia-indelingen
* slideMasters

en volgende xml-bestanden:

* presentatie.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Referenties ##

* [OpenXML-presentatiebestandsindeling](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

