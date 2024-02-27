{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lær om OSR-filformat og API'er, der kan oprette og åbne OSR-filer.",
  "title" : "OSR-fil - osu! Genafspil filformat",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-da",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Hvad er en OSR fil?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**MIME-type af OSR-filformat:** x-osu-replay

## OSR filformat

OSR-filer gemmes som binære filer med faste såvel som variabel længde datafelter.

|Datatype| Format|
---|---|
|Byte |Genafspilningens spiltilstand (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Heltal |Version af spillet, da replayet blev oprettet (f.eks. 20131216)|
|String |osu! beatmap MD5 hash|
|String| Spillernavn|
|String| osu! replay MD5 hash (inkluderer visse egenskaber ved replay)|
|Kort| Antal 300'er|
|Kort| Antal 100'ere i standard, 150'ere i Taiko, 100'ere i CTB, 100'ere i mani|
|Kort| Antal 50'ere i standard, små frugter i CTB, 50'ere i mani|
|Kort| Antal Gekis i standard, Max 300s i mani|
|Kort| Antal Katus i standard, 200'er i mani|
|Kort| Antal misser|
|Heltal| Samlet score vist på resultatrapporten|
|Kort| Bedste kombination vist på resultatrapporten|
|Byte| Perfekt/fuld kombination (1 = ingen miss og ingen skyderpauser og ingen tidligt færdige skydere)|
|Heltal| Mods brugt. Se nedenfor for en liste over modværdier.|
|String| Livsbjælkediagram: kommaseparerede par u/v, hvor u er tiden i millisekunder inde i sangen, og v er en flydende kommaværdi fra 0 - 1, der repræsenterer mængden af liv, du har på det givne tidspunkt (0 = levetidsbjælke er tom, 1= liv bar er fuld)|
|Lang| Tidsstempel (Windows tikker)|
|Heltal| Længde i bytes af komprimerede afspilningsdata|
|Byte |Array Komprimerede afspilningsdata|
|Lang| Online Score ID|
|Dobbelt| Yderligere mod information. Kun til stede, hvis Target Practice er aktiveret.|

## Referencer

* [OSU! Rhythm Game](https://osu.ppy.sh/home)

* [OSR-filformat](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


