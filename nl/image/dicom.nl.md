{
  "date" : "2019-10-11",
  "keywords" :[ "dicom-bestand", "dicom-bestandsindeling", "wat is een dicom-bestand", "bestand", "dicom-voorbeeld", "dicom-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - Digitale beeld- en communicatiebestandsindeling",
  "description":"Meer informatie over DICOM-bestandsindelingen en API's die DICOM-bestanden kunnen maken en openen.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een DICOM-bestand?

DICOM is de afkorting voor Digital Imaging and Communications in Medicine en heeft betrekking op het vakgebied Medische Informatica. DICOM wordt gebruikt voor de integratie van medische beeldvormingsapparatuur zoals printers, servers, scanners enz. van verschillende leveranciers en bevat ook identificatiegegevens van elke patiënt voor uniekheid. DICOM-bestanden kunnen tussen twee partijen worden gedeeld als ze beeldgegevens in DICOM-indeling kunnen ontvangen. Het communicatiegedeelte van DICOM is een applicatielaagprotocol en gebruikt TCP/IP om te communiceren tussen entiteiten. Versies die worden ondersteund door webservices zijn 1.0, 1.1, 2 of hoger.

## Geschiedenis ##

DICOM is gezamenlijk ontwikkeld door American College of Radiology (ACR) en National Electrical Manufacturers Association (NEMA) voor het uitwisselen en bekijken van medische beelden zoals MRI's, CT-scans en echografiebeelden. Aanvankelijk was het moeilijk om de afbeeldingen te decoderen die de machines produceerden. Daarom vormden ACR en NEMA in 1983 samen een team dat in 1985 zijn eerste standaard, ACR/NEMA 300, uitbracht. De tweede versie werd uitgebracht in 1988, die populairder was bij leveranciers, maar al snel realiseerde men zich dat de tweede versie ook verbeterd moest worden. De 3e versie van de standaard werd in 1993 uitgebracht als "DICOM". 3.0 is nog steeds de nieuwste versie, maar wordt sinds 1993 voortdurend bijgewerkt.

## DICOM-bestandsindeling ##

DICOM is de combinatie van bestandsformaatdefinitie en een netwerkcommunicatieprotocol. DICOM gebruikt de .DCM-extensie. .DCM bestaat in twee verschillende formaten, namelijk formaat 1.x en formaat 2.x. DCM Format 1.x is verder beschikbaar in twee versies normaal en uitgebreid. Voor de webservices van DICOM worden HTTP- en HTTPS-protocollen gebruikt.

### Bestandskop ###

De bestandskop bevat een bestandspreamble van 128 bytes en een DICOM-voorvoegsel van 4 bytes.

**Preambule # 128 Bytes**|**Prefix # 4 Bytes “D, I, C, M**

**Preambule** wordt gebruikt om toegang te krijgen tot de afbeeldingen en andere gegevens in het DICOM-bestand en biedt compatibiliteit met veelgebruikte afbeeldingsbestandsindelingen.

**Voorvoegsel** bevat de tekenreeks "DICM" als hoofdletters.

### Gegevensset ###

Elk bestand moet een enkele dataset bevatten die SOP-instantie en SOP-klasse met gerelateerde IOD vertegenwoordigt. Dataset is de weergave van informatie uit de echte wereld. Dataset bevat data-elementen en data-elementen bevatten waarden van de attributen van dat object. De structuur van attributen wordt gespecificeerd in IOD's. Een DICOM-gegevensobject bestaat uit een aantal attributen, waaronder items zoals naam, ID, enz., en ook één speciaal attribuut dat de beeldpixelgegevens bevat.

### Gegevenselementen ###

Data-element bestaat uit data-element Tag, Value lengte en waarde voor het Data Element. Er zijn 5 soorten data-elementen, namelijk Type 1 Vereiste Data-elementen, Type 1C Voorwaardelijke Data-elementen, Type 2 Vereiste Data-elementen, Type 2C Voorwaardelijke Data-elementen en Type 3 optionele Data-elementen. Basis Drie soorten data-elementstructuren zijn als volgt.

**Gegevenselement met een expliciete VR**

|Groepsnummer|Elementnummer|Waardeweergave|Gereserveerd|Waardelengte|Waardeveld
---|---|---|---|---|---|
|2 Bytes|2 Bytes|2 Bytes|2 Bytes # 0x00, 0x00|4 Bytes|"Waardelengte Bytes"

**Gegevenselement met een expliciete VR**

|Groepsnummer|Elementnummer|Waardeweergave|Waardelengte|Waardeveld
---|---|---|---|---|
|2 bytes|2 bytes|2 bytes|2 bytes|"Waardelengte bytes"

**Gegevenselement met een impliciete VR**


|Groepsnummer|Elementnummer|Waardelengte|Waardeveld
---|---|---|---|
|2 bytes|2 bytes|4 bytes|"Waardelengte bytes"

1. **Data Element Tag**: een geordend geheel getal dat het groepsnummer en het elementnummer vertegenwoordigt
1. **Waardeweergave VR**: VR is een tekenreeks die de VR van het gegevenselement vertegenwoordigt.
1. **Waardelengte**: is het niet-ondertekende geheel getal dat de expliciete lengte van het waardeveld vertegenwoordigt.
1. **Waardeveld**: beschrijft de waarden van de gegevenselementen.

## Syntaxis overzetten ##

Overdrachtsyntaxis is een set regels voor codering om ondubbelzinnig meer abstracte syntaxis weer te geven. Met behulp van overdrachtsyntaxis onderhandelen communicerende entiteiten over gemeenschappelijke coderingstechnieken die zij ondersteunen.

## SOP's ##

Unie van IOD en DIMSE definieert een SOP-klasse. De SOP Class-definitie bevat de regels en semantiek die het gebruik van de services in de DIMSE Service Group of de Attributen van de IOD kunnen beperken. Voorbeelden van service-elementen zijn Opslaan, Ophalen, Zoeken, Verplaatsen, enz. Voorbeelden van objecten zijn CT-beelden, MR-beelden, maar ook planningslijsten, afdrukwachtrijen, enz.

## Diensten ##

DICOM levert diverse diensten, veelal gerelateerd aan de communicatie van data. Elk wordt hieronder kort beschreven:


**Store:** De DICOM Store-service stuurt afbeeldingen of andere objecten naar een beeldarchiverings- en communicatiesysteem (PACS) of server.


**Storage commitment:** Storage commitment service wordt gebruikt om te bevestigen dat een afbeelding permanent is opgeslagen op een apparaat op elk type media.


**Query/retrieve:** Met deze service kan een werkstation de lijsten met afbeeldingen of andere objecten vinden en deze vervolgens ophalen uit PACS.


**Modaliteitswerklijst:** De modaliteitswerklijstservice geeft een lijst met beeldvormingsprocedures die zijn gepland voor uitvoering door een beeldacquisitieapparaat.


**Afdrukken:** Deze service stuurt afbeeldingen naar de printer.

## Poortnummers via IP ##

DICOM gebruikt de volgende TCP- en UDP-poorten:

1. 104
1. 2761
1. 2762
1. 11112

## Referenties ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

