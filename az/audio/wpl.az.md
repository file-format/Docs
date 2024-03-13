{
  "date": "2021-06-11",
  "keywords": [
"wpl",
"wpl faylı",
"uzadılması",
"format",
"wpl faylı nədir",
"musiqi",
"wpl fayl formatı"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "WPL faylları yarada, çevirə və aça bilən WPL fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "WPL - Windows Media Player Playlist Faylı",
  "linktitle": "WPL",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wp-azl"
}
},
  "lastmod": "2021-06-11"
}

## WPL faylı nədir?

.wpl uzantılı fayl Microsoft Windows Media Player-də işlədiləcək mahnıların siyahısını ehtiva edir. Bu fayllar adətən istifadəçilər tərəfindən video və audio kolleksiyaları üçün yaradılır. WPL faylında yazılmış məzmun .wpl faylının yaradıcısı tərəfindən seçilmiş multimedia faylları üçün sadəcə kataloq yolları və ya yerlərdir, beləliklə, media pleyer proqramı multimedia məzmununu öz kataloq yerlərindən dərhal tapıb oxuya bilər.

## WPL fayl formatı

WPL (Windows Media Player Playlist) Microsoft Windows Media Player 9 və ya daha yuxarı versiyalarında istifadə edilən xüsusi fayl formatıdır. Bu, multimedia çalğı siyahılarını saxlayan kompüter fayl formatıdır. Varsayılan olaraq, çalğı siyahısı .wpl (Windows Media Player Playlist) genişləndirilməsi ilə saxlanılır. Data disklərinizi bu artırmanı dəstəkləməyən cihazda oynamaq istəyirsinizsə, bunun əvəzinə [.m3u](/audio/m3u/) artırmasından istifadə edə bilərsiniz. WPL faylının elementləri XML formatında təqdim olunur.

Ən yüksək səviyyəli smil elementi faylın elementlərinin Sinxronlaşdırılmış Multimedia İnteqrasiya Dili (SMIL) strukturunu izlədiyini müəyyən edir. Fayl .wpl uzantısı ilə yaradılır və saxlanılır və onun MIME növü application/vnd.ms-wpl-dir.

### WPL nümunəsi

Budur wpl faylının bir nümunəsi:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## İstinadlar ##

* [MPEG-1 Audio Layer II - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)


