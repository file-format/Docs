{
"datum": "2023-02-02",
  "keywords": [
"app-bestand",
"wat is een app-bestand",
"bestand",
"hoe app-bestand openen",
"app-bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
  "description":"Leer meer over de APP-bestandsindeling en API's die APP-bestanden kunnen maken en openen.",
"title":"APP-bestandsindeling - macOS-applicatiebundel",
"linktitel": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app",
"parent":"uitvoerbaar"
}
},
"laatste mod": "2023-02-02"
}

## Wat is een APP-bestand?

Een .app-bestand op macOS is een speciaal type map dat alle bestanden bevat die nodig zijn om een specifieke applicatie uit te voeren, inclusief de uitvoerbare code, bronnen en metagegevens. De .app-extensie geeft aan het besturingssysteem door dat deze map als één geheel moet worden behandeld, in plaats van als een verzameling afzonderlijke bestanden, en dat deze rechtstreeks vanuit de Finder of het Dock kan worden gestart.

Finder is de standaard applicatie voor bestandsbeheer op macOS. Hiermee kunt u door de bestanden en mappen op uw computer bladeren en deze ordenen. Het Dock is een functie van macOS die snelle toegang biedt tot veelgebruikte applicaties en documenten. Met zowel Finder als het Dock kunt u applicaties starten door op hun .app-bestanden te klikken, waardoor de bijbehorende applicatiebundel wordt geopend. Wanneer u een applicatie start, wordt de uitvoerbare code binnen de .app-bundel uitgevoerd, waardoor de applicatie beschikbaar wordt voor gebruik. Het .app-bestand is de representatie van de applicatie op het bestandssysteem en biedt de gebruiker een manier om toegang te krijgen tot de applicatie en deze te starten.

Wanneer u met de rechtermuisknop op een .app-bestand in Finder op een macOS-systeem klikt en "Toon pakketinhoud" selecteert, kunt u de interne structuur van de applicatiebundel zien. Dit is handig als u toegang wilt krijgen tot bronnen of bestanden die door de toepassing worden gebruikt, of als u de inhoud van de toepassing wilt inspecteren om problemen op te lossen. De pakketinhoud van een .app-bestand omvat doorgaans mappen voor bronnen zoals afbeeldingen en geluiden, evenals de uitvoerbare code voor de toepassing. Door de inhoud van een .app-bestand te verkennen, kunt u dieper inzicht krijgen in hoe de applicatie in elkaar zit en wat deze doet.

## Hoe APP-bestand openen?

Om een .app-bestand op macOS te openen, dubbelklikt u eenvoudig op het bestand in Finder. Hierdoor wordt de applicatie in de .app-bundel gestart. Als de applicatie op uw systeem is geïnstalleerd en is gekoppeld aan het .app-bestandstype, zou dubbelklikken op het bestand de applicatie automatisch moeten starten. Als de applicatie niet is gekoppeld aan het .app-bestandstype, moet u mogelijk met de rechtermuisknop op het bestand klikken en 'Openen met' selecteren om een geschikte applicatie te kiezen om het mee te openen.

U kunt een .app-bestand openen op de terminal in macOS met behulp van de opdracht "open". Om dit te doen, navigeert u naar de map waar het .app-bestand zich bevindt met behulp van de opdracht "cd" en voert u vervolgens de volgende opdracht uit:

```
open <AppName>.app 
```

waar<AppName> is de naam van de toepassing die u wilt starten. Hierdoor wordt de toepassing gestart alsof u erop hebt gedubbelklikt in Finder. De opdracht "open" is een hulpprogramma voor algemene doeleinden dat kan worden gebruikt om veel verschillende soorten bestanden te openen, waaronder toepassingen, documenten en mappen. Wanneer u de opdracht "open" gebruikt voor een .app-bestand, wordt de applicatie in de bundel gestart.

## Referenties
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
