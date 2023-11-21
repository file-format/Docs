{
"date":"2023-01-04",
   "keywords":[
"cs",
"cs-bestand",
"cs cleo aangepast script",
"hoe een cs-bestand te openen",
"bestand",
"cs bestandsextensie",
"verlenging",
"bestand"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"CS-bestandsindeling - CLEO aangepast script",
   "description":"Leer meer over het CS CLEO Custom Script-formaat en API's waarmee CS-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"CS CLEO",
   "menu":{
      "docs":{
         "identifier":"game-cs-cleo",
"parent":"spel"
}
},
"lastmod":"2023-01-04"
}

## Wat is een CS-bestand?

Een .CS-bestand in de context van CLEO (afkorting van CLEO Library) verwijst doorgaans naar een aangepast scriptbestand dat wordt gebruikt in de Grand Theft Auto (GTA)-serie videogames. CLEO is een populair modding-framework waarmee spelers aangepaste scripts kunnen maken en toevoegen aan GTA-games, waardoor ze de gameplay kunnen aanpassen, nieuwe functies kunnen toevoegen en de algehele game-ervaring kunnen verbeteren.

## Overzicht van CS-bestand

Hier is een basisoverzicht van wat een .cs-bestand in CLEO kan bevatten:

1. **Scriptcode**: een .cs-bestand bevat scriptcode geschreven in CLEO-scripttaal. Deze scripttaal is specifiek voor CLEO en wordt gebruikt om het gedrag van aangepaste scripts in het spel te definiëren. De code kan worden geschreven met behulp van een teksteditor en volgt doorgaans een specifieke syntaxis.
    









2. **Aanpassingen**: CLEO-scripts kunnen verschillende wijzigingen in het spel aanbrengen, zoals het veranderen van het gedrag van in-game-objecten, het maken van aangepaste missies, het toevoegen van nieuwe voertuigen, wapens en meer. De mogelijkheden zijn uitgebreid en afhankelijk van de creativiteit en programmeervaardigheden van de scriptauteur.
    









3. **Triggers**: CLEO-scripts bevatten vaak triggers die bepalen wanneer en hoe een aangepast script moet worden uitgevoerd. Deze triggers kunnen gebaseerd zijn op in-game gebeurtenissen, spelersacties of specifieke omstandigheden.
    









4. **Variabelen en functies**: CLEO-scripts kunnen variabelen gebruiken om gegevens op te slaan en te manipuleren, evenals functies om code in te kapselen en opnieuw te gebruiken. Deze variabelen en functies worden gebruikt om het gedrag van het script te controleren.

## Voorbeeld van CS-bestand

Hier is een eenvoudig voorbeeld van een CLEO .cs-script dat het weer in het spel verandert:

```
{$CLEO .cs}

03A4: name_thread 'WEATHER'

:WEATHER_LOOP
    // Change the weather to sunny
    0085: 0@ = 11 // Weather ID for sunny weather
    00D8: mission_cleanup
    0051: return 0@ // Exit the script

// Add more code and conditions as needed
```

## CLEO-bibliotheek

De **CLEO-bibliotheek**, vaak eenvoudigweg "CLEO" genoemd, is een populair en krachtig modding-framework voor de Grand Theft Auto (GTA)-serie videogames. Hiermee kunnen spelers en modders aangepaste scripts maken en toevoegen aan GTA-games, waardoor ze de gameplay kunnen aanpassen, nieuwe functies kunnen toevoegen en de algehele game-ervaring kunnen verbeteren. CLEO staat vooral bekend om zijn flexibiliteit en gebruiksgemak in de GTA-moddinggemeenschap.

Hier zijn enkele belangrijke kenmerken en aspecten van de CLEO-bibliotheek:

1. **Scripttaal**: CLEO introduceert zijn scripttaal, die specifiek is voor het modding-framework. De scripttaal is ontworpen om relatief eenvoudig te begrijpen en te gebruiken, waardoor deze toegankelijk is voor zowel beginnende als ervaren modders.
    









2. **Aangepaste scripts**: Met CLEO kunt u aangepaste scripts maken die een breed scala aan functies binnen de gamewereld kunnen uitvoeren. Deze scripts kunnen het gedrag in de game veranderen, nieuwe missies toevoegen, nieuwe voertuigen of wapens introduceren, de spelfysica veranderen en nog veel meer.
    









3. **Triggers en gebeurtenissen**: CLEO-scripts kunnen worden geactiveerd door verschillende in-game evenementen, spelersacties of specifieke omstandigheden. Hierdoor kunnen modders dynamische en interactieve inhoud in de game creëren.
    









4. **Ondersteuning voor meerdere GTA-versies**: CLEO heeft versies die zijn afgestemd op verschillende GTA-games, waaronder GTA III, GTA Vice City, GTA San Andreas, GTA IV en andere. Dit betekent dat modders hun aangepaste scripts voor verschillende GTA-titels kunnen maken en delen.

## Bestandsformaten gebruikt door CLEO-bibliotheek

Bij CLEO-modding voor Grand Theft Auto (GTA)-games worden vaak verschillende bestandsindelingen gebruikt om mods te maken en te installeren. Deze bestandsformaten dienen verschillende doeleinden, van het bevatten van daadwerkelijke scripts tot het opslaan van extra bronnen zoals texturen, modellen of audio. Hier zijn enkele van de belangrijkste bestandsformaten die worden gebruikt bij CLEO-modding:

1. **.cs (aangepast script)**: CLEO .cs-bestanden zijn aangepaste scriptbestanden geschreven in CLEO-scripttaal. Deze bestanden bevatten code die het gedrag en de functionaliteit van mod definieert. .cs-bestanden vormen de kern van CLEO-modding en worden per game uitgevoerd om aangepaste functies te implementeren.
    









2. **.csa (aangepast scriptarchief)**: .csa-bestanden zijn archieven waarin meerdere .cs-scriptbestanden kunnen worden opgeslagen. Ze worden vaak gebruikt om gerelateerde scripts samen te verpakken voor eenvoudiger installatie en beheer.
    









3. **.fxt (tekstbestanden)**: .fxt-bestanden zijn tekstbestanden die kunnen worden gebruikt om tekstvertalingen voor CLEO-mods te lokaliseren of te leveren. Ze bevatten tekstreeksen die in het spel kunnen worden weergegeven, waardoor mods toegankelijk zijn voor spelers in verschillende talen.
    









4. **[.bmp](/nl/image/bmp/), [.png](/nl/image/png/), [.jpg](/nl/image/jpeg/) (Afbeeldingsformaten)**: Deze afbeeldingsformaten zijn gebruikt om texturen en afbeeldingen voor mods op te slaan. Ze kunnen worden gebruikt voor aangepaste skins, voertuigtexturen, HUD-elementen en meer. Afhankelijk van het spel kunnen verschillende beeldformaten de voorkeur hebben.

## Hoe open je een CS-bestand?

Om de inhoud van een CLEO .cs-bestand (aangepast script) te openen en te bekijken, kunt u een teksteditor of code-editor naar keuze gebruiken. Veel voorkomende keuzes zijn onder meer:

- **Kladblok**: een eenvoudige teksteditor die vooraf is geïnstalleerd bij Windows.
- **Kladblok++**: een teksteditor met meer functies, ontworpen voor codering en scripting.
- **Visual Studio Code**: een populaire, gratis en zeer uitbreidbare code-editor.
- **Sublieme tekst**: nog een code-editor die bekend staat om zijn snelheid en veelzijdigheid.
- **Atom**: een open-source code-editor ontwikkeld door GitHub.

## Andere CS-bestanden

Hier volgen andere bestandstypen die de bestandsextensie **.cs** gebruiken.

**Gegevensbestanden en spel**
- [CS - ColorSchemer Studio-kleurenschema](/nl/data/cs-colorschemer/)
- [CS - CLEO aangepast script](/nl/game/cs-cleo/)

**Programmeren**
- [CS - CSharp-codebestand] (/nl/programmering/cs/)

## Referenties
* [CLEO-bibliotheek](https://cleo.li/)

