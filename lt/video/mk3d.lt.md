{
  "date": "2021-23-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MK3D failo formatas",
  "keywords": [
"mk3d",
"matroskos vaizdo įrašas",
"mkv formatu",
"stereoskopinis 3d",
"StereoMode",
"vaizdo įrašą",
"failą",
"formatu"
],
  "description": "Sužinokite apie „Matroska“ sukurtų stereoskopinių 3D vaizdo įrašų MK3D failo formatą ir API, kurios gali kurti ir atidaryti MK3D failus.",
  "linktitle": "MK3D",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk3-ltd"
}
},
  "lastmod": "2021-23-02"
}

## Kas yra MK3D failas? ##

MK3D failai priklauso Matroska vaizdo formatų šeimai. Šie failai iš tikrųjų yra **stereoskopiniai 3D** vaizdo įrašai, sukurti naudojant Matroska 3D formatą. MKV failo konteineris naudoja StereoMode lauko reikšmę stereoskopinių 3D vaizdo įrašų tipui apibrėžti. StereoMode reikšmė taip pat pasiekiama norint rodyti senus stereo 3D vaizdo įrašus, atskiriant žalsvai mėlyną ir raudoną spalvas (AnaGlyph)

## Techninės detalės ##
3D vaizdo įrašus galima suglaudinti dviem būdais:

- Atskiras takelis kiekvienai akiai.
- Sujunkite kiekvieną akių stebėjimą į vieną takelį.

MKV failų konteineris palaiko abu šiuos dalykus.

Vieno takelio vaizdo įrašams, kurie yra lengvesni, kai juose yra 3D medžiaga, turite nustatyti lauką **StereoMode**, kuris nusprendžia, ar plokštumos sumontuotos monofoniniame takelyje, arba kairiajame dešiniajame kombinuotame takelyje. Galite naudoti vieną iš šių StereoMode lauko reikšmių:

|Vertė | Aprašymas |
|---|---|
|0| mono|
|1| greta (kairė akis pirma)|
|2| viršus-apačia (dešinė akis pirma)|
|3| viršus-apačia (kairė akis pirma)|
|4| šachmatų lenta (dešinė yra pirma)|
|5| šachmatų lenta (kairėje yra pirmoji)|
|6| eilute perklijuota (dešinysis yra pirmas)|
|7| eilute suterpta (kairysis yra pirmas)|
|8| stulpelis tarpinis (dešinė yra pirma)|
|9| stulpelis tarpinis (kairysis yra pirmas)|
|10| anaglifas (žydra/raudona)|
|11| greta (dešinė akis pirma)|
|12| anaglifas (žalias/rausvai raudonas)|
|13| abi akys surištos viename bloke (kairė akis pirma) (lauko nuoseklus režimas)|
|14| abi akys surištos viename bloke (dešinė akis pirma) (lauko nuoseklus režimas)|

Kelių takelių atveju MKV konteineris turi nuspręsti dėl kiekvieno takelio funkcionalumo atskirai. Darbui atlikti naudojama **TrackOperation** su **TrackCombinePlanes**.


## Nuorodos Nr.

- [Matroska Specification Notes](https://www.matroska.org/technical/notes.html)
- [MKV File Container Support for Stereo 3D Video and the MK3D Files](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

