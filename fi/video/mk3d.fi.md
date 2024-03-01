{
  "date": "2021-23-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MK3D tiedostomuoto",
  "keywords": [
"mk3d",
"matroska video",
"mkv muodossa",
"stereoskooppinen 3d",
"StereoMode",
"video",
"tiedosto",
"muoto"
],
  "description": "Opi Matroskan luomien stereoskooppisten 3D-videoiden MK3D-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata MK3D-tiedostoja.",
  "linktitle": "MK3D",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk3-fid"
}
},
  "lastmod": "2021-23-02"
}

## Mikä on MK3D-tiedosto? ##

MK3D-tiedostot kuuluvat Matroska-videoformaattien perheeseen. Nämä tiedostot ovat itse asiassa **stereoskooppisia 3D**-videoita, jotka on luotu Matroska 3D -muodossa. MKV-tiedostosäiliö käyttää StereoMode-kentän arvoa stereoskooppisen 3D-videomateriaalin tyypin määrittämiseen. StereoMode-arvo on myös käytettävissä vanhojen stereo3D-videoiden näyttämiseen erottamalla syaani ja punainen värit (AnaGlyph)

## Tekniset yksityiskohdat ##
3D-videot voidaan pakata kahdella tavalla:

- Erillinen rata jokaiselle silmälle.
- Yhdistä jokainen katseenseuranta yhdeksi kappaleeksi.

MKV-tiedostosäiliö tukee näitä molempia.

Yksiraitaisia videoita varten, jotka ovat helpompia, kun niiden sisällä on 3D-materiaalia, sinun on asetettava **StereoMode**-kenttä, joka päättää, kootaanko tasot mono- tai vasemmalle oikealle yhdistetylle radalle. Voit käyttää yhtä seuraavista StereoMode-kentän arvoista:

|Arvo | Kuvaus |
|---|---|
|0| mono|
|1| vierekkäin (vasen silmä ensin)|
|2| ylhäältä alas (oikea silmä on ensin)|
|3| ylhäältä alas (vasen silmä ensin)|
|4| valintalauta (oikea on ensin)|
|5| valintalauta (vasen on ensimmäinen)|
|6| rivi lomitettu (oikea on ensimmäinen)|
|7| rivi lomitettu (vasen on ensimmäinen)|
|8| sarake limitetty (oikea on ensin)|
|9| sarake limitetty (vasen on ensimmäinen)|
|10| anaglyfi (syaani/punainen)|
|11| vierekkäin (oikea silmä on ensin)|
|12| anaglyfi (vihreä/magenta)|
|13| molemmat silmät sidottu yhteen lohkoon (vasen silmä on ensimmäinen) (kenttäjärjestystila)|
|14| molemmat silmät sidottu yhteen lohkoon (oikea silmä on ensin) (kenttäjärjestystila)|

Useita raitoja varten MKV-kontin on päätettävä kunkin raidan toimivuudesta erikseen. **TrackOperation** ja **TrackCombinePlanes** käytetään työn suorittamiseen.


## Viitteet ##

- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

