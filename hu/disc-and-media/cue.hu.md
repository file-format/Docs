{
  "date" : "2021-06-09",
  "keywords" :[ "cue", "file", "extension", "format", "mi a cue fájl", "zene", "cue fájl formátum", "cue fájl formátum specifikációja", "cue lap", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tudjon meg többet a CUE fájlformátumról és az API-król, amelyek CUE-fájlokat hozhatnak létre, konvertálhatnak és megnyithatnak.",
  "title" :"CUE - Cue Sheet File",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Mi az a CUE fájl?

A .cue kiterjesztésű fájl, más néven cue sheet fájl, olyan metaadatfájl, amely a CD-n vagy DVD-n található műsorszámok elrendezéséről tartalmaz információkat. Ezeket a médialejátszók és az optikai lemezkészítő alkalmazások támogatják. A CD-n tárolt fő hangadatokra a cue fájl hivatkozik, valamint a műsorszámok hosszának, a lemezcímeknek és az előadóknak a specifikációi. Így ha egyetlen hangfájl több sávot tartalmaz, a cue fájl felhasználható a hang több fájlra történő felosztására vagy különböző műsorszámokra való hivatkozásra.

## CUE fájlformátum

A CUE- vagy cue-lapfájlok egyszerű szöveges formátumban vannak tárolva, amely ember által olvasható. A cue fájlban lévő információk egy vagy több paraméterrel rendelkező parancsok. Ezek a parancsok az adott parancstól és a kontextustól függően vagy a teljes fájlra, vagy egy külön sávra vonatkoznak. A CDRWIN felhasználói kézikönyv leírja a jelzőlap szintaxisának és szemantikájának specifikációit.

## A CUE lap alapvető parancsai

|Parancs|Leírás|
---|---|
|FILE| Az adatokat tartalmazó fájlra és annak formátumára utal, például [MP3](/hu/audio/mp3/), [WAV](/hu/audio/wav/), vagy egyszerű bináris lemezkép)|
|PÁLYA| Meghatározza a műsorszám környezeti információit, például annak számát és típusát vagy üzemmódját.|
|INDEX| A pozíciót indexként jeleníti meg a FÁJLON belül. A formátum: mm:ss:ff (perc-másodperc-kocka).|
|PREGAP és POSTGAP|Ez egy olyan sáv elő- vagy utórését jelzi, amely nincs tárolva egyetlen adatfájlban sem. A hossza ugyanabban a perc-másodperc képkocka formátumban van megadva, mint az INDEX.|

### CUE lappélda

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## Hivatkozások

* [.cda fájl – a Wikipédia által](https://en.wikipedia.org/wiki/.cda_file)

