{
  "date" : "2020-03-16",
  "keywords" :[ "IGES-bestand", "Bestandsindeling", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over IGES-bestandsindelingen en API's die IGES-bestanden kunnen maken en openen.",
  "title" :"IGES-bestandsindeling",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Wat is een IGES-bestand?

Een bestand met de extensie .iges wordt gebruikt om ontwerpinformatie uit te wisselen tussen CAD-toepassingen (computer-aided design). IGES staat voor Initial Graphics Exchange Specifications. Informatie die wordt uitgewisseld met behulp van IGES omvat schakelschema's, draadframes, vrije-vormoppervlakken of solide modelleringsweergaven. IGES vindt zijn toepassingen in traditionele technische tekeningen, modelanalyse en productiefuncties. Het formaat kan zowel 2D- als 3D-ontwerpinformatie uitwisselen tussen CAD-programma's. IGES-bestanden kunnen worden geopend met verschillende CAD-toepassingen zoals Autodesk en CADSoftTools ABViewer. Er zijn ook verschillende API's beschikbaar om IGES-bestanden programmatisch te openen en te converteren.

## IGES-bestandsindeling

IGES-bestanden zijn in ASCII-tekstindeling en kunnen in elke teksteditor worden geopend om de inhoud van het bestand te bekijken. Tekstuele informatie in een IGES-bestand wordt weergegeven in "Hollerith"-formaat. Een algemeen IGES-bestand kan duizenden regels bevatten om de 2D- of 3D-informatie weer te geven die volgens dit formaat kan worden uitgewisseld. Een IGES-bestand is opgesplitst in vijf secties, aangegeven met de specifieke hoofdletter in de 73e kolom. Die secties zijn `Start` (S), `Global` (G), `Data Entry` (D), `Parameter Data` (P) en `Terminate` (T) secties. De secties Gegevensinvoer en Parametergegevens worden gewoonlijk respectievelijk afgekort als DE en PD.

### IGES-bestandskop

De secties Start en Globaal bevatten basisinformatie over:
* Naam van het bestand en de bron
* Scheidingstekens voor de sectie Parametergegevens
* Auteur van het bestand en andere algemene informatie.

Start- en Global-secties uit het voorbeelddocument op Wikipedia zijn als volgt.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Zoals te zien is, bevat het startveld voor mensen leesbare beschrijvingen van het bestand, en ik heb tekens in kolommen 1-72, waarbij de regel eindigt met de sectiekop en het sectieregelnummer. Er moet minimaal 1 regel van de sectie Start zijn. Het globale gedeelte bevat preprocessorgegevens. Het moet ook aanwezig zijn in het bestand en eindigen met het G000000#-formaat.

### Gegevensinvoer (DE) en parametergegevens (PD) Sectie

#### Gegevensinvoersectie
Een IGES-bestand bestaat uit verschillende entiteiten die de informatie over de basisgegevens van het IGES-bestandsformaat bevatten. Een entiteit bevat informatie over verschillende elementen van een IGES-gegevensformaat en wordt gebruikt voor tekenen. Meer algemeen gebruikte entiteiten zijn onder meer:
* Cirkelboog
* Samengestelde curve
* Conische boog
* Vlak
* Lijn

Dit zijn er maar een paar en er zijn ongeveer 150 verschillende entiteiten in IGES. Elke entiteit wordt geïdentificeerd door een typenummer, zoals:
* CIRKEL BOOG (Type 100)
* LIJN (Type 110)

##### Entiteitseigenschappen

Elke gedeclareerde entiteit heeft de volgende eigenschappen.

|Veldnaam|Beschrijving|
---|---|
|Entiteitstype |Dit is het type entiteit dat wordt beschreven. 116 beschrijft bijvoorbeeld een entiteit Punt.|
|PD-pointer |Dit geeft de locatie voor deze entiteitsgegevens in de sectie Parametergegevens. Deze locatie is gewoon het regelnummer binnen de PD-sectie met de eerste regel van deze entiteitsgegevens.|
|Structure |Zero of pointer naar definitie-entiteit. Niet van toepassing voor de meeste entiteiten|
|Lijn lettertypepatroon| Nummer of aanwijzer naar lijnlettertypepatroonentiteit. Getal betekent: * 0 Geen patroon gespecificeerd (standaard) * 1 Effen * 2 Gestreept * 3 Fantoom * 4 Middellijn * 5 Gestippeld|
|Niveau| Specificeert niveaus die aan deze entiteit moeten worden gekoppeld. Staat toe dat entiteit op meer dan één niveau verschijnt|
|Bekijken| Specificeert weergave-opties. Dit zijn: 0 Geeft gelijke zichtbaarheid en kenmerken in alle weergaven aan. Standaardaanwijzer naar de View-entiteit (Type 410) waaruit deze kan worden bekeken Verwijs naar een View Visible Associativity-entiteit (Type 402, Form 3)
|Transformatiematrixaanwijzer| Verwijst naar een transformatiematrixentiteit (Type 124) of is standaard nul (geen transformatie)|
|Label Display Associativiteit| Verwijst naar een labelweergave-associativiteit (type 402, formulier 5) die definieert hoe het entiteitslabel wordt weergegeven.|
|Statusnummer| Bevat vier secties van twee nummers. 1-2: blanco status. Ofwel 00 voor normaal of 01 voor blanco. 3-4: Ondergeschikte entiteitsschakelaar: is 00 voor onafhankelijk, 01 voor fysiek afhankelijk, 02 voor logisch afhankelijk en 03 voor beide. 5-6: Entiteit Gebruik vlag: is ofwel 00 voor Geometrie, 01 voor annotatie, 02 voor definitie, 03 voor Overige, 04 voor Logisch, 05 voor 2D parametrisch, en 06 voor Constructiegeometrie. Ten slotte is 7-8 de hiërarchie, waarbij 00 globaal top-down aangeeft (gebruik de kenmerken van deze entiteit), 01 is globaal uitstellen (gebruik de kenmerken van deze entiteit niet), en 02 is gebruik hiërarchie-eigenschap (gebruik hiërarchie-entiteit (Type 406, Formulier) 10) om kenmerken van hiërarchische groepering te bepalen).|
|Volgnummer| Gespecificeerd door D#, waarbij # het regelnummer is voor deze sectie (niet vanaf de bovenkant van het bestand). Dit wordt ook gebruikt om naar deze entiteit voor gegevensinvoer te verwijzen.|
|Entiteitstype| het wordt twee keer gespecificeerd per entiteitslijst|
|Lijngewichtnummer| Specificeert de dikte bij het weergeven van entiteit. Kleinste is 1, 0 is standaard|
|Kleurnummer| Specificeert de entiteitskleur. Toegestane gehele waarden zijn: 0 Geen kleur (standaard) 1 Zwart 2 Rood 3 Groen 4 Blauw 5 Geel 6 Magenta 7 Cyaan 8 Wit|
|Parameterregel telnummer| Specificeert het aantal regels dat deze entiteit inneemt in de Parameter Data Section|
|Formuliernummer| Geeft de vorm of de representatie van deze entiteit aan. Wijzigt hoe de parametergegevens worden geïnterpreteerd. Standaard is 0|
|Gereserveerd veld| Niet gebruikt|
|Gereserveerd veld| Niet gebruikt|
|Entiteitslabel| Toepassing gespecificeerde identifier-recht gerechtvaardigd|
|Abonnementsnummer| Numerieke kwalificatie voor het entiteitslabel. Beide vormen samen een unieke identificatie voor de entiteit|
|Volgnummer Zie hierboven. |Dit wordt D#+1, aangezien elke entiteit op twee regels wordt gespecificeerd.|

#### Parametergegevenssectie
Het gedeelte Gegevensinvoer wordt gevolgd door het gedeelte Parametergegevens. Het geeft een overzicht van de gegevens voor elk respectief item en geeft een lijst van parameters voor de entiteit op basis van de scheidingstekens die zijn opgegeven in de sectie Globaal (meestal komma's om parameters te scheiden en een puntkomma om de lijst te beëindigen).


## Referenties
* [IGES door WikiPedia](https://en.wikipedia.org/wiki/IGES)

