{
  "date": "2021-23-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MK3D filformat",
  "keywords": [
"mk3d",
"matroska video",
"mkv format",
"stereoskopisk 3d",
"StereoMode",
"video",
"fil",
"format"
],
  "description": "Lær om MK3D-filformat til stereoskopiske 3d-videoer skabt af Matroska og API'er, der kan oprette og åbne MK3D-filer.",
  "linktitle": "MK3D",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk3-dad"
}
},
  "lastmod": "2021-23-02"
}

## Hvad er en MK3D fil? ##

MK3D-filerne tilhører Matroska-videoformatfamilien. Disse filer er faktisk **stereoskopiske 3d**-videoer oprettet ved hjælp af Matroska 3D-format. MKV-filbeholderen bruger et StereoMode-felts værdi til at definere typen af stereoskopisk 3D-video. En StereoMode-værdi er også tilgængelig for at vise de gamle stereo 3D-videoer ved at adskille cyan og røde farver (AnaGlyph)

## Tekniske detaljer ##
3D-videoerne kan komprimeres på følgende to måder:

- Separat spor for hvert øje.
- Kombiner hver øjensporing til et enkelt spor.

MKV-filbeholderen understøtter begge disse.

For enkeltsporede videoer, som er nemmere med 3D-materialet inde i dem, skal du indstille feltet **StereoMode**, som bestemmer, at enten flyene samles i mono- eller venstre-højre kombinerede spor. Du kan bruge en af følgende StereoMode-feltværdier:

|Værdi | Beskrivelse |
|---|---|
|0| mono|
|1| side om side (venstre øje er først)|
|2| top-bund (højre øje er først)|
|3| top-bund (venstre øje er først)|
|4| checkboard (højre er først)|
|5| checkboard (venstre er først)|
|6| række indskudt (højre er først)|
|7| række indskudt (venstre er først)|
|8| kolonne sammenflettet (højre er først)|
|9| kolonne interleaved (venstre er først)|
|10| anaglyf (cyan/rød)|
|11| side om side (højre øje er først)|
|12| anaglyf (grøn/magenta)|
|13| begge øjne snøret i én blok (venstre øje er først) (felt sekventiel tilstand)|
|14| begge øjne snøret i én blok (højre øje er først) (feltsekventiel tilstand)|

For de flere spor skal MKV-beholderen bestemme funktionaliteten af hvert spor separat. **TrackOperation** med **TrackCombinePlanes** bruges til at udføre jobbet.


## Referencer ##

- [Matroska Specification Notes](https://www.matroska.org/technical/notes.html)
- [MKV File Container Support for Stereo 3D Video and the MK3D Files](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

