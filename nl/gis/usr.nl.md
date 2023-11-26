{
"datum": "03-08-2023",
  "keywords": [
"usr",
"usr-bestand",
"wat is een usr-bestand",
"hoe usr-bestand te openen",
"bestand",
"usr-bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"USR-bestandsindeling - Lowrance GPS-gegevensbestand",
  "description":"Leer meer over het USR-formaat en API's waarmee USR-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
"parent":"gis"
}
},
"laatste mod": "2023-08-03"
}

## Wat is een USR-bestand?

De bestandsextensie ".usr" heeft ook betrekking op GPS-apparaten van Lowrance. In het bijzonder wordt het gebruikt voor het opslaan van GPS-gegevens in een formaat dat bekend staat als "User Data Format" (USR-formaat) en dat wordt gebruikt door GPS-apparaten van Lowrance.

Wanneer u een Lowrance GPS-apparaat gebruikt, kunt u uw waypoints, tracks en routes opslaan als ".usr"-bestanden. Deze bestanden bevatten doorgaans informatie zoals breedtegraad, lengtegraad, hoogte, tijdstempel en andere gegevens met betrekking tot uw GPS-activiteiten.

Hier volgen enkele veelvoorkomende toepassingen van .usr-bestanden met GPS-apparaten van Lowrance:

- **Waypoints:** Waypoints zijn specifieke locaties die op de GPS zijn gemarkeerd, zoals oriëntatiepunten, favoriete visplekken of interessante plaatsen. U kunt deze locaties opslaan als .usr-bestanden en ze kunnen worden geïmporteerd, geëxporteerd of gedeeld met andere Lowrance GPS-gebruikers.

- **Tracks:** Tracks vertegenwoordigen het geregistreerde pad van uw GPS-bewegingen. U kunt uw tracklogs opslaan als .usr-bestanden, zodat u uw routes later kunt bekijken en analyseren of deze met anderen kunt delen.

- **Routes:** Routes zijn vooraf gedefinieerde paden die u kunt maken en opslaan op uw GPS-apparaat. Deze routes kunnen ook worden opgeslagen als .usr-bestanden voor toekomstig gebruik of delen.

Om .usr-bestanden op uw Lowrance GPS-apparaat te beheren, gebruikt u doorgaans software zoals Lowrance's "Insight Planner" of "Lowrance GPS Utility" om uw GPS-gegevens te importeren, exporteren en manipuleren.

## USR-bestandsindeling - Meer informatie

In Lowrance iFinder GPS-apparaten worden de .usr-bestanden gemaakt en opgeslagen op de MultiMediaCard (MMC)-geheugenkaart die in het apparaat is geplaatst. Deze bestanden bevatten gebruikersgegevens zoals waypoints, tracks en routes.

Om de .usr-bestanden van de MMC naar een computer over te brengen, volgt u deze stappen:

- **Verwijder de MMC:** Verwijder voorzichtig de MultiMediaCard (MMC) uit het Lowrance iFinder GPS-apparaat.

- **MMC in de computer plaatsen:** Gebruik een geschikte MMC-kaartlezer om de geheugenkaart in de kaartlezersleuf van uw computer te plaatsen.

- **Zoek .usr-bestanden:** Zodra de MMC door uw computer wordt herkend, zou u toegang moeten hebben tot de bestanden die erop zijn opgeslagen. Zoek naar de .usr-bestanden die uw GPS-gegevens bevatten.

- **Conversie met GPSBabel:** Om de .usr-bestanden naar een ander GPS-formaat te converteren, kunt u GPSBabel gebruiken, een gratis en open source tool voor het werken met verschillende GPS-bestandsformaten. GPSBabel ondersteunt een breed scala aan invoer- en uitvoerformaten, waardoor u de .usr-bestanden kunt converteren naar formaten die compatibel zijn met andere GPS-software of -apparaten.

U kunt GPSBabel downloaden van de officiële website (http://www.gpsbabel.org/) en op uw computer installeren. Eenmaal geïnstalleerd, kunt u de opdrachtregelinterface of de grafische gebruikersinterface van de software (indien beschikbaar) gebruiken om de conversie uit te voeren.

Als u bijvoorbeeld .usr-bestanden naar het GPX-formaat wilt converteren, kunt u een opdracht gebruiken zoals:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

Het bovenstaande commando instrueert GPSBabel om het invoerbestand "input.usr" in Lowrance USR-formaat te lezen en het uitvoerbestand "output.gpx" in GPX-formaat te schrijven.

- **Geconverteerde bestanden importeren/gebruiken:** Na de conversie beschikt u over uw GPS-gegevens in het nieuwe formaat (bijvoorbeeld GPX), dat u kunt gebruiken met andere GPS-software of apparaten die dat formaat ondersteunen.

## Hoe open je een USR-bestand?

Programma's die USR-bestanden openen of ernaar verwijzen, omvatten

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## Referenties
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)

