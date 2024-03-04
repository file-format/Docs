{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Sužinokite apie OSU failo formatą ir API, kurios gali kurti ir atidaryti OSU failus.",
  "title" : "OSU failas – Osu! Scenarijaus failo formatas",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-lt",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Kas yra OSU failas?

OSU failas yra žaidimo scenarijus, parašytas osu! ritmo žaidimas. Jame pateikiama informacija apie žaidime naudojamą ritmo schemą, pvz., sudėtingumo lygį, grojamą dainą ir pataikymų objektų, su kuriais žaidėjas turi sinchronizuoti su muzika, laiką. Tai leidžia ritmo žaidimų žaidėjams kurti pasirinktinius iššūkius ir dalytis jais su žaidimų bendruomene.

** MIME tipas OSR failo formatas:** x-osu-beatmap

## OSU failo formatas

OSU failai išsaugomi kaip paprasto teksto failai diske, o jų struktūra labai aiškiai apibrėžta osu! [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29).

### Skiltys OSU faile

Įprastas OSU failas turi šiuos skyrius.

|Skyrius |Aprašymas |Turinio tipas|
---|---|---|
|[Bendra]| Bendra informacija apie beatmap| raktas: verčių poros|
|[Redaktorius]| Išsaugoti beatmap redaktoriaus nustatymai| raktas: verčių poros|
|[Metaduomenys] |Informacija, naudojama identifikuoti beatmap| raktas:reikšmių poros|
|[Sunkumas] |Sunkumo nustatymai| raktas:reikšmių poros|
|[Įvykiai]| Beatmap ir storyboard grafiniai įvykiai| Kableliais atskirti sąrašai|
|[Laiko taškai]| Laiko ir kontrolės taškai| Kableliais atskirti sąrašai|
|[Spalvos]| Derinys ir odos spalvos| raktas : verčių poros|
|[HitObjects]| Pataikė į objektus| Kableliais atskirti sąrašai|

## Nuorodos

* [OSU! Ritmo žaidimas](https://osu.ppy.sh/home)

* [OSU failo formatas](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


