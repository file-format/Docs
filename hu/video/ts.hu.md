{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TS Fájlformátum - Videóátviteli adatfolyam fájl",
  "keywords" :[ "ts", "flie", "extension", "extension", ".ts", "format" ],
  "description":"További információ arról, hogy mi az a TS-fájl és az API-k, amelyek létrehozhatnak és megnyithatnak TS-fájlokat.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## Mi az a TS fájl?

A .ts kiterjesztésű fájl egy videofolyam, amely az adatokat DVD-n tárolja. MPEG-2 ([.mpeg](/hu/video/mpg/)) tömörítési algoritmust használ, hogy maximális hatékonyságot és kompatibilitást érjen el a különböző médiatípusok között, mint például az internetes streamelés és a műsorszórás. A TS fájlformátumot úgy hozták létre, hogy gyenge internetkapcsolattal rendelkező eszközökön, például okostévén is lejátszható legyen.

## TS fájlformátum - További információ

A TS-fájlban lévő adatok hasonlóak az [MP4](/hu/video/mp4/) fájlhoz, de apró darabokra vannak osztva. Mindegyik darab egy apró videóból áll, amelyet egy kis hang követ, és egy opcionális felirat. Egyetlen TS-fájl sok ilyen darabból áll. A videón, a hangon és a feliratokon kívül minden egyes adatcsomag tartalmaz néhány további adatot is a csonkban lévő hibák észleléséhez. Ennek köszönhetően a TS fájlok valamivel nagyobb méretűek.

### Miért érdemes a TS fájlformátumot használni?

Tehát, ha a TS fájlok kissé nagy méretűek, milyen előnyökkel jár ezek használata más fájlformátumok helyett? Nos, a műsorszórásban a kép és hang apró darabjai valós időben továbbíthatók a kommunikációs médián keresztül (vezetékes vagy rádiós). A darabokban lévő extra adatokat a vevő arra használja fel, hogy kihagyja a hibás darabokat.

Ezenkívül a rendszer TS fájlokat használ, mert a műsorszóró rendszernek nincs szüksége a teljes adatfolyamra a lejátszáshoz. Az átvitel felvehető és valós időben használható audio és videó összeállításával.

## Hogyan kell lejátszani a TS fájlokat?

Nos, a TS-fájlok megnyithatók és lejátszhatók a népszerű [VideoLAN VLC médialejátszóban](https://www.videolan.org/vlc/features.html), amely ingyenesen letölthető.

## Referenciák ##

* [MPEG Transport Stream – Wikipedia](https://en.wikipedia.org/wiki/MPEG_transport_stream)

