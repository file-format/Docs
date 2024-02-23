{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lär dig om OSU-filformat och API:er som kan skapa och öppna OSU-filer.",
  "title" : "OSU-fil - Osu! Skriptfilformat",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Vad är OSU fil?

En OSU-fil är ett spelskript skrivet för OSU! rytm spel. Den innehåller information om en beatmap som används i spelet, till exempel svårighetsgraden, låten som ska spelas och tidpunkterna för de träffade objekten som spelaren måste synkronisera med musiken. Det låter rytmspelsspelare utveckla anpassade utmaningar och dela med spelgemenskapen.

**MIME-typ av OSR-filformat:** x-osu-beatmap

## OSU filformat

OSU-filer sparas som vanliga textfiler på skiva och dess struktur är mycket tydligt definierad i [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) av osu!.

### Avsnitt i OSU-fil

En typisk OSU-fil har följande avsnitt.

|Avsnitt |Beskrivning |Innehållstyp|
---|---|---|
|[Allmänt]| Allmän information om beatmap| nyckel: värdepar|
|[Redaktör]| Sparade inställningar för beatmap-redigeraren| nyckel: värdepar|
|[Metadata] |Information som används för att identifiera beatmapen| nyckel:värdepa-svr|
|[Svårighet] |Svårighetsinställningar| nyckel:värdepar|
|[Händelser]| Beatmap och storyboard grafiska händelser| Kommaseparerade listor|
|[TimingPoints]| Timing och kontrollpunkter| Kommaseparerade listor|
|[Färger]| Combo och hudfärger| nyckel : värdepar|
|[HitObjects]| Hit objekt| Kommaseparerade listor|

## Referenser

* [OSU! Rhythm Game](https://osu.ppy.sh/home)

* [OSU-filformat](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


