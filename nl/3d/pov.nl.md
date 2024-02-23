
{
  "date": "2023-01-05",
  "keywords": [
"pov-bestand",
"pov-bestandsformaat",
"wat is een pov-bestand",
"bestand",
"pov voorbeeld",
"pov-bestandsextensie",
"verlenging",
"formaat"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Leer meer over de POV-bestandsindeling en API's waarmee POV-bestanden kunnen worden geopend en gemaakt.",
  "title": "POV - Bestand voor persistentie van het gezichtsvermogen",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-nlv"
}
},
  "lastmod": "2023-01-05"
}

## Wat is een POV-bestand?

Een POV-bestand is een tekstbestand met instructies voor de POV-Ray ray tracing-software. Deze instructies zijn geschreven in een speciale scripttaal die specifiek is voor POV-Ray. Het specificeert de scène die moet worden weergegeven, inclusief de 3D-objecten, materialen, verlichting en andere eigenschappen die het uiterlijk van de scène bepalen. POV-bestanden gebruiken een speciale scripttaal die specifiek is voor POV-Ray en kan worden gebruikt om complexe en gedetailleerde 3D-scènes te creëren. De bestandsextensie voor een POV-bestand is doorgaans .pov of .povray. Wanneer u een POV-bestand opent in POV-Ray, leest de software de instructies in het bestand en gebruikt deze om een gerenderd beeld van de scène te genereren.

De .pov-bestanden worden vaak door kunstenaars en ontwerpers gebruikt om 3D-graphics en animaties te maken voor een verscheidenheid aan toepassingen, waaronder film, televisie, videogames en marketingmateriaal.

## POV-bestandsformaat

Het **.pov-bestand** begint doorgaans met een reeks **#include**-instructies, die worden gebruikt om bibliotheken met vooraf gedefinieerde kleuren, texturen en andere bronnen op te nemen die in de scène kunnen worden gebruikt. Vervolgens definieert het bestand de objecten, materialen en andere eigenschappen van de scène met behulp van een reeks blokken. Er zijn veel andere soorten objecten, materialen en andere eigenschappen die u in een .pov-bestand kunt opgeven, en u kunt loops en voorwaardelijke instructies gebruiken om complexere en gedetailleerdere scènes te maken.

## Softwareapplicaties voor POV

Het .pov-bestandsformaat wordt gebruikt door de POV-Ray ray tracing-software, dus de primaire toepassing voor het openen van .pov-bestanden is de POV-Ray-software zelf. Je kunt de nieuwste versie van POV-Ray downloaden van de officiële website op https://www.povray.org/.

Naast POV-Ray zijn er nog een aantal andere applicaties die .pov-bestanden kunnen openen en bewerken, waaronder:

- BRL-CAD: een open source 3D-modelleringssoftware die .pov-bestanden kan importeren en exporteren
- MeshLab: software voor 3D-meshverwerking die .pov-bestanden kan importeren en exporteren
- Blender: een populaire open-source grafische 3D-software die .pov-bestanden kan importeren en exporteren

Er zijn mogelijk ook andere softwaretoepassingen die .pov-bestanden kunnen openen, dus u kunt een bestandsviewer of conversietool proberen als u een .pov-bestand niet kunt openen met de bovenstaande toepassingen.

## POV-voorbeeld

Hier is bijvoorbeeld een voorbeeld van een .pov-bestand dat een scène met een enkele blauwe cilinder definieert:

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

In dit voorbeeld specificeert het camerablok de positie en oriëntatie van de camera in de scène, het blok 'lichtbron' declareert een lichtbron en specificeert de positie en kleur ervan, en het blok 'cilinder' declareert een cilinderobject en specificeert de eindpunten ervan. straal en materiaaleigenschappen. Wanneer u dit .pov-bestand in de POV-Ray-software opent, wordt er een afbeelding weergegeven van een enkele blauwe cilinder.

## Referenties
 * [POV-Ray - Wikipedia](https://en.wikipedia.org/wiki/POV-Ray)
 * [Documentatie POV-Ray-website](http://www.povray.org/documentation/)

