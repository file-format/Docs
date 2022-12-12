{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "Soubor", "Rozšíření", "Formát souboru", "Formát videa", "TrueMotion Video", "VPX", "On2 Technologies"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 - TrueMotion Video File",
  "description":"Další informace o formátu souboru VP9 a rozhraních API, která mohou vytvářet a otevírat soubory VP9.",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## Co je soubor VP9?

Google vyvinul kodek VP9 jako bezplatný standard kódování videa s otevřeným zdrojovým kódem jako nástupce VP8. Původně byl navržen pro kompresi ultra HD obsahu na YouTube, protože rozšiřuje a zvyšuje efektivitu kódování svého předchůdce. Pokud mluvíme o původních kodecích VPX, pocházely od společnosti On2 Technologies, kterou asimiloval Google v roce 2010. Google později kodek získal jako open-source. Oba formáty VP8 a VP9 jsou k dispozici pod bezplatnou licencí BSD, která operátorům umožňuje organizovat znalosti kódování nebo dekódování jak v exkluzivním softwaru, tak v softwaru s otevřeným zdrojovým kódem, aniž by byl odhalen jejich zdrojový kód.

## Technické vlastnosti VP9

* VP9 poskytuje maximální rozlišení 8192 x 4352 při až 120 fps a více barevných prostorech, s Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 a sRGB
* Tento formát plně podporuje celou řadu webových a mobilních případů použití od komprese s nízkou bitovou rychlostí po vysoce kvalitní ultra-HD s další podporou 10/12bitového kódování a HDR
* Ve srovnání s ostatními může snížit přenosovou rychlost videa až o 50 %.
* Je připraven pro adaptivní streamování a je používán službou YouTube a dalšími známými poskytovateli webových videí
* Dekódování tohoto kodeku podporují zařízení Chrome, Opera, Edge, Firefox a Android a také miliony chytrých televizorů
* Rozlišení videa vyšší než 1080p jsou upravena pomocí VP9 a umožňuje bezeztrátovou kompresi
* Různé barevné prostory jako Rec. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240 a sRGB jsou podporovány VP9
* VP9 může také podporovat HDR video využívající Hybrid Log-Gamma a Perceptual Quantizer


## Stručná historie

* Vývoj video kodeku VP9 byl zahájen v roce 2011 a jeho dekodér byl do webového prohlížeče Chromium přidán v prosinci 2012
* První verze webového prohlížeče Google Chrome byla vydána v únoru 2013 a v té době byla vydána dekódování
* Google vydal Chrome 29.0.1547 s finální podporou VP9 v srpnu 2013
* V říjnu 2013 byl do FFmpeg přidán instinktivní dekodér VP9
* Mozilla přidala podporu VP9 do Firefoxu v prosinci 2013 ve verzi 2, která byla poté vydána 18. března 2014
 

## Práce s VP9

4K video obvykle zvyšuje kvalitu obrazu tím, že konkrétní pixely zmenšuje, kodek VP9 a HEVC je zvětšují, aby se zmenšil datový tok a velikost souboru. I když se to může zdát protichůdné, kódovací stroj bere větší pixely a mění je na produktivitu s vyšším rozlišením. Zdrojové video, obsahující video snímky, je zakódováno nebo komprimováno, aby se vytvořil komprimovaný bitový tok videa. Každý samostatný snímek je nejprve rozdělen na bloky pixelů. Bloky jsou poté prozkoumány na trojrozměrné zrušení a sekvenční spojení mezi snímky jsou vyhodnocena, aby se využily oblasti, které nelze změnit. Ty jsou zakódovány pomocí pohybových vektorů, které zajišťují kvality daného bloku na dalším snímku. Zbytková informace je zakódována pomocí účinné binární komprese.

## Reference

* [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9#:~:text=VP9%20is%20an%20open%20and,on%20Google's%20video%20platform%20YouTube)
* [Webové dokumenty MDN](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [Kokos](https://www.coconut.co/)

