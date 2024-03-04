{
  "date": "2021-03-12",
  "keywords": [
"VP9",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Vaizdo įrašo formatas",
"TrueMotion vaizdo įrašas",
"VPX",
"On2 technologijos"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "VP9 – „TrueMotion“ vaizdo failas",
  "description": "Sužinokite apie VP9 failo formatą ir API, kurios gali kurti ir atidaryti VP9 failus.",
  "linktitle": "VP9",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp-lt9"
}
},
  "lastmod": "2021-03-27"
}

## Kas yra VP9 failas?

Google has developed the VP9 codec as a royalty-free, open-source video coding standard as the successor to VP8. Iš pradžių jis buvo skirtas suspausti itin HD turinį YouTube, nes išplečia ir pagerina savo pirmtako kodavimo efektyvumą. Jei kalbėsime apie originalius VPX kodekus, jie atkeliavo iš On2 Technologies, kurią 2010 m. asimiliavo Google. Vėliau Google sukūrė kodeką atviruoju šaltiniu. VP8 ir VP9 abu formatai yra prieinami pagal nemokamą BSD licenciją, leidžiančią operatoriams koduoti arba dekoduoti tiek išskirtinės programinės įrangos, tiek atvirojo kodo programinės įrangos įgūdžius, neatskleidžiant jų šaltinio kodo.

## Techninės VP9 savybės

* VP9 suteikia maksimalią 8192 x 4352 skiriamąją gebą iki 120 kadrų per sekundę ir kelias spalvų erdves su Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 ir sRGB
* Šis formatas visiškai palaiko visas žiniatinklio ir mobiliojo ryšio naudojimo atvejus nuo mažo bitų dažnio glaudinimo iki aukštos kokybės ultra-HD, su papildomu 10/12 bitų kodavimo ir HDR palaikymu.
* Palyginti su kitais, vaizdo įrašo spartą galima sumažinti net 50%.
* Jis pritaikytas adaptyviam srautiniam perdavimui ir yra naudojamas YouTube bei kitų žinomų interneto vaizdo įrašų teikėjų
* Chrome, Opera, Edge, Firefox ir Android įrenginiai, taip pat milijonai išmaniųjų televizorių palaiko šio kodeko iššifravimą
* Didesnė nei 1080p vaizdo raiška modifikuojama naudojant VP9 ir leidžia glaudinti be nuostolių
* Skirtingos spalvų erdvės, pvz., Rec. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240 ir sRGB palaiko VP9
* VP9 taip pat gali palaikyti HDR vaizdo įrašą, naudojant hibridinį log-gamą ir suvokimo kvantavimo priemonę


## Trumpa istorija

 *  VP9 vaizdo kodekas pradėtas kurti 2011 m., o jo dekoderis buvo pridėtas prie Chromium žiniatinklio naršyklės 2012 m. gruodžio mėn.
 *  Pirmoji jos Google Chrome žiniatinklio naršyklės versija buvo išleista 2013 m. vasario mėn. ir tuo metu išleista dekodavimo versija
 *  2013 m. rugpjūčio mėn. Google išleido Chrome 29.0.1547 su galutiniu VP9 palaikymu
 *  2013 m. spalio mėn. prie FFmpeg buvo pridėtas instinktyvus VP9 dekoderis
 *  Mozilla 2013 m. gruodžio mėn. Firefox pridėjo VP9 išlaikymą 2 versijoje, kuri tada buvo išleista 2014 m. kovo 18 d.
 
## VP9 veikimas

Paprastai 4K vaizdo įrašas pagerina vaizdo kokybę sumažindamas tam tikrus pikselius, o VP9 kodekas ir HEVC padidina juos, kad sumažintų bitų spartą ir failo dydį. Nors tai gali atrodyti prieštaringa, kodavimo variklis paima didesnius pikselius ir pakeičia juos į geresnę skiriamąją gebą. Šaltinio vaizdo įrašas, sudarytas iš vaizdo kadrų, yra užkoduotas arba suglaudintas, kad būtų sukurtas suspaustas vaizdo bitų srautas. Kiekvienas atskiras kadras pirmiausia yra padalintas į pikselių blokus. Tada blokai kruopščiai tikrinami, ar nėra trimačių atmetimų, ir įvertinamos nuoseklios jungtys tarp kadrų, kad būtų galima pasinaudoti sritimis, kurių negalima pakeisti. Jie užkoduojami per judesio vektorius, kurie užtikrina nurodyto bloko savybes kitame kadre. Likutinė informacija užkoduojama naudojant efektyvų dvejetainį suspaudimą.

## Nuorodos

 * [VP9 Vikipedija](https://en.wikipedia.org/wiki/VP9)
 * [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
 * [Coconut](https://www.coconut.co/)

