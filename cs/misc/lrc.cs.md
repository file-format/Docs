{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru LRC - Co je soubor LRC?",
  "description":"Další informace o souboru LRC Lyric a rozhraních API, která mohou vytvářet a otevírat soubory LRC.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Co je soubor LRC?

Soubor LRC je textový soubor, který obsahuje text zvukové písně. Když se zvuková skladba přehrává pomocí hudebního přehrávače nebo softwaru audio přehrávače v počítači, soubor LRC se čte paralelně a zobrazuje se s časem. Soubory LRC obsahují startovací body pro zobrazení textu při přehrávání skladby. Obecně mají soubory LRC stejný název jako odpovídající zvukový soubor, například audio.mp3 a audio.lrc. Soubory LRC jsou podobné souborům titulků, jako je [SRT](/cs/video/srt/).

## Formát souboru LRC – Další informace

Soubory ve formátu textů LRC se ukládají jako soubory prostého textu a lze je otevřít a upravit v textovém souboru. Obsah souboru LRC obsahuje barevné informace pro zobrazení textu písně.

## Formáty LRC

Existuje několik formátů souborů LRC, které byly vyvinuty v průběhu času. Tyto

### Jednoduchý formát LRC

Časové značky řádku jsou ve formátu `[mm:ss.xx]`, kde mm jsou minuty, ss jsou sekundy a xx jsou setiny sekundy.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Rozšířený jednoduchý formát

Zahrnuje možnost změnit a určit pohlaví textů pomocí M: Male, F: Female, D: Duet.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Vylepšený formát LRC

Rozšířený formát LRC je rozšířenou verzí jednoduchého formátu LRC. Přidá Word Time Tag ve formátu`<mm:ss.xx>` na konci předchozího slova.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## Reference

* [Formát souboru s texty LRC – Wikipedie](https://en.wikipedia.org/wiki/LRC_(file_format))

