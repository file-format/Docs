{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Opi OSR-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OSR-tiedostoja.",
  "title" : "OSR-tiedosto - osu! Toista tiedostomuoto",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-fi",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Mikä on OSR-tiedosto?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**OSR-tiedostomuodon MIME-tyyppi:** x-osu-replay

## OSR-tiedostomuoto

OSR-tiedostot tallennetaan binääritiedostoina, joissa on sekä kiinteitä että muuttuvapituisia tietokenttiä.

|Tietotyyppi| Muoto|
---|---|
|Tavu |Uudelleentoiston pelitila (0 = osu! Vakio, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Kokonaisluku |Pelin versio, kun uusinta luotiin (esim. 20131216)|
|Jou |osu! beatmap MD5 hash|
|merkkijono| Pelaajan nimi|
|merkkijono| osu! toista MD5 hash (sisältää tietyt toiston ominaisuudet)|
|Lyhyt| Luku 300s|
|Lyhyt| Lukumäärä 100s vakiossa, 150s Taikossa, 100s CTB:ssä, 100s maniassa|
|Lyhyt| Normaalissa 50s, pienet hedelmät CTB:ssä, 50s maniassa|
|Lyhyt| Gekien määrä vakiona, max 300s maniassa|
|Lyhyt| Katusten määrä vakiona, 200s maniassa|
|Lyhyt| Poissaolojen määrä|
|Kokonaisluku| Pisteraportissa näkyvä kokonaispistemäärä|
|Lyhyt| Paras tulosraportissa näkyvä yhdistelmä|
|tavu| Täydellinen/täysi-yhdistelmä (1 = ei väliin jää, ei liukusäätimen katkoksia eikä aikaisin valmiita liukusäätimiä)|
|Kokonaisluku| Modit käytetty. Katso alta luettelo mod-arvoista.|
|merkkijono| Elämän pylväsdiagrammi: pilkuilla erotetut parit u/v, jossa u on kappaleeseen kulunut aika millisekunteina ja v on liukuluku arvo välillä 0 - 1, joka edustaa eliniän määrää tiettynä ajankohtana (0 = elämäpalkki on tyhjä, 1= elämänpalkki on täynnä)|
|Pitkä| Aikaleima (Windows rastittaa)|
|Kokonaisluku| Pakatun toistodatan pituus tavuina|
|Tavu |Matriisi Pakatut toistotiedot|
|Pitkä| Online Score ID|
|Kaksinkertainen| Lisätiedot mod. Esiintyy vain, jos Target Practice on käytössä.|

## Viitteet

* [OSU! Rytmipeli](https://osu.ppy.sh/home)

* [OSR-tiedostomuoto](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


