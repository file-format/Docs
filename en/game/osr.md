{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about OSR file format and APIs that can create and open OSR files.",
  "title" : "OSR File - osu! Replay File Format",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr",
      "parent" : "game"
    }
  },
  "lastmod" : "2021-09-08"
}

## What is an OSR file?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**MIME Type of OSR File Format:** x-osu-replay

## OSR File Format

OSR files are saved as binary files with fixed as well as variable length data fields.

|Data Type| Format|
---|---|
|Byte	|Game mode of the replay (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Integer	|Version of the game when the replay was created (ex. 20131216)|
|String	|osu! beatmap MD5 hash|
|String|	Player name|
|String|	osu! replay MD5 hash (includes certain properties of the replay)|
|Short|	Number of 300s|
|Short|	Number of 100s in standard, 150s in Taiko, 100s in CTB, 100s in mania|
|Short|	Number of 50s in standard, small fruit in CTB, 50s in mania|
|Short|	Number of Gekis in standard, Max 300s in mania|
|Short|	Number of Katus in standard, 200s in mania|
|Short|	Number of misses|
|Integer|	Total score displayed on the score report|
|Short|	Greatest combo displayed on the score report|
|Byte|	Perfect/full combo (1 = no misses and no slider breaks and no early finished sliders)|
|Integer|	Mods used. See below for list of mod values.|
|String|	Life bar graph: comma separated pairs u/v, where u is the time in milliseconds into the song and v is a floating point value from 0 - 1 that represents the amount of life you have at the given time (0 = life bar is empty, 1= life bar is full)|
|Long|	Time stamp (Windows ticks)|
|Integer|	Length in bytes of compressed replay data|
|Byte |Array	Compressed replay data|
|Long|	Online Score ID|
|Double|	Additional mod information. Only present if Target Practice is enabled.|

## References

* [OSU! Rhythm Game](https://osu.ppy.sh/home)
* [OSR File Format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)
