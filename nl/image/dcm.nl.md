{
  "date" : "2019-10-11",
  "keywords" :[ "dcm file", "dcm file format", "wat is een dcm file", "file", "dcm example", "dcm file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCM-bestandsformaat - digitaal medisch informatiebestand",
  "description":"Meer informatie over DCM-bestandsindeling en API's die DCM-bestanden kunnen maken en openen.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## Wat is een DCM-bestand?

Bestanden met de extensie .dcm vertegenwoordigen een digitaal beeld waarin medische informatie van patiënten is opgeslagen, zoals MRI's, CT-scans en echografiebeelden. DCM-bestanden gebruiken het [DICOM](/nl/image/dicom) (Digital Imaging and Communications in Medicine) beeldbestandsformaat en kunnen patiëntinformatie bevatten ter referentie. Het is ontwikkeld door de [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) en was bedoeld om het bestandsformaat voor beeldvorming te standaardiseren voor het distribueren en bekijken van medische beelden.

## DCM-bestandsindeling

DCM-bestanden slaan informatie op in DICOM-beeldformaat. Deze bestanden slaan de gegevensset op, wat informatie uit de echte wereld is, die een SOP-instantie vertegenwoordigt die verband houdt met een DICOM IOD. DICOM-bestandsmeta-informatie wordt opgeslagen in het bestand, gevolgd door de bytestroom van de feitelijke gegevensset.

### DICOM-bestandsmeta-informatie ##

Elk DICOM-bestand bevat een identificatie-informatiekop voor de ingekapselde dataset die bestaat uit:
* Een 128-byte bestandspreambule
* 4 byte DICOM-voorvoegsel
* Bestandsmeta-elementen

Deze header is een must voor elk DICOM-bestand.

### Bestandsmeta-elementen ###
|Attribuutnaam|Tag|Type| Kenmerk Beschrijving
---|---|---|---|
|Bestandspreambule|Geen tag- of lengtevelden|1|Een vast veld van 128 bytes beschikbaar voor toepassingsprofiel of door implementatie gespecificeerd gebruik. Indien niet gebruikt door een applicatieprofiel of een specifieke implementatie, worden alle bytes ingesteld op 00H. File-set Readers of Updaters zullen niet vertrouwen op de inhoud van deze Preambule om te bepalen of dit Bestand al dan niet een DICOM-bestand is.
|DICOM-prefix|Geen tag- of lengtevelden|1|Vier bytes met de tekenreeks "DICM". Dit voorvoegsel is bedoeld om te worden gebruikt om te herkennen dat dit bestand al dan niet een DICOM-bestand is.
|File Meta Information Group Length|(0002.0000)|1|Aantal bytes volgend op dit File Meta Element (einde van het veld Waarde) tot en met het laatste File Meta Element van de Group 2 File Meta Information
|File Meta Information Version|(0002.0001)|1|Dit is een veld van twee bytes waarin elke bit een versie van deze File Meta Information-header identificeert. In versie 1 is de eerste bytewaarde 00H en de tweede waardebytewaarde is 01H. Implementaties die bestanden lezen met meta-informatie waarbij dit attribuut bit 0 (lsb) van de tweede byte heeft ingesteld op 1 kunnen de bestandsmeta-informatie interpreteren zoals gespecificeerd in deze versie van PS3.10. Alle andere bits worden niet gecontroleerd.
|Media Storage SOP Class UID|(0002.0002)|1|Identificeert op unieke wijze de SOP Class die is gekoppeld aan de dataset. SOP Class UID's die zijn toegestaan voor media-opslag worden gespecificeerd in PS3.4 - Media Storage Application Profiles.
|Media Storage SOP Instance UID|(0002,0003)|1|Identificeert op unieke wijze de SOP-instance die is gekoppeld aan de dataset die in het bestand is geplaatst en de meta-informatie van het bestand volgt.
|Transfer Syntax UID|(0002.0010)|1|Identificeert op unieke wijze de Transfer Syntax die wordt gebruikt om de volgende dataset te coderen. Deze overdrachtssyntaxis is niet van toepassing op de bestandsmeta-informatie.
|Implementatieklasse UID|(0002.0012)|1|Identificeert op unieke wijze de implementatie die dit bestand en de inhoud ervan heeft geschreven. Het geeft een eenduidige identificatie van het type implementatie dat het bestand het laatst heeft geschreven in het geval van uitwisselingsproblemen.
|Implementation Version Name|(0002.0013)|3|Identificeert een versie voor een implementatieklasse UID (0002.0012) die maximaal 16 tekens van het repertoire gebruikt.
|Bron Application Entity Title|(0002.0016)|3|De DICOM Application Entity (AE) Titel van de AE die de inhoud van dit bestand heeft geschreven (of het laatst heeft bijgewerkt). Indien gebruikt, kan de bron van fouten worden opgespoord in het geval van problemen met de uitwisseling van media.
|Private Information Creator UID|(0002.0100)|3|De UID van de maker van de privé-informatie (0002.0102).
|Privé-informatie|(0002.0102)|1C|Bevat privé-informatie die in de bestandsmeta-informatie is geplaatst. De maker wordt geïdentificeerd in (0002.0100). Vereist als Private Information Creator UID (0002.0100) aanwezig is.

### Dataset inkapseling ###

Een DICOM-bestand bevat een enkele gegevensset die een enkele SOP-instantie vertegenwoordigt die verband houdt met een enkele SOP-klasse. De overdrachtsyntaxis-UID van de meta-informatie van het DICOM-bestand definieert de overdrachtsyntaxis die wordt gebruikt om de gegevensset te coderen.

### Ondersteuning voor bestandsbeheerinformatie ###

De media-indelingslaag biedt indien nodig de volgende bestandsbeheerinformatie voor een bepaald DICOM-toepassingsprofiel.

* Identificatie van de eigenaar van de inhoud van het bestand

* Statistieken over bestandstoegang (bijv. datum en tijd van aanmaak)

* Toegangscontrole voor toepassingsbestanden

* Toegangscontrole fysieke media (bijv. schrijfbeveiliging)

## Referenties ##
* [DICOM-standaard](https://www.dicomstandard.org/current/)
* [DICOM-bestandsindeling](http://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

