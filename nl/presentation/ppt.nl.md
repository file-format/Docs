{
  "date" : "2019-12-13",
  "keywords" :[ "ppt-bestand", "ppt-bestandsindeling", "wat is een ppt-bestand", "bestand", "ppt-voorbeeld", "ppt-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over PPT-bestandsindeling en API's die PPT-bestanden kunnen maken en openen.",
  "title" :"PPT - PowerPoint-bestandsindeling",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een PPT-bestand?

Een bestand met de PPT-extensie vertegenwoordigt een PowerPoint-bestand dat bestaat uit een verzameling dia's voor weergave als SlideShow. Het specificeert het binaire bestandsformaat dat wordt gebruikt door Microsoft PowerPoint 97-2003. Een PPT-bestand kan verschillende soorten informatie bevatten, zoals tekst, opsommingstekens, afbeeldingen, multimedia en andere ingesloten OLE-objecten. Microsoft kwam met een nieuwere bestandsindeling voor PowerPoint, bekend als [PPTX](/nl/presentation/pptx/), vanaf 2007, die is gebaseerd op Office OpenXML en verschilt van deze binaire bestandsindeling. Verschillende andere applicatieprogramma's zoals OpenOffice Impress en Apple Keynote kunnen ook PPT-bestanden maken.

## Korte geschiedenis ##

Microsoft introduceerde het PPT-bestandsformaat met de release van PowerPoint in 1987. Het stabiele binaire formaat werd als standaard gedeeld in PowerPoint 97-2003 voor Windows. Het binaire bestandsformaat wordt ondersteund voor lezen en schrijven door de meest recente versies van PowerPoint, inclusief PowerPoint 2016.

## Specificaties bestandsindeling ##

Sinds de introductie heeft het PPT-bestandsformaat verschillende revisies ondergaan voor toevoegingen van nieuwe functies en verbeteringen. De nieuwste versiespecificaties die beschikbaar zijn, zijn die van revisie 6.0 die in augustus 2018 zijn gepubliceerd en die niet mogen worden gemengd met het echte productnummer van het PPT-bestandsformaat, aangezien Microsoft geen wijzigingen meer aanbrengt voor dit formaat.

### Overzicht bestandsindeling ###

Enkele van de belangrijkste componenten van een PPT-bestandsindeling zijn als volgt:

#### Dia's ####

Gebruikersgegevens zoals vormen, tekst, animaties en media worden toegevoegd aan een presentatie in een dia. Een presentatie kan een of meer dia's bevatten die als diavoorstelling worden weergegeven wanneer een presentatie wordt uitgevoerd. Een presentatie bevat basisdia's en titeldia's die fungeren als sjabloon voor de algemene visuele eigenschappen van presentatiedia's. Er is ook een basisdia voor notities en een basisdia voor hand-outs die een soortgelijk doel dienen en gemeenschappelijke visuele eigenschappen bieden voor alle dia's met notities en alle afgedrukte hand-outs.

#### Vormen ####

Vormen zijn objecten waarmee gebruikers een verscheidenheid aan inhoud aan een dia kunnen toevoegen in de vorm van tijdelijke aanduidingen, afbeeldingen en grafieken. Vormen op een basisdia definiëren algemene gegevens voor groepen vormen.

#### Tijdelijke aanduidingen Vormen ####

Dit zijn speciale tijdelijke aanduidingen die dienen als containers voor een verscheidenheid aan objecten. Er kunnen verschillende vormen voor tijdelijke aanduidingen worden gebruikt om aanwijzingen te geven voor het invoegen van specifieke soorten vormen, zoals tabellen of grafieken. Binnen een dia neemt een vorm van een tijdelijke aanduiding de visuele eigenschappen van een hoofdmodeldia, titelmodeldia of notitiemodeldia aan.

#### Externe objecten ####

Externe objecten zoals ingesloten en gekoppelde audio, gekoppelde video, ingesloten en gekoppelde OLE-objecten en hyperlinks kunnen in een dia worden ingesloten. Deze objecten kunnen worden gebruikt om gekoppelde objecten te activeren voor toegang tot externe bronnen tijdens een diavoorstelling.

### Bestandsformaatstructuren ###

De binaire bestandsindelingen van PowerPoint bestaan uit de volgende stromen om de algemene documentstructuur en gegevens weer te geven.

* Huidige gebruikersstream
* PowerPoint-documentstream
* Foto's streamen
* Samenvattingsinformatie en Document Samenvattingsinformatie (optioneel)

De volledige specificaties voor het DOC-bestandsformaat kunnen worden gevonden door [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) en moeten worden geraadpleegd met verwijzing naar de secties die in de volgende details worden genoemd.

#### Huidige gebruikersstroom ####

Het houdt de laatste gebruiker bij die het document heeft geopend en de naam moet "Huidige gebruiker" zijn.

#### PowerPoint-documentstroom ####

Houdt alle informatie over een PowerPoint-presentatie bij en legt de lay-out en inhoud uit. Het is een vereiste stream waarvan de naam "PowerPoint-document" MOET zijn. De inhoud van deze stream wordt gespecificeerd door een reeks records op het hoogste niveau. Gedeeltelijke bestelbeperkingen voor de recordvolgorde worden gespecificeerd in de PersistDirectoryAtom- en UserEditAtom-records.

Als containerrecords zijn de DocumentContainer-, MainMasterContainer (paragraaf 2.5.3), HandoutContainer (paragraaf 2.5.8), SlideContainer (paragraaf 2.5.1) en NotesContainer (paragraaf 2.5.6) records elk de root van een boom met containerrecords en atoomrecords. Binnen elk containerrecord kunnen andere records voorkomen die niet expliciet als onderliggende records worden vermeld. Onbekende records worden geïdentificeerd wanneer het veld recType van de RecordHeader-structuur (paragraaf 2.3.1) een waarde bevat die niet is gespecificeerd door de RecordType-opsomming (paragraaf 2.13.24). Deze onbekende records MOETEN, als ze worden aangetroffen, worden genegeerd en KUN <1> worden bewaard. Onbekende records kunnen worden genegeerd door recLen-bytes voorwaarts te zoeken vanaf het einde van de RecordHeader-structuur.

Elke keer dat deze stream wordt geschreven, kunnen nieuwe records op het hoogste niveau, een gebruikersbewerking, worden toegevoegd aan de bestaande stream, of de volledige inhoud van de stream kan worden vervangen door een bijgewerkte reeks records op het hoogste niveau. Als de volledige stream niet wordt vervangen, kunnen alle eerder bestaande records op het hoogste niveau die een eerdere gebruikersbewerking bevatten, verouderd worden gemaakt door de vervolgens toegevoegde records op het hoogste niveau die de huidige gebruikersbewerking omvatten.

#### Foto's streamen ####

Dit is een optionele stream die gegevens bevat over de afbeeldingen in een PowerPoint-presentatie. De naam MOET "Foto's" zijn. De inhoud van deze stream wordt gespecificeerd door het OfficeArtBStoreDelay-record zoals gespecificeerd in [MS-ODRAW] sectie 2.2.21.

#### Samenvatting informatiestroom ####

Het houdt statistieken bij over het document volgens de Microsoft Office-standaard. De naam van de samenvattingsinformatiestroom moet "\005SummaryInformation" zijn, waarbij \005 het teken is met de waarde 0x0005, niet de letterlijke tekenreeks "\005". Deze stream MOET worden weggelaten voor versleutelde documenten. De inhoud van deze stream wordt gespecificeerd in [MS-OSHARED] paragraaf 2.3.3.2.1.

#### Document Samenvatting Informatiestroom ####

Een optionele stream waarvan de naam "\005DocumentSummaryInformation" MOET zijn, waarbij \005 het teken is met de waarde 0x0005, niet de letterlijke tekenreeks "\005". Deze stream KAN <2> worden weggelaten voor versleutelde documenten. De inhoud van deze stream wordt gespecificeerd in [MS-OSHARED] sectie 2.3.3.2.2.

#### Versleutelde samenvatting informatiestroom ####

Een optionele stream waarvan de naam "EncryptedSummary" MOET zijn. Deze stream bestaat alleen in een versleuteld document. De inhoud van deze stream wordt gespecificeerd in [MS-OFFCRYPTO] paragraaf 2.3.5.4.

#### Digitale handtekening opslag ####

Een optionele opslag waarvan de naam "_xmlsignatures" MOET zijn. Het KAN worden weggelaten en KUNNEN worden genegeerd. De inhoud van deze opslag wordt gespecificeerd in [MS-OFFCRYPTO] paragraaf 2.5.2.

#### Aangepaste XML-gegevensopslag ####

Een optionele opslag waarvan de naam "MsoDataStore" MOET zijn. De inhoud van de opslag wordt gespecificeerd in [MS-OSHARED] paragraaf 2.3.6.

#### Handtekeningen streamen ####

Een optionele stream waarvan de naam "_signatures" MOET zijn. Het MOET worden weggelaten en MAG worden genegeerd. De inhoud van deze stream wordt gespecificeerd in [MS-OFFCRYPTO] paragraaf 2.5.1.

## Referenties ##

* [specificaties PPT-bestandsindeling](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: gemeenschappelijke gegevenstypen en objectstructuren van Office](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Cryptografiestructuur voor Office-documenten](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [PowerPoint-bestandsindelingen](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

