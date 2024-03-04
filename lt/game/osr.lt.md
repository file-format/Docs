{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Sužinokite apie OSR failo formatą ir API, kurios gali kurti ir atidaryti OSR failus.",
  "title" : "OSR failas – osu! Pakartotinis failo formatas",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-lt",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Kas yra OSR failas?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

** MIME tipas OSR failo formatas:** x-osu-replay

## OSR failo formatas

OSR failai išsaugomi kaip dvejetainiai failai su fiksuoto ir kintamo ilgio duomenų laukais.

|Duomenų tipas| Formatas|
---|---|
|Baitas |Pakartojimo žaidimo režimas (0 = osu! Standartinis, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Sveikasis skaičius |Žaidimo versija, kai buvo sukurtas pakartojimas (pvz., 20131216)|
|Styga |osu! beatmap MD5 maiša|
|Styga| Žaidėjo vardas|
|Styga| osu! pakartokite MD5 maišą (apima tam tikras pakartojimo savybes)|
|Trumpas| Skaičius 300s|
|Trumpas| Skaičius 100s standartinėje, 150s Taiko, 100s CTB, 100s manija|
|Trumpas| Skaičius 50s standartinėje, smulkūs vaisiai CTB, 50s manijos atveju|
|Trumpas| Gekių skaičius standartinėje, Max 300s manijoje|
|Trumpas| Katus skaičius standarte, 200 manijos|
|Trumpas| Praleidimų skaičius|
|Sveikasis skaičius| Bendras balas rodomas balų ataskaitoje|
|Trumpas| Geriausias derinys, rodomas balų ataskaitoje|
|Baitas| Tobulas / pilnas derinys (1 = nėra praleistų, be slankiklio pertraukų ir be anksti užbaigtų slankiklių)|
|Sveikasis skaičius| Naudoti modifikacijos. Mod verčių sąrašą žr. toliau.|
|Styga| Gyvenimo juostos diagrama: kableliais atskirtos poros u/v, kur u yra dainos laikas milisekundėmis, o v yra slankiojo kablelio reikšmė nuo 0 iki 1, nurodanti gyvenimo trukmę nurodytu laiku (0 = gyvenimo juosta yra tuščia, 1= gyvybės juosta pilna)|
|Ilgas| Laiko žyma (Windows pažymima)|
|Sveikasis skaičius| Suspaustų atkūrimo duomenų ilgis baitais|
|Baitas |Masyvas Suspausti pakartojimo duomenys|
|Ilgas| Interneto balo ID|
|Dvigubas| Papildoma mod informacija. Rodoma tik tada, jei įjungta Target Practice.|

## Nuorodos

* [OSU! Ritmo žaidimas](https://osu.ppy.sh/home)

* [OSR failo formatas](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


