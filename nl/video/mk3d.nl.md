{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MK3D-bestandsindeling",
  "keywords" :[ "mk3d", "matroska video", "mkv-formaat", "stereoscopisch 3d", "StereoMode", "video", "bestand", "formaat"],
  "description":"Meer informatie over het MK3D-bestandsformaat voor stereoscopische 3D-video's gemaakt door Matroska en API's die MK3D-bestanden kunnen maken en openen.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## Wat is een MK3D-bestand? ##

De MK3D-bestanden behoren tot de familie Matroska-videoformaten. Deze bestanden zijn eigenlijk **stereoscopische 3d** video's gemaakt met Matroska 3D-formaat. Het MKV-bestand Container gebruikt de waarde van een StereoMode-veld om het type stereoscopisch 3D-videomateriaal te definiëren. Er is ook een StereoMode-waarde beschikbaar om de oude stereo 3D-video's weer te geven door cyaan en rode kleuren te scheiden (AnaGlyph)

## Technische details ##
De 3D-video's kunnen op de volgende twee manieren worden gecomprimeerd:

- Aparte baan voor elk oog.
- Combineer elke eye-tracking in een enkele track.

De MKV-bestandscontainer ondersteunt beide.

Voor de single-track video's die gemakkelijker zijn met het 3D-materiaal erin, moet je het veld **StereoMode** instellen dat bepaalt of de vliegtuigen worden geassembleerd in de mono of links-rechts gecombineerde track. U kunt een van de volgende StereoMode-veldwaarden gebruiken:

|Waarde | Beschrijving |
|---|---|
|0| mono|
|1| naast elkaar (linkeroog is eerst)|
|2| boven-onder (rechteroog is eerst)|
|3| boven-onder (linkeroog is eerst)|
|4| checkboard (rechts is eerst)|
|5| checkboard (links is eerst)|
|6| rij interleaved (rechts is eerst)|
|7| rij interleaved (links is eerst)|
|8| kolom interleaved (rechts is eerst)|
|9| kolom interleaved (links is eerst)|
|10| anaglyph (cyaan/rood)|
|11| naast elkaar (rechteroog is eerst)|
|12| anaglyph (groen/magenta)|
|13| beide ogen in één blok geregen (linkeroog is eerst) (veldsequentiële modus)|
|14| beide ogen in één blok geregen (rechteroog is eerst) (veldsequentiële modus)|

Voor de meerdere sporen moet de MKV-container de functionaliteit van elk spoor afzonderlijk bepalen. De **TrackOperation** met **TrackCombinePlanes** worden gebruikt om het werk te doen.


## Referenties ##

- [Matroska-specificaties](https://www.matroska.org/technical/notes.html)
- [MKV-bestandscontainerondersteuning voor stereo 3D-video en de MK3D-bestanden](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d- bestanden/)

