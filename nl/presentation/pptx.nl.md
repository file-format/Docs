{
  "date" : "2019-12-13",
  "keywords" :[ "pptx-bestand", "pptx-bestandsindeling", "wat is een pptx-bestand", "bestand", "pptx-voorbeeld", "pptx-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over PPTX-bestandsindelingen en API's die PPTX-bestanden kunnen maken en openen.",
  "title" :"PPTX - PowerPoint-presentatiebestandsindeling",
  "linktitle" : "PPTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een PPTX-bestand?

Bestanden met de extensie PPTX zijn presentatiebestanden die zijn gemaakt met de populaire Microsoft PowerPoint-toepassing. In tegenstelling tot de vorige versie van het presentatiebestandsformaat PPT, dat binair was, is het PPTX-formaat gebaseerd op het Microsoft PowerPoint open XML-presentatiebestandsformaat. Een presentatiebestand is een verzameling dia's waarbij elke dia kan bestaan uit tekst, afbeeldingen, opmaak, animaties en andere media. Deze dia's worden aan het publiek gepresenteerd in de vorm van diavoorstellingen met aangepaste presentatie-instellingen.

## Korte geschiedenis

Het PPTX-bestandsformaat werd geïntroduceerd in 2007 en maakt gebruik van de Open XML-standaard die in 2000 door Microsoft is aangepast. Voorafgaand aan PPTX was het gebruikelijke bestandsformaat PPT dat een puur binair bestandsformaat was. Het nieuwe bestandstype heeft voordelen toegevoegd van kleine bestandsgroottes, minder veranderingen van corruptie en goed opgemaakte afbeeldingen. Het was in het begin van 2000 toen Microsoft besloot om voor de verandering te gaan om de standaard voor **Office Open XML** te accommoderen. In 2007 werd dit nieuwe bestandsformaat onderdeel van Office 2007 en wordt het ook voortgezet in de nieuwe versies van Microsoft Office.

## Specificaties PPTX-bestandsindeling

Bestanden die zijn gegenereerd met Office Open XML-bestandsindeling is een verzameling XML-bestanden samen met andere bestanden die koppelingen bieden tussen alle samenstellende bestanden. Deze verzameling is eigenlijk een gecomprimeerd archief dat kan worden uitgepakt om de inhoud ervan te bekijken. Om dit te doen, hernoemt u de PPTX-bestandsextensie met zip en extraheert u deze om de inhoud te bekijken (zie [specificaties voor PPTX-bestandsindeling](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/ efd8bb2d-d888-4e2e-af25-cad476730c9f) door Microsoft).

De volgende paragrafen werpen enig licht op elk van deze.

### [Content_Types].xml

Dit is het enige bestand dat op het basisniveau wordt gevonden wanneer de zip wordt uitgepakt. Het vermeldt de inhoudstypen voor onderdelen in het pakket. Alle verwijzingen naar de XML-bestanden die in het pakket zijn opgenomen, worden in dit XML-bestand verwezen. Hieronder volgt een inhoudstype voor een diagedeelte:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

Als er nieuwe onderdelen aan het pakket moeten worden toegevoegd, kan dit worden gedaan door het nieuwe onderdeel toe te voegen en eventuele relaties binnen de .rels-bestanden bij te werken. Houd er rekening mee dat voor een dergelijke wijziging ook de Content_Types.xml moet worden bijgewerkt.

### \_rels (map) ###

Relaties tussen de andere onderdelen en resources buiten het pakket worden onderhouden door het relatiegedeelte. De map Relaties bevat één XML-bestand waarin de relaties op pakketniveau zijn opgeslagen. Links naar de belangrijkste delen van de PPTX-bestanden zijn als URI's in dit bestand opgenomen. Deze URI's identificeren het type relatie van elk belangrijk onderdeel met het pakket. Dit omvat de relatie met het primaire kantoordocument dat zich bevindt als ppt/presentation.xml en andere delen binnen docProps als kern- en uitgebreide eigenschappen.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
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
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
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

* [[MS-PPTX] - PPTX-bestandsindeling](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

