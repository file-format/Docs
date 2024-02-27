{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lær om OSU-filformat og API'er, der kan oprette og åbne OSU-filer.",
  "title" : "OSU-fil - Osu! Script filformat",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-da",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Hvad er OSU fil?

En OSU-fil er et spilscript skrevet til osu! rytme spil. Den indeholder information om et beatmap, der bruges i spillet, såsom sværhedsgraden, den sang, der skal spilles, og timingen af de hitobjekter, som spilleren skal synkronisere med musikken. Det lader rytmespillere udvikle tilpassede udfordringer og dele med spilfællesskabet.

**MIME-type af OSR-filformat:** x-osu-beatmap

## OSU filformat

OSU-filer gemmes som almindelige tekstfiler på disken, og dens struktur er meget klart defineret i [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) af osu!.

### Sektioner i OSU-fil

En typisk OSU-fil har følgende sektioner.

|Sektion |Beskrivelse |Indholdstype|
---|---|---|
|[Generelt]| Generel information om beatmap| nøgle: værdipar|
|[Redaktør]| Gemte indstillinger for beatmap-editoren| nøgle: værdipar|
|[Metadata] |Oplysninger brugt til at identificere beatmap| nøgle:værdipar|
|[Sværhedsgrad] |Sværhedsgradsindstillinger| nøgle:værdipar|
|[Begivenheder]| Beatmap og storyboard grafiske begivenheder| Kommaseparerede lister|
|[TimingPoints]| Timing og kontrolpunkter| Kommaseparerede lister|
|[Farver]| Combo og hudfarver| nøgle : værdipar|
|[HitObjects]| Hit objekter| Kommaseparerede lister|

## Referencer

* [OSU! Rhythm Game](https://osu.ppy.sh/home)

* [OSU-filformat](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


