{
  "date" : "2021-06-09",
  "keywords" :[ "cue", "soubor", "přípona", "formát", "co je soubor cue", "hudba", "formát souboru cue", "specifikace formátu souboru cue", "list cue", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru CUE a rozhraních API, která mohou vytvářet, převádět a otevírat soubory CUE.",
  "title" :"CUE - Cue Sheet File",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Co je soubor CUE?

Soubor s příponou .cue, také známý jako soubor cue sheet, je soubor metadat, který obsahuje informace o rozložení stop na disku CD nebo DVD. Ty jsou podporovány přehrávači médií a aplikacemi pro tvorbu optických disků. Na hlavní zvuková data uložená na CD se odkazuje soubor cue spolu se specifikacemi délek stop, názvů disků a interpretů. Pokud tedy jeden zvukový soubor obsahuje více stop, soubor cue lze použít k rozdělení zvuku do více souborů nebo k odkazování na různé stopy.

## Formát souboru CUE

Soubory CUE nebo cue sheet jsou uloženy ve formátu prostého textu, který je čitelný pro člověka. Informace v souboru cue jsou příkazy s jedním nebo více parametry. Tyto příkazy se vztahují buď na celý soubor, nebo na jednotlivou stopu, v závislosti na konkrétním příkazu a kontextu. Uživatelská příručka CDRWIN popisuje specifikace syntaxe a sémantiky cue listu.

## Základní příkazy listu CUE

|Příkaz|Popis|
---|---|
|SOUBOR| Odkazuje na soubor obsahující data a jejich formát, jako je [MP3](/cs/audio/mp3/), [WAV](/cs/audio/wav/) nebo prostý binární obraz disku)|
|TRACK| Definuje informace o kontextu stopy, jako je její číslo a typ nebo režim.|
|INDEX| Představuje pozici jako index v rámci SOUBORU. Formát je mm:ss:ff (minuta-sekunda-snímek).|
|PREGAP a POSTGAP|Toto označuje pregap nebo post-gap stopy, která není uložena v žádném datovém souboru. Délka je zadána ve stejném formátu minuta sekundy jako u INDEX.|

### Příklad listu CUE

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
## Reference

* [soubor .cda – z Wikipedie](https://en.wikipedia.org/wiki/.cda_file)

