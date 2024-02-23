{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"GCODE-bestand - Wat is een .gcode-bestand en hoe opent u het?",
   "description":"Meer informatie over de GCODE-bestandsindeling en API's waarmee GCODE-bestanden kunnen worden gemaakt en geopend.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-nl",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Wat is een GCODE-bestand?

Een **GCODE-bestand** is een tekstbestand dat instructies bevat voor het besturen van geautomatiseerde werktuigmachines en 3D-printers; G-code, of 'geometrische code', is een taal die wordt gebruikt om bewegingen en acties van **CNC (Computer Numerical Control)**-machines te besturen; Onder CNC-machines vallen freesmachines, draaibanken, bovenfrezen en 3D-printers.

G-code-opdrachten zijn geschreven in een specifieke syntaxis, meestal bestaande uit letters en cijfers; elk commando instrueert de machine om specifieke actie uit te voeren, zoals het verplaatsen van gereedschap naar een bepaalde positie, het wisselen van gereedschap of het aanpassen van de snelheid.

G-code wordt vaak gegenereerd door **CAM-software (Computer-Aided Manufacturing)**; CAM-software neemt een 3D-model of 2D-ontwerp en genereert bijbehorende toolpaths en G-code-instructies; het G-codebestand wordt vervolgens voor uitvoering in de CNC-machine of 3D-printer geladen.

G-code-bestanden hebben doorgaans de bestandsextensie .nc of .gcode, bijvoorbeeld program.nc of print.gcode.

## GCODE-bestandsstructuur:

GCODE-bestanden zijn platte tekstbestanden waarbij elke regel een specifieke opdracht bevat; deze opdrachten variëren van het besturen van de beweging van de machine tot het aanpassen van de temperatuur, snelheid en andere parameters die cruciaal zijn voor de fabricage van een object.

De syntaxis van GCODE omvat een combinatie van letters en cijfers; elk vertegenwoordigt een afzonderlijke actie of parameter; gebruikelijke commando's zijn onder meer G0 en G1 voor beweging, M3 en M5 voor spilbesturing, en S en F voor respectievelijk snelheids- en voedingssnelheidaanpassingen.

## GCODE-generatie:

Slicing-software zoals **Simplify3D** en **Slic3r** vertaalt CAD-tekeningen (Computer-Aided Design) naar GCODE; CAD-software wordt gebruikt om 3D-modellen te maken, die vervolgens worden geëxporteerd in formaten zoals STL; de slicingsoftware gebruikt deze modellen en genereert een GCODE-bestand met details zoals laaghoogte, afdruksnelheid en temperatuurinstellingen.

## GCODE-voorbeeld

Hier is een eenvoudig voorbeeld van G-code voor het verplaatsen van een CNC-machine:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Hoe open je een GCODE-bestand?

Om een G-codebestand te openen, kunt u afhankelijk van uw behoeften verschillende soorten software gebruiken.

Als u G-code voor de 3D-printer hebt gegenereerd; u kunt het openen met software die bij uw 3D-printer is geleverd of met speciale slicingsoftware; voorbeelden hiervan zijn **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** of **Repetier-Host**; deze programma's hebben vaak een gebruiksvriendelijke interface waarmee u G-code kunt laden en visualiseren.

GCODE-bestanden zijn platte tekst, dus u kunt ze met elke teksteditor openen; Veelgebruikte teksteditors zijn **Kladblok (op Windows)**, **TextEdit (op macOS)** of **Gedit (op Linux)**; klik gewoon **met de rechtermuisknop** op het G-codebestand, kies **Openen met,** en selecteer een teksteditor.

