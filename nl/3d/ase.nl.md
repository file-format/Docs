{
  "date" : "2021-01-22",
  "keywords" :[ "ASE", "bestand", "formaat", "bestandstype", "extensie", "wat is een ASE-bestand?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over ASE-bestandsindeling en API's die ASE-bestanden kunnen openen en maken.",
  "title" :"ASE - Autodesk ASCII-scène-exportbestand",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## Wat is een ASE-bestand?

Een bestand met de extensie .ase is een Autodesk ASCII Scene Export-bestandsindeling die een ASCII-weergave is van een scène, die 2D- of 3D-informatie bevat tijdens het exporteren van scènegegevens met Autodesk. Autodesk biedt opties om scènecomponenten op te nemen tijdens het exporteren van scènegegevens. U kunt mesh-definitie opnemen samen met vertex- en gezichtsinformatie, materiaalbeschrijving, transformatie-animatiegegevens voor de objecten, volledige mesh-definitie van elke n frames, animatiegegevens voor camera's en lichten en IK-verbindingsinstellingen.

## ASE-bestandsindeling - Meer informatie

ASE-bestanden zijn tekstbestanden die zijn opgeslagen in ASCII-indeling en die in elke teksteditor kunnen worden geopend. Een ASE-bestand kan de volgende soorten informatie bevatten die door Autodesk worden verstrekt.

### Uitvoeropties

* `Mesh Definition` - Exporteert de definitie van elke mesh, inclusief vertex- en vlakinformatie voor geometrische objecten. Als u dit inschakelt, worden bovendien de items in het groepsvak Mesh-opties ingeschakeld, zoals hieronder beschreven.
* `Materialen` - Bevat de materiaalbeschrijving. Als een materiaal niet aan een object is toegewezen, wordt de draadframekleur geëxporteerd. Alle niveaus van een materiaalboom zijn inbegrepen, dus dit kan veel tekst opleveren.
* `Transform Animation Keys` - Bevat de transformatie-animatiegegevens voor de objecten. Als het object een doelcamera of spotlight is, bevat dit doelanimatiegegevens.
* `Geanimeerde Mesh` - Exporteert een volledige mesh-definitie van elke n frames. De frequentie wordt gespecificeerd door de Controller Output spinner, zoals hieronder beschreven. Elk blok bevat dezelfde informatie die is gespecificeerd in het groepsvak Mesh-opties, zoals hieronder beschreven. Als u dit inschakelt, kan dit resulteren in een enorm bestand, zelfs voor kleine scènes.
* `Geanimeerde camera-/lichtinstellingen` - Exporteert de animatiegegevens voor camera's en lichten, zoals kleur, intensiteit, uitval, kaartbias, enzovoort. Voert elke n frames een blok uit, zoals gespecificeerd door de Controller Output-spinner.
* `Inverse Kinematic Joints` - Exporteert de IK-gewrichtsinstellingen in de Hiërarchie-tak.

### Objecttypen

Met de items hier kunt u aangeven welke categorie objecten u in de uitvoer wilt opnemen. U kunt geometrische objecten, vormen, camera's, lichten en hulpobjecten opnemen.

* Geometrisch
* Vormen
* Camera's
* Lichten
* Helpers

### Mesh-opties

* `Mesh Normals` - Exporteert de face en vertex normals. De normaal van het gezicht wordt als eerste vermeld, gevolgd door de normalen van de drie hoekpunten die het gezicht ondersteunen. Als u dit inschakelt, krijgt u een veel groter bestand.
* `Kaartcoördinaten` - Exporteert een lijst met toewijzingshoeken en vlakken, volgens de TVert- en TVFace-structuren die zijn beschreven in de 3ds Max Software Development Kit. Als een object gezichtstoewijzing gebruikt, wordt een lijst met gezichtskaarten geëxporteerd met UVW-coördinaten voor elk gezicht.
* `Vertex Colors` - Exporteert vertex-kleuren.

### Controller-uitgang

* `Gebruik sleutels` - Exporteert sleutelwaarden. Als de controller geen toetsen gebruikt, wordt de Force Sample-methode gebruikt. In het geval van transformatiecontrollers werkt de optie Sleutels gebruiken alleen als alle transformatiecontrollers Lineair/TCB of Bezier zijn. Als een van de transformatietracks een ander type controller gebruikt, wordt de Force Sample-methode gebruikt voor alle transformatietracks.
* `Force Samples` - Samplet controllerwaarden op basis van de frequentie die is gespecificeerd in de Frames per Sample Controller.

## Referenties

* [Autodesk - Exporteren naar ASCII](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2020/ENU/3DSMax-Data-Exchange/files/GUID-98B2388D -A3A7-4096-8E81-888A3F9D6069-htm.html)

