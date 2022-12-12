{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "File", "Extension", "File Format", "Video Format", "TrueMotion Video", "VPX", "On2 Technologies"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 – TrueMotion Video File",
  "description":"További információ a VP9 fájlformátumról és az API-król, amelyek VP9 fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## Mi az a VP9 fájl?

A Google a VP9 kodeket jogdíjmentes, nyílt forráskódú videókódolási szabványként fejlesztette ki a VP8 utódjaként. Eredetileg a YouTube ultra HD-tartalmának tömörítésére tervezték, mert kiterjeszti és javítja elődje kódolási hatékonyságát. Ha már az eredeti VPX kodekekről beszélünk, akkor azok az On2 Technologiestől származtak, amelyet a Google 2010-ben asszimilált. A Google később nyílt forráskódú kodeket biztosított. A VP8 és a VP9 mindkét formátum ingyenes BSD-licenc alatt érhető el, amely lehetővé teszi az üzemeltetők számára, hogy megszervezzék kódolási vagy dekódolási jártasságukat mind az exkluzív szoftverek, mind a nyílt forráskódú szoftverek terén anélkül, hogy felfednék forráskódjukat.

## A VP9 műszaki jellemzői

* A VP9 8192x4352 maximális felbontást biztosít akár 120 képkocka/mp sebességgel és többféle színtérrel a Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 és sRGB segítségével
* Ez a formátum a webes és mobilhasználati esetek teljes választékát az alacsony bitsebességű tömörítéstől a kiváló minőségű ultra-HD-ig, a 10/12 bites kódolás és a HDR további támogatásával teljes mértékben támogatja
* Másokhoz képest akár 50%-kal is csökkentheti a videó bitsebességét
* Az adaptív streaminghez készült, és a YouTube és más jól ismert webes videószolgáltatók használják
* Chrome, Opera, Edge, Firefox és Android eszközök, valamint több millió okostévé támogatja ennek a kodeknek a dekódolását
* Az 1080p-nél nagyobb videofelbontásokat a VP9 módosítja, és veszteségmentes tömörítést tesz lehetővé
* Különböző színterek, mint például Rec. 601, Rec. 709, Rec. A 2020, az SMPTE-170, az SMPTE-240 és az sRGB-t a VP9 támogatja
* A Hybrid Log-Gamma és a Perceptual Quantizer használatával HDR videót a VP9 is támogatja


## Rövid története

* A VP9 videokodek fejlesztése 2011-ben kezdődött, dekódolója pedig 2012 decemberében került be a Chromium webböngészőbe
* Az első Google Chrome webböngésző verziója 2013 februárjában jelent meg, és ekkor adta ki a dekódolást
* A Google 2013 augusztusában kiadta a Chrome 29.0.1547-es verzióját a VP9 végleges támogatásával
* 2013 októberében egy ösztönös VP9 dekódert adtak az FFmpeghez
* A Mozilla 2013 decemberében hozzáadta a VP9 támogatást a Firefoxhoz a 2-es verzióban, amelyet 2014. március 18-án adtak ki.
 

## A VP9 működése

Általában a 4K videó javítja a képminőséget azáltal, hogy bizonyos pixeleket kisebbít, a VP9 kodek és a HEVC pedig megnöveli őket a bitráta és a fájlméret csökkentése érdekében. Bár ez ellentmondásosnak tűnhet, a kódoló motor a nagyobb képpontokat veszi fel, és jobb felbontású termelékenységre változtatja azokat. A videokockákat tartalmazó forrásvideót kódolják vagy tömörítik, hogy tömörített videó bitfolyamot készítsenek. Minden különálló képkockát először pixelblokkokra osztanak fel. A blokkokat ezután alaposan megvizsgálják a háromdimenziós elvetések szempontjából, és kiértékelik a keretek közötti szekvenciális kapcsolatokat, hogy kihasználják azokat a területeket, amelyeken nem lehet változtatni. Ezeket mozgásvektorok kódolják, amelyek biztosítják az adott blokk minőségét a következő képkockán. A maradék információt hatékony bináris tömörítéssel kódolják.

## Hivatkozások

* [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9#:~:text=VP9%20is%20an%20open%20and,on%20Google's%20video%20platform%20YouTube)
* [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [Coconut](https://www.coconut.co/)

