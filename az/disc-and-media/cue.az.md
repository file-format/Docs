{
  "date": "2021-06-09",
  "keywords": [
"replika",
"fayl",
"uzadılması",
"format",
"cue faylı nədir",
"musiqi",
"cue fayl formatı",
"cue fayl formatının spesifikasiyası",
"işarə vərəqi",
"CDRWIN"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "CUE faylları yarada, çevirə və aça bilən CUE fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "CUE - Cue Vərəq Faylı",
  "linktitle": "CUE",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cu-aze"
}
},
  "lastmod": "2021-07-01"
}

## CUE faylı nədir?

Cue vərəqi faylı kimi də tanınan .cue uzantısı olan fayl CD və ya DVD-də treklərin tərtibatı haqqında məlumatı ehtiva edən metadata faylıdır. Bunlar media pleyerləri və optik disklərin müəllif proqramları tərəfindən dəstəklənir. CD-də saxlanılan əsas audio məlumatlara trek uzunluğu, disk adları və ifaçıların spesifikasiyası ilə yanaşı replika faylı istinad edilir. Beləliklə, bir audio faylda bir neçə trek varsa, replika faylı səsi bir neçə fayla bölmək və ya müxtəlif treklərə istinad etmək üçün istifadə edilə bilər.

## CUE Fayl Format

CUE və ya replika vərəqi faylları insan tərəfindən oxuna bilən düz mətn formatında saxlanılır. Replika faylındakı məlumatlar bir və ya bir neçə parametrli əmrlərdir. Bu əmrlər xüsusi əmr və kontekstdən asılı olaraq ya bütün fayla, ya da fərdi trekə tətbiq edilir. CDRWIN istifadəçi təlimatı replika vərəqinin sintaksisi və semantikası üçün spesifikasiyaları təsvir edir.

## CUE Vərəqinin Əsas Əmrləri

|Əmr|Təsvir|
---|---|
|FILE| Məlumatı və onun [MP3](/audio/mp3/), [WAV](/audio/wav/) və ya sadə ikili disk şəkli kimi formatını ehtiva edən fayla istinad edir)|
|TRACK| Nömrə və növü və ya rejimi kimi trek kontekst məlumatını müəyyən edir.|
|İNDEKS| Mövqeyi FILE daxilində indeks kimi təmsil edir. Format mm:ss:ff (dəqiqə-saniyə-kadr).|
|PREGAP və POSTGAP|Bu, heç bir məlumat faylında saxlanmayan trekin əvvəlcədən və ya sonrakı boşluğunu göstərir. Uzunluq INDEX.| ilə eyni dəqiqə-saniyə kadr formatında müəyyən edilir

### CUE Vərəqinin Nümunəsi

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

## Digər CUE faylları

Burada **.cue** fayl uzantısından istifadə edən digər fayl növləri var.

**Disk və Media**
- [CUE - Cue Vərəq Faylı](/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/disc-and-media/cue-cdrwin/)

## İstinadlar

* [.cda faylı - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/.cda_file)


