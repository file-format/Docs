{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LRC fájlformátum - Mi az LRC fájl?",
  "description":"További információ az LRC Lyric fájlról és az API-król, amelyek LRC fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Mi az LRC fájl?

Az LRC fájl egy szöveg alapú dalszövegfájl, amely egy hangos dal szövegét tartalmazza. Ha az audio dalt egy zenelejátszóval vagy egy számítógép audiolejátszó szoftverével játssza le, az LRC-fájl párhuzamosan olvasható, és az idő függvényében megjelenik. Az LRC fájlok jelzőpontokat tartalmaznak a dalszöveg megjelenítéséhez a dal lejátszása közben. Általában az LRC fájlok neve megegyezik a megfelelő hangfájllal, például audio.mp3 és audio.lrc. Az LRC-fájlok hasonlóak a feliratfájlokhoz, például [SRT](/hu/video/srt/).

## LRC fájlformátum - További információ

Az LRC dalszöveg formátumú fájlok egyszerű szöveges fájlként kerülnek mentésre, és szövegfájlban nyithatók meg és szerkeszthetők. Az LRC-fájl tartalma színinformációkat tartalmaz a dalszöveg megjelenítéséhez.

## LRC formátumok

Az LRC-fájloknak több formátuma is létezik, amelyeket az idők során fejlesztettek ki. Ezek

### Egyszerű LRC formátum

A soridő címkék formátuma `[mm:ss.xx]`, ahol mm a perc, ss másodperc és xx századmásodperc.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Egyszerű formátum kiterjesztett

Tartalmazza a dalszöveg nemének megváltoztatásának és megadásának lehetőségét az M: Férfi, F: Nő, D: Duett használatával.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Továbbfejlesztett LRC formátum

A továbbfejlesztett LRC formátum a Simple LRC formátum kiterjesztett változata. Hozzáad egy Word időcímkét a formátumban`<mm:ss.xx>` az előző szó végén.

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

## Hivatkozások

* [LRC dalszöveg fájlformátuma – Wikipédia](https://en.wikipedia.org/wiki/LRC_(file_format))

