{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over de OSR-bestandsindeling en API's waarmee OSR-bestanden kunnen worden gemaakt en geopend.",
  "title" : "OSR-bestand - osu! Bestandsformaat opnieuw afspelen",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-nl",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Wat is een OSR-bestand?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**MIME-type OSR-bestandsindeling:** x-osu-replay

## OSR-bestandsindeling

OSR-bestanden worden opgeslagen als binaire bestanden met gegevensvelden met zowel vaste als variabele lengte.

|Gegevenstype| Formaat|
---|---|
|Byte |Spelmodus van de herhaling (0 = osu! Standaard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Geheel getal |Versie van het spel toen de herhaling werd gemaakt (bijvoorbeeld 20131216)|
|String |osu! beatmap MD5-hash|
|String| Spelernaam|
|String| osu! replay MD5-hash (bevat bepaalde eigenschappen van de replay)|
|Kort| Aantal 300's|
|Kort| Aantal 100's in standaard, 150's in Taiko, 100's in CTB, 100's in manie|
|Kort| Aantal 50's in standaard, kleinfruit in CTB, 50's in manie|
|Kort| Aantal Gekis in standaard, Max 300s in manie|
|Kort| Aantal Katu's in standaard, 200s in manie|
|Kort| Aantal missers|
|Geheel getal| Totale score weergegeven op het scorerapport|
|Kort| Beste combo weergegeven op het scorerapport|
|Byte| Perfecte/volledige combo (1 = geen missers en geen sliderpauzes en geen vroegtijdig voltooide sliders)|
|Geheel getal| Mods gebruikt. Zie hieronder voor een lijst met mod-waarden.|
|String| Levensbalkgrafiek: door komma's gescheiden paren u/v, waarbij u de tijd in milliseconden in het nummer is en v een drijvende-kommawaarde van 0 - 1 is die de hoeveelheid leven vertegenwoordigt die u op een bepaald moment heeft (0 = levensbalk is leeg, 1= levensbalk is vol)|
|Lang| Tijdstempel (Windows-tikjes)|
|Geheel getal| Lengte in bytes van gecomprimeerde herhalingsgegevens|
|Byte |Array Gecomprimeerde herhalingsgegevens|
|Lang| Onlinescore-ID|
|Dubbel| Aanvullende mod-informatie. Alleen aanwezig als Target Practice is ingeschakeld.|

## Referenties

* [OSU! Ritmespel](https://osu.ppy.sh/home)

* [OSR-bestandsindeling](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


