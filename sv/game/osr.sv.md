{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lär dig mer om OSR-filformat och API:er som kan skapa och öppna OSR-filer.",
  "title" : "OSR-fil - osu! Spela om filformat",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-sv",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Vad är en OSR fil?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**MIME-typ av OSR-filformat:** x-osu-replay

## OSR filformat

OSR-filer sparas som binära filer med både fasta och varierande datafält.

|Datatyp| Format|
---|---|
|Byte |Spelläge för reprisen (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Heltal |Version av spelet när reprisen skapades (ex. 20131216)|
|Sträng |osu! beatmap MD5 hash|
|Sträng| Spelarens namn|
|Sträng| osu! replay MD5 hash (inkluderar vissa egenskaper för replay)|
|Kort| Antal 300-tal|
|Kort| Antal 100-tal i standard, 150-tal i Taiko, 100-tal i CTB, 100-tal i mani|
|Kort| Antal 50-tal i standard, liten frukt i CTB, 50-tal i mani|
|Kort| Antal Gekis i standard, Max 300s i mani|
|Kort| Antal Katus i standard, 200-tal i mani|
|Kort| Antal missar|
|Heltal| Totalpoäng som visas i poängrapporten|
|Kort| Bästa kombinationen som visas i poängrapporten|
|Byte| Perfekt/full kombo (1 = inga missar och inga skjutreglage och inga tidigt färdiga skjutreglage)|
|Heltal| Mods används. Se nedan för lista över modvärden.|
|Sträng| Livsstapeldiagram: kommaseparerade par u/v, där u är tiden i millisekunder in i låten och v är ett flyttalvärde från 0 - 1 som representerar mängden liv du har vid en given tidpunkt (0 = livsstapel är tom, 1= livstapeln är full)|
|Lång| Tidsstämpel (Windows bockar)|
|Heltal| Längd i byte av komprimerad uppspelningsdata|
|Byte |Array Komprimerad uppspelningsdata|
|Lång| Online poäng-ID|
|Dubbel| Ytterligare modinformation. Endast närvarande om Target Practice är aktiverat.|

## Referenser

* [OSU! Rhythm Game](https://osu.ppy.sh/home)

* [OSR-filformat](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


