{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Přečtěte si o formátu souboru OSU a rozhraních API, která mohou vytvářet a otevírat soubory OSU.",
  "title" : "Soubor OSU - Osu! Formát souboru skriptu",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-cs",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Co je soubor OSU?

Soubor OSU je herní skript napsaný pro osu! rytmická hra. Obsahuje informace o beatmap používaném ve hře, jako je úroveň obtížnosti, skladba, která se má hrát, a načasování zasažených objektů, se kterými se hráč musí synchronizovat s hudbou. Umožňuje hráčům rytmických her vyvíjet vlastní výzvy a sdílet je s herní komunitou.

**MIME Typ souboru OSR Formát:** x-osu-beatmap

## Formát souboru OSU

Soubory OSU jsou uloženy jako soubory ve formátu prostého textu na disk a jejich struktura je velmi jasně definována v [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) od osu!.

### Sekce v souboru OSU

Typický soubor OSU má následující sekce.

|Sekce |Popis |Typ obsahu|
---|---|---|
|[Obecné]| Obecné informace o beatmap| klíč: páry hodnot|
|[Editor]| Uložená nastavení editoru beatmap| klíč: páry hodnot|
|[Metadata] |Informace použité k identifikaci beatmap| klíč:páry hodnot|
|[Obtížnost] |Nastavení obtížnosti| klíč:páry hodnot|
|[Události]| Beatmap a grafické události scénáře| Čárkami oddělené seznamy|
|[Časové body]| Časové a kontrolní body| Čárkami oddělené seznamy|
|[Barvy]| Kombinace a barvy pleti| klíč : páry hodnot|
|[HitObjects]| Zasahovat objekty| Čárkami oddělené seznamy|

## Reference

* [OSU! Rytmická hra](https://osu.ppy.sh/home)

* [formát souboru OSU](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


