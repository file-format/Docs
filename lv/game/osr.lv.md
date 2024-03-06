{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Uzziniet par OSR faila formātu un API, kas var izveidot un atvērt OSR failus.",
  "title" : "OSR fails - osu! Atkārtot faila formātu",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-lv",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Kas ir OSR fails?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**OSR faila formāta MIME tips:** x-osu-replay

## OSR faila formāts

OSR faili tiek saglabāti kā bināri faili ar fiksēta, kā arī mainīga garuma datu laukiem.

|Datu tips| Formāts|
---|---|
|Baits |Atkārtojuma spēles režīms (0 = osu! Standarta, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mānija)|
|Integer |Spēles versija, kad tika izveidots atkārtojums (piem., 20131216)|
|String |osu! beatmap MD5 hash|
|String| Spēlētāja vārds|
|String| osu! replay MD5 hash (ietver noteiktas atkārtojuma īpašības)|
|Īss| Skaits 300s|
|Īss| 100s skaits standarta, 150s Taiko, 100s CTB, 100s mānijas gadījumā|
|Īss| Skaits 50s standarta, mazs auglis CTB, 50s mānijai|
|Īss| Geki skaits standartā, Max 300s mānijai|
|Īss| Katus skaits standartā, 200s mānijai|
|Īss| Netrāpījumu skaits|
|Vesels skaitlis| Kopējais punktu skaits, kas parādīts rezultātu pārskatā|
|Īss| Labākā kombinācija, kas parādīta rezultātu pārskatā|
|Baits| Ideāla/pilna kombinācija (1 = bez garām un bez slīdņa pārtraukumiem un bez agri pabeigtiem slīdņiem)|
|Vesels skaitlis| Izmantotie modi. Skatiet zemāk mod vērtību sarakstu.|
|String| Dzīves joslas diagramma: ar komatu atdalīti pāri u/v, kur u ir dziesmas laiks milisekundēs un v ir peldošā komata vērtība no 0 līdz 1, kas atspoguļo jūsu dzīves ilgumu konkrētajā laikā (0 = dzīves josla ir tukša, 1= dzīves josla ir pilna)|
|Ilgu| Laika zīmogs (Windows atzīmē)|
|Vesels skaitlis| Saspiesto atkārtošanas datu garums baitos|
|Baits |Masīvs Saspiestie atkārtošanas dati|
|Ilgu| Tiešsaistes rezultāta ID|
|Dubultā| Papildu informācija par moduļiem. Parādās tikai tad, ja ir iespējota Target Practice.|

## Atsauces

* [OSU! Ritma spēle](https://osu.ppy.sh/home)

* [OSR faila formāts](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


