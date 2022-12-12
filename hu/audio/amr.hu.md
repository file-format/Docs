{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "fájl", "kiterjesztés", "formátum", "mi az amr fájl", "zene", "amr fájlformátum", "amr fájl", "amr fájl konvertálása mp3", "play amr file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az AMR-fájlformátumról és az API-król, amelyek AMR-fájlokat hozhatnak létre, konvertálhatnak és megnyithatnak.",
  "title" :"AMR – adaptív többsebességű kodekfájl",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## Mi az AMR fájl?
Az .amr kiterjesztésű fájl az **Adaptive Multi-Rate** audiokodek számára releváns audioadat-formátum; egy többsebességű keskeny sávú beszédkodekből áll, amely a keskeny sávú jeleket 4,75-12,2 kbit/s bitsebességgel kódolja, 7,4 kbit/s-tól kezdődően díjas minőségű beszéddel; link adaptációt használ a nyolc különböző bitsebesség egyikének kiválasztásához.

## AMR fájlformátum
Az AMR fájlformátum számos kódolási technikát használ, az ACELP (Algebraic Code Excited Linear Prediction) algoritmus az egyik legjobb technika; Az emberi beszédhang hatékonyabb tömörítésére tervezték. Az AMR-t a 3GPP szabvány hang- vagy beszédkodekként állította be 1999-ben. Az AMR fájlformátumot a beszédhang tárolására is használják az **Adaptive Multi-Rate** audiokodek használatával, amelyet sok okostelefon használ a rögzített felvételek tárolására. beszédeket.

### Fájlformátum szerkezete
Az AMR (Adaptive Multi-Rate) egy hangformátum; széles körben használják különféle mobil alkalmazásokban és eszközökben, jellemzően audiolejátszókban/felvevőkben vagy VoIP típusú alkalmazásokban. Az AMR tovább osztályozható:

1. AMR-NB (keskenysáv)
2. AMR-WB (szélessávú)

Az AMR általában az AMR-NB-re utal. Az AMR fájlformátum a következő szerkezettel rendelkezik:

Minden AMR-fájl tartalmaz egy 6 bájtos fejlécet, amely AMR-hangként ismeri fel a fájlt. Ez a fejléc mindig a következőre van állítva:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Ez általában minden AMR-NB fájlra hasonló. Ha a fejléc szabványt követ, akkor valószínű, hogy a fájl sérült, ezért nem szabad használni. az AMR fájl egész számú csomagolt hangkockából áll. Ezek a képkockák egyenként 20 ms-os hangot alkotnak. Minden egyes képkocka kódolható az érvényes AMR-NB módok bármelyikével (0-7, 8 SID DTX módban). Mivel a keretek különböző bitsebességgel kódolhatók, ezt a tipikus módszert Adaptive Multi-Rate (AMR)-nek nevezik.
#### AMR módok
Íme a különböző AMR módok és a hozzájuk tartozó bitráták:

|MODE| BITÁRAK |
---|---|
|0| AMR 4.75 – 4.75 kbit/s|
|1 | AMR 5.15 – 5.15 kbit/s sebességgel kódol|
|2 | AMR 5.9 - 5,9 kbit/s sebességgel kódol|
|3 | AMR 6.7 - 6,7 kbit/s sebességgel kódol|
|4 | AMR 7.4 - 7,4 kbit/s sebességgel kódol|
|5 | AMR 7,95 – 7,95 kbit/s|
|6 | AMR 10.2 - 10,2 kbit/s sebességgel kódol|
|7 | AMR 12.2 - 12,2 kbit/s sebességgel kódol|

Az AMR módok keretmérete bájtban (beleértve a fejléc bájtját is) az alábbiakban látható:

|CMR |MODE |KERET MÉRETE( bájtban )|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5,15 |14|
|2 |AMR 5,9 |16|
|3 |AMR 6,7 |18|
|4 |AMR 7,4 |20|
|5 |AMR 7,95 |21|

## Referenciák ##

* [Adaptive Multi-Rate audiokodek – a Wikipedia által](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [RTP hasznos adatformátum és fájltároló formátum AMR és AMR-WB audiokodekekhez](https://tools.ietf.org/html/rfc4867#page-35)

