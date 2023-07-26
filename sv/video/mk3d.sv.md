{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MK3D filformat",
  "keywords" :[ "mk3d", "matroska video", "mkv-format", "stereoskopisk 3d", "StereoMode", "video", "fil", "format" ],
  "description":"Lär dig om MK3D-filformat för stereoskopiska 3d-videor skapade av Matroska och API:er som kan skapa och öppna MK3D-filer.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## Vad är en MK3D fil? ##

MK3D-filerna tillhör Matroska-videoformatfamiljen. Dessa filer är faktiskt **stereoskopiska 3D**-videor skapade med Matroska 3D-format. MKV-filbehållaren använder ett StereoMode-fälts värde för att definiera typen av stereoskopisk 3D-video. Ett StereoMode-värde är också tillgängligt för att visa de gamla stereo 3D-videorna genom att separera cyan och röda färger (AnaGlyph)

## Tekniska detaljer ##
3D-videorna kan komprimeras på följande två sätt:

- Separat spår för varje öga.
- Kombinera varje eyetracking till ett enda spår.

MKV-filbehållaren stöder båda dessa.

För enkelspårsvideor som är enklare med 3D-materialet inuti dem, måste du ställa in fältet **StereoMode** som bestämmer att antingen planen monteras i mono eller vänster höger kombinerat spår. Du kan använda ett av följande StereoMode-fältvärden:

|Värde | Beskrivning |
|---|---|
|0| mono|
|1| sida vid sida (vänster öga är först)|
|2| topp-botten (höger öga är först)|
|3| topp-botten (vänster öga är först)|
|4| checkboard (höger är först)|
|5| checkboard (vänster är först)|
|6| rad interfolierad (höger är först)|
|7| rad interfolierad (vänster är först)|
|8| kolumn interfolierad (höger är först)|
|9| kolumn interfolierad (vänster är först)|
|10| anaglyf (cyan/röd)|
|11| sida vid sida (höger öga är först)|
|12| anaglyf (grön/magenta)|
|13| båda ögonen spetsade i ett block (vänster öga är först) (fältsekventiellt läge)|
|14| båda ögonen spetsade i ett block (höger öga är först) (fältsekventiellt läge)|

För flera spår måste MKV-behållaren bestämma funktionaliteten för varje spår separat. **TrackOperation** med **TrackCombinePlanes** används för att göra jobbet.


## Referenser ##

- [Matroska-specifikationsanmärkningar](https://www.matroska.org/technical/notes.html)
- [MKV File Container Support for Stereo 3D Video and the MK3D Files](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

