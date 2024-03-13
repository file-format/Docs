{
  "date": "2022-01-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LRC fayl formatı - LRC faylı nədir?",
  "description": "LRC faylları yarada və aça bilən LRC Lyric faylı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "LRC",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-lr-azc"
}
},
  "lastmod": "2022-01-26"
}

## LRC faylı nədir?

LRC faylı audio mahnının sözlərini ehtiva edən mətn əsaslı sözlər faylıdır. Audio mahnı kompüterdə musiqi pleyer və ya audio pleyer proqramı ilə ifa edildikdə, LRC faylı paralel oxunur və zamanla göstərilir. LRC fayllarında mahnı ifa olunan zaman sözlərin göstərilməsi üçün işarə nöqtələri var. Ümumiyyətlə, LRC faylları audio.mp3 və audio.lrc kimi müvafiq audio faylı ilə eyni ada malikdir. LRC fles [SRT](/video/srt/) kimi altyazı fayllarına bənzəyir.

## LRC Fayl Format - Ətraflı Məlumat

LRC lirik formatlı fayllar düz mətn faylları kimi saxlanılır və mətn faylında açıla və redaktə edilə bilər. LRC faylının məzmunu söz mətninin göstərilməsi üçün rəng məlumatını ehtiva edir.

## LRC formatları

Zamanla hazırlanmış LRC fayllarının bir çox formatı var. Bunlar

### Sadə LRC Format

Xətt Vaxtı Teqləri `[mm:ss.xx]` formatındadır, burada mm dəqiqə, ss saniyə və xx saniyənin yüzdə bir hissəsidir.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Sadə Format Genişləndirilmiş

Buraya M: Male, F: Female, D: Duet istifadə edərək sözlərin cinsini dəyişmək və müəyyən etmək imkanı daxildir.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Təkmilləşdirilmiş LRC formatı

Təkmilləşdirilmiş LRC formatı Simple LRC formatının genişləndirilmiş versiyasıdır. O, ` formatında Word Time Tag əlavə edir<mm:ss.xx> ` əvvəlki sözün sonunda.

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

## İstinadlar

* [LRC Lyrics File Format - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))


