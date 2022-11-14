{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "extensie", "bestand", "format", "systeem", "LNK-bestand", "link", "LNK-bestanden", "LNK-documenten", "toepassing", "programma's"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Link Bestandsformaat",
  "description":"Meer informatie over LNK-bestandsindeling en API's die LNK-bestanden kunnen maken en openen.",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Wat is een LNK-bestand? ##

Een LNK-bestand, analoog aan een identiteit op het Mac-systeem, is een Windows-alternatief of "link" dat dient als verbinding met een originele afbeeldingsdocumentmap of -programma. Het bevat het type, de positie en de bestandsnaam van de bestemming van de snelkoppeling, evenals de toepassing die het doeldocument opent en een extra sneltoets.

Ga in Windows naar een bestand, map of uitvoerbaar programma en kies Snelkoppeling maken. De locatie van het bestandsformaat en de map "Begin" zijn twee basisfuncties van LNK-bestanden. Het bestandsformaat van LNK-bestanden is gemaskeerd en een gebogen pijl geeft aan dat het snelkoppelingen zijn.

## LNK-bestandsindeling ##

LNK-bestandsindelingen hebben meestal hetzelfde pictogram als hun doelbestanden, maar met de toevoeging van een kleine gekrulde pijl om aan te geven dat het bestand naar een andere locatie wijst. Wanneer op de snelkoppeling wordt gedubbelklikt, gedraagt deze zich alsof de gebruiker op het eigenlijke bestand heeft gedubbelklikt.

LNK-bestanden die toepassingssnelkoppelingen bevatten, kunnen eigenschappen hebben die van invloed zijn op hoe het programma wordt uitgevoerd. Om de kenmerken te wijzigen, klikt u met de rechtermuisknop op het snelkoppelingsbestand en kiest u **Eigenschappen**, en wijzigt u vervolgens het veld Doel.

In plaats van bestandsextensies zijn LNK-bestanden Windows Verkenner-extensies. Als terminalextensie kunnen .lnk-documenten alleen in Windows Verkenner worden gebruikt om een bestand te vervangen, en ze hebben andere doeleinden in Windows Verkenner dan als snelkoppeling naar een lokaal document. Deze bestanden beginnen ook met de letter "L".

Hoewel snelkoppelingen naar specifieke bestanden en mappen verwijzen wanneer ze worden gemaakt, kunnen ze onbruikbaar worden als het doel naar een andere locatie wordt gewijzigd. Explorer begint een snelkoppelingsmap te repareren die naar een dood doel verwijst wanneer deze wordt geopend.


## Technische specificatie ##

Alleen wanneer de "Verberg extensies voor herkende bestandstypen" mapweergave-instelling is uitgeschakeld, toont Windows de .lnk-documentextensie niet voor documentsnelkoppelingen. Hoewel het niet wordt geadviseerd, kunt u de bestandsextensie weergeven door de eigenschap "NeverShowExt" te verwijderen uit het HKEY_CLASSES_ROOT\lnk-bestand Windows-registeritem.

Voer hiervoor de volgende stappen uit:

* Open "Registratie-editor" door "Regedit" in het zoekveld van de taakbalk in te voeren en het programma te kiezen
* Navigeer in de applicatie naar de locatie Computer\HKEY HKEY_CLASSES_ROOT\lnkfile
* Maak een back-up van het item door er met de rechtermuisknop op te klikken en Exporteren te kiezen
* Selecteer en verwijder het kenmerk "NeverShowExt"
* Windows moet opnieuw worden opgestart


## Referentie ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
