{
  "date" : "2019-10-11",
  "keywords" :[ "potm-bestand", "potm-bestandsformaat", "wat is een potm-bestand", "bestand", "potm-voorbeeld", "potm-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POTM - Microsoft PowerPoint-sjabloonbestand met macro's",
  "description":"Meer informatie over POTM-bestandsindelingen en API's die POTM-bestanden kunnen maken en openen.",
  "linktitle" : "POTM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een POTM-bestand?

Bestanden met de extensie POTM zijn Microsoft PowerPoint-sjabloonbestanden met ondersteuning voor macro's. POTM-bestanden worden gemaakt met PowerPoint 2007 of hoger en bevatten standaardinstellingen die kunnen worden gebruikt om verdere presentatiebestanden te maken. Deze instellingen kunnen stijlen, achtergronden, kleurenpalet, lettertypen en standaardinstellingen omvatten, samen met macro's die bestaan uit aangepaste functies voor het uitvoeren van een bepaalde taak. Ze kunnen ook worden geopend door een eerdere versie van PowerPoint waarop Open XML-documentondersteuning is geïnstalleerd. POTM-bestanden kunnen worden geopend in Microsoft PowerPoint voor bewerking zoals elk ander PowerPoint-bestand.

## Specificaties bestandsindeling ##

Het POTM-bestandsformaat is gebaseerd op Office OpenXML-specificaties en lijkt op de structuur van het [PPTX](/nl/presentation/pptx/)-bestand dat een gecomprimeerd [ZIP](/nl/compression/zip/)-archief is.

Dia's in een POTM-bestand kunnen tekst, afbeeldingen, video's, afbeeldingen en andere objecten bevatten die vrij op de pagina kunnen worden gerangschikt. POTM-sjablonen worden vervolgens gebruikt om meerdere bestanden te maken die alle opmaakopties van het bestand overnemen. Macro's in het POTM-bestand worden daarom ook overgenomen door andere presentaties. Het insluiten ervan in de structuur van het document gebeurt via de Macro Recorder die is opgenomen in MS Office, die opdrachtreeksen kan opslaan en macro's kan maken om ze automatisch te repliceren.

Bestanden die zijn gegenereerd met Office Open XML-bestandsindeling is een verzameling XML-bestanden samen met andere bestanden die koppelingen bieden tussen alle samenstellende bestanden. Deze verzameling is eigenlijk een gecomprimeerd archief dat kan worden uitgepakt om de inhoud ervan te bekijken. Om dit te doen, hernoemt u gewoon de POTM-bestandsextensie met zip en extraheert u deze om de inhoud te bekijken.

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

Voor een impliciete relatie is er geen directe verwijzing naar een `<Relationship> id`. In plaats daarvan wordt de verwijzing begrepen.

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

* [[MS-PPTX] - PPTX-bestandsindeling](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

