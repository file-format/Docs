{
"date":"2023-10-18",
   "keywords":[
"cpi",
"cpi-bestand",
"cpi-codepagina-informatiebestand",
"hoe open ik een cpi-bestand",
"bestand",
"cpi bestandsextensie",
"verlenging",
"bestand"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"CPI-bestandsindeling - Codepagina-informatiebestand",
   "description":"Meer informatie over de CPI Codepage Information-bestandsindeling en API's waarmee CPI-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"CPI",
   "menu":{
      "docs":{
         "identifier":"system-cpi",
"parent":"systeem"
}
},
"lastmod":"2023-10-18"
}

## Wat is een CPI-bestand?

Een `.cpi`-bestand is, in de context van Microsoft Windows- en DOS-besturingssystemen, doorgaans **"Code Page Information File."** Deze bestanden bevatten informatie over codepagina's die worden gebruikt voor tekstcodering en tekensettoewijzingen. Codepagina's zijn essentieel voor het weergeven en verwerken van tekst in verschillende talen en tekensets.

In de context van Windows en DOS worden codepagina's gebruikt om te definiëren hoe tekens worden weergegeven en gecodeerd in verschillende talen en regio's. Deze codepagina's bepalen hoe tekens in het geheugen worden opgeslagen en op het scherm worden weergegeven. Elke codepagina heeft een unieke identificatie en `.cpi`-bestanden slaan informatie op over deze codepagina's, inclusief details zoals karaktertoewijzingen en lettertype-informatie.

`.cpi`-bestanden worden vaak aangetroffen in Windows- of DOS-systeemmappen en spelen een cruciale rol bij het mogelijk maken dat het besturingssysteem tekst correct weergeeft voor verschillende landinstellingen en tekensets. Ze helpen het systeem te begrijpen hoe tekens uit verschillende talen en coderingen moeten worden geïnterpreteerd en weergegeven.

## Codepagina-informatiebestanden

Laten we codepagina-informatiebestanden (.cpi) eens nader bekijken en hoe ze functioneren binnen het raamwerk van MS-DOS en eerdere versies van Microsoft Windows:

1. **Tekencodering en codepagina's**: Codepagina's zijn een cruciaal onderdeel van de manier waarop tekst wordt gecodeerd en weergegeven op de computer. Ze definiëren tekencodering voor een specifieke taal of tekenset. Elke codepagina kent numerieke waarden (codepunten) toe aan tekens, waardoor de computer deze kan weergeven en weergeven. Codetabel 437 wordt bijvoorbeeld vaak gebruikt in de Verenigde Staten en West-Europa, terwijl codetabel 850 wordt gebruikt voor Latin-1-codering.
    







2. **Systeeminitialisatie**: Tijdens de systeeminitialisatie (wanneer de computer opstart) lazen MS-DOS en oudere versies van Windows `.cpi`-bestanden om te bepalen welke codepagina's moesten worden ondersteund. Deze informatie was cruciaal voor tekstweergave, toetsenbordinvoer en tekensetconversies.
    







3. **Weergave- en toetsenbordondersteuning**: deze bestanden bieden informatie over hoe tekens op het scherm moeten worden weergegeven en welke tekensets of codepagina's moeten worden ondersteund voor toetsenbordinvoer. Verschillende codepagina's definiëren verschillende tekensets, dus deze bestanden helpen het besturingssysteem te weten hoe het met gebruikersinvoer moet omgaan en tekst correct moet weergeven.
    







4. **Lokalisatie**: `.cpi`-bestanden zijn essentieel voor de lokalisatie van het besturingssysteem. Ze zorgen ervoor dat het systeem zich kan aanpassen aan verschillende talen, regio's en tekensets, waardoor gebruikers over de hele wereld MS-DOS of Windows in hun voorkeurstaal kunnen gebruiken.
    







5. **Meerdere `.cpi`-bestanden**: op computers met meertalige ondersteuning kunt u mogelijk meerdere `.cpi`-bestanden vinden die overeenkomen met verschillende codepagina's. Het systeem kan bijvoorbeeld '437.cpi' hebben voor de Verenigde Staten, '850.cpi' voor Latin-1, '852.cpi' voor Centraal-Europa, enzovoort. Het juiste bestand wordt geladen op basis van de landinstellingen van de gebruiker of de geselecteerde codetabel.
    







6. **Lettertype-informatie**: naast tekentoewijzingen kunnen deze bestanden lettertype-informatie bevatten, waarin wordt aangegeven welke lettertypen voor elke codepagina moeten worden gebruikt. Dit is belangrijk voor het weergeven van tekst in de juiste stijl en grootte.
    







7. **Oude systemen**: `.cpi`-bestanden kwamen vaker voor in oudere versies van MS-DOS en Windows. Moderne Windows-versies (zoals Windows 10 en hoger) gebruiken doorgaans Unicode voor tekstcodering, dat een breed scala aan tekens en talen ondersteunt. Unicode vereenvoudigt tekstverwerking voor meertalige omgevingen en is standaard voor moderne software.

## Hoe open je een CPI-bestand?

Het openen van het .CPI-bestand (Code Page Information) is geen typische gebruikersactie en deze bestanden zijn over het algemeen niet bedoeld om handmatig te worden geopend. Ze worden door het besturingssysteem gebruikt om tekstcodering en tekensets te beheren en de inhoud ervan wordt automatisch door het systeem benaderd en gebruikt.

Als u echter geïnteresseerd bent in het bekijken van de inhoud van het .CPI-bestand voor informatieve doeleinden, kunt u proberen het te openen met een teksteditor of hexadecimale viewer. Hier ziet u hoe u kunt proberen het .CPI-bestand te openen:

1. **Teksteditor**: u kunt een teksteditor zoals Kladblok (op Windows) of een gewone teksteditor op andere besturingssystemen gebruiken om het .CPI-bestand te openen en te bekijken. Houd er rekening mee dat de inhoud van .CPI-bestanden niet bedoeld is om door mensen leesbaar te zijn en dat u mogelijk reeksen tekens tegenkomt die moeilijk te interpreteren zijn.
    







2. **Hexadecimale viewer**: een hexadecimale viewer of hex-editor kan worden gebruikt om de inhoud van het .CPI-bestand in zijn onbewerkte binaire vorm te openen en te inspecteren. Hex-editors bieden een gedetailleerder overzicht van de bestandsgegevens, wat handig kan zijn als u de structuur ervan probeert te begrijpen. Voorbeelden van dergelijke software zijn HxD, Hex Fiend (voor macOS) en 010 Editor.

## Andere CPI-bestanden

Hier volgen andere bestandstypen die de bestandsextensie **.cpi** gebruiken.

**Video systeem**
- [CPI - AVCHD-videoclipinformatie](/nl/video/cpi/)
- [CPI - Codepagina-informatiebestand](/nl/system/cpi/)

## Referenties
* [Codepagina](https://en.wikipedia.org/wiki/Code_page)

