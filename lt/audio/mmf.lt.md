{
  "date": "2021-08-09",
  "keywords": [
"mmf",
"failą",
"pratęsimas",
"formatu",
"garso",
"smaf",
"mmf plėtinys",
"mmf failus",
"mobilusis muzikos failas",
"yamaha"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie MMF failo formatą ir API, kurios gali kurti ir atidaryti MMF failus.",
  "title": "MMF – mobiliosios muzikos failo formatas",
  "linktitle": "MMF",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mm-ltf"
}
},
  "lastmod": "2021-08-09"
}

## Kas yra MMF failas?

MMF yra failo plėtinys, susietas su SMAF failu. MMF reiškia mobilųjį muzikos failą, o SMAF reiškia sintetinės muzikos mobiliosios programos formatą. Išmaniajame telefone esančiuose MMF failuose yra sistemos skambėjimo tonų, garso, taip pat gali būti grafika ir teksto ekranas. PRF taip pat yra trijų tipų instrumentų parametrai, įskaitant FM, PCM ir srauto PCM. Šie failų formatai yra suderinami su Windows sistemos platforma. PMF failai priskiriami duomenų failų kategorijai. Paprastai Microsoft Mail palaiko MMF failus. Failas su MMF priesaga gali būti nukopijuotas į bet kurį mobilųjį įrenginį ar sistemos platformą.

Be to, šie failai yra daug mažesni, palyginti su standartiniais MIDI formato failais. [WAV](/audio/wav/) ir [MID](/audio/mid/) failus galima konvertuoti į MMF formatą, kurį vėliau galima bendrinti ir platinti kaip garso turinį. Šiuos failus galima gauti el. paštu tiesiai į telefonus ir kompiuterį.


## Trumpa MMF failo formato istorija

Yamaha sukūrė SMAF įrankius kaip garso failus, kad išmanieji telefonai galėtų saugoti daugiau unikalių skambėjimo melodijų. Yamaha pristatė SMAF gamindama MA-1, MA-2, MA-3, MA-5 ir MA-7 LSI garso lustus. Visi šie formatai tapo gana pažįstami tarp mobiliųjų telefonų Rytų Azijos rinkoje 2000 m. pradžioje.

Tarptautiniu lygiu MMF formatą patvirtino Samsung. Naudodama MMF formatą, Samsung sugebėjo sukurti platų polifoninių skambėjimo melodijų asortimentą, skirtą naudoti Samsung išmaniuosiuose telefonuose.

Yamaha norėjo padaryti formatą dar populiaresnį, todėl oficialiuose Yamaha SMAF failuose paskelbė daugiau su šiuo formatu suderinamų įrankių. Su šiuo naudotojai dabar gali lengvai leisti MMF failus savo kompiuteriuose.


## MMF failo formato specifikacijos ##

PMF failai yra suskirstyti į duomenų skyrius. Kiekvienam segmentui apibūdinti naudojama priešdėlinė struktūra aplink 8 baitus.
4 baitų etiketė apima CNTI, OPDA, MSTR, MTR ir ATR. Duomenų dydis plius 8 baitai yra gabalo dydis; visas failo dydis apskaičiuojamas sudedant visus gabalų dydžius. Jei failas nebuvo pažeistas, susumuotas failo dydis turi būti toks pat kaip ir pirminės antraštės dydis.

### Antraštė ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Štai MMF failo pavyzdys:

![](../mmf.png)

## Nuorodos

* [MMF – Vikipedija](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)


