{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Uzziniet par OSU failu formātu un API, kas var izveidot un atvērt OSU failus.",
  "title" : "OSU fails - Osu! Skripta faila formāts",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-lv",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Kas ir OSU fails?

OSU fails ir spēles skripts, kas rakstīts Os! ritma spēle. Tajā ir informācija par spēlē izmantoto ritmu karti, piemēram, grūtības pakāpi, atskaņojamo dziesmu un trāpījuma objektu laiku, ar kuriem spēlētājam ir jāsinhronizējas ar mūziku. Tas ļauj ritma spēļu spēlētājiem izstrādāt pielāgotus izaicinājumus un dalīties ar spēļu kopienu.

**OSR faila formāta MIME tips:** x-osu-beatmap

## OSU faila formāts

OSU faili tiek saglabāti diskā kā vienkārša teksta faili, un to struktūra ir ļoti skaidri noteikta osu! [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29).

### Sadaļas OSU failā

Tipiskam OSU failam ir šādas sadaļas.

|Sadaļa |Apraksts |Satura veids|
---|---|---|
|[Vispārīgi]| Vispārīga informācija par beatmap| atslēga: vērtību pāri|
|[Redaktors]| Saglabāti Beatmap redaktora iestatījumi| atslēga: vērtību pāri|
|[Metadati] |Informācija, kas tiek izmantota, lai identificētu ritma karti| atslēga:vērtību pāri|
|[Grūtības] |Grūtības iestatījumi| atslēga:vērtību pāri|
|[Notikumi]| Beatmap un storyboard grafikas notikumi| Komatatdalītie saraksti|
|[Laika punkti]| Laika un kontroles punkti| Komatatdalītie saraksti|
|[Krāsas]| Kombinētās un ādas krāsas| atslēga : vērtību pāri|
|[HitObjects]| Sitieni objektos| Komatatdalītie saraksti|

## Atsauces

* [OSU! Ritma spēle](https://osu.ppy.sh/home)

* [OSU faila formāts](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


