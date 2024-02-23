{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over de OSU-bestandsindeling en API's waarmee OSU-bestanden kunnen worden gemaakt en geopend.",
  "title" : "OSU-bestand - Osu! Scriptbestandsformaat",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-nl",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Wat is een OSU-bestand?

Een OSU-bestand is een spelscript geschreven voor osu! ritme spel. Het bevat informatie over een beatmap die in het spel wordt gebruikt, zoals de moeilijkheidsgraad, het nummer dat moet worden gespeeld en de timing van de hitobjecten waarmee de speler met de muziek moet synchroniseren. Hiermee kunnen ritmespelers aangepaste uitdagingen ontwikkelen en delen met de gamegemeenschap.

**MIME-type OSR-bestandsindeling:** x-osu-beatmap

## OSU-bestandsindeling

OSU-bestanden worden als gewone tekstbestanden op schijf opgeslagen en de structuur ervan wordt heel duidelijk gedefinieerd in de [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) door osu!.

### Secties in OSU-bestand

Een typisch OSU-bestand heeft de volgende secties.

|Sectie |Beschrijving |Inhoudstype|
---|---|---|
|[Algemeen]| Algemene informatie over de beatmap| sleutel: waardeparen|
|[Redacteur]| Opgeslagen instellingen voor de beatmap-editor| sleutel: waardeparen|
|[Metadata] |Informatie gebruikt om de beatmap te identificeren| sleutel:waardeparen|
|[Moeilijkheidsgraad] |Instellingen voor moeilijkheidsgraad| sleutel:waardeparen|
|[Gebeurtenissen]| Beatmap en storyboard grafische evenementen| Door komma's gescheiden lijsten|
|[Tijdpunten]| Timing en controlepunten| Door komma's gescheiden lijsten|
|[Kleuren]| Combo en huidskleuren| sleutel: waardeparen|
|[HitObjects]| Raak objecten| Door komma's gescheiden lijsten|

## Referenties

* [OSU! Ritmespel](https://osu.ppy.sh/home)

* [OSU-bestandsindeling](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


