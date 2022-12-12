{
  "date" : "2019-12-13",
  "keywords" :[ "AC3", "soubor", "přípona", "formát", "Kódování zvuku", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů AC3 a rozhraních API, která mohou vytvářet a otevírat soubory AC3.",
  "title" :"AC3 - Audio Codec 3 File",
  "linktitle" : "AC3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Co je soubor AC3?

Soubor s příponou .ac3 je soubor Audio Codec 3 představený společností Dolby Laboratories. Jedná se o zvukový formát, který může obsahovat až šest kanálů zvukového výstupu. Formát byl původně používán pro zvuk, ale nyní se používá také pro jiné aplikace, jako je HDTV vysílání, DVD, Blue-ray disky a herní konzole. Aplikace, které mohou otevřít soubory AC3, zahrnují přehrávač Apple QuickTime, Microsoft Windows Media Player, Winamp, MPlayer a další podobné.

## Formát souboru AC3

Soubory AC3 jsou binární povahy a jsou založeny na Modified Discrete Cosine Transform (MDCT), což je ztrátový kompresní algoritmus. Dolby Laboratories použily algoritmus MDCT spolu s principy percepčního kódování k vývoji zvukového formátu AC-3. To vedlo k vydání formátu AC-3 jako standardu Dolby Digital v roce 1991. Formát podporuje poskytování pěti kanálů pro reproduktory s normálním dosahem (20 Hz - 20 000 Hz) a jednoho kanálu (20 Hz - 120 Hz) pro nízkofrekvenční efekty řízené subwooferem. AC3 podporuje vzorkovací frekvence až 48 kHz.

### Technické podrobnosti o formátu souboru AC3

Technologie Dolby Digital využívá velmi účinný způsob komprese velikosti vícekanálových zvukových souborů bez zhoršení kvality zvuku. Tato komprese vede k menší velikosti souboru, což usnadňuje distribuci zvukových souborů. Pomocí Dolby Digital je možné zahrnout plný 5.1kanálový zvukový mix na film nebo DVD.

#### Specifikace
Specifikace Dolby Digital jsou následující.

|Pole|Specifikace|
---|---|
|Kanály |1.0 až 5.1, diskrétní|
|Datová rychlost DVD, 5.1kanálový zvuk| 384 nebo 448 kbps|
|Datová rychlost disku Blu-ray, 5.1kanálový zvuk|640 kbps|
|Podporuje metadata Dolby |Ano|
|Připojení |S/PDIF, HDMI®, IEEE 1394|
|Možnosti míchání/streamování|Ano|

#### Parametry metadat

|Parametr metadat| Informační|Kontrola|
---|---|---|
|Úroveň dialogu| |Ano|
|Režim kanálu| | Ano|
|LFE kanál| | Ano|
|Režim bitového toku| Ano| Ano|
|Komprese v režimu řádky| | Ano|
|Komprese v režimu RF| | Ano|
|Ochrana proti přemodulování RF| | Ano|
|Střední úroveň downmixu| | Ano|
|Úroveň prostorového downmixu| | Ano|
|Režim Dolby Surround| |Ano|
|Informace o produkci zvuku| Ano ||
|Úroveň míchání| Ano ||
|Typ pokoje| Ano ||
|Autorská práva| Ano||
|Původní bitstream| Ano ||
|Preferovaný stereo downmix| |Ano|
|Úroveň downmixu centra Lt/Rt||Ano|
|Lt/Rt Surround úroveň downmixu||Ano|
|Lo/Ro Středová úroveň downmixu||Ano|
|Lo/Ro Surround úroveň downmixu||Ano|
|Režim Dolby Digital Surround EX™||Ano|
|Typ A/D převodníku|Ano||
|DC filtr||Ano|
|Dolní propust||Ano|
|LFE dolní propust||Ano|
|Prostorový útlum 3 dB||Ano|
|Posun prostorové fáze||Ano|

## Reference

* [AC3 – Wikiepedia](https://en.wikipedia.org/wiki/Dolby_Digital)
* [Dolby Digital 5.1](https://professional.dolby.com/tv/dolby-digital)

