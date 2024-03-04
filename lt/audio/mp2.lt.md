{
  "date": "2021-06-11",
  "keywords": [
"mp2",
"mp2 failą",
"pratęsimas",
"formatu",
"kas yra mp2 failas",
"muzika",
"mp2 failo formatas"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie MP2 failų formatą ir API, kurios gali kurti, konvertuoti ir atidaryti MP2 failus.",
  "title": "MP2 – MPEG Layer 2 garso failo formatas",
  "linktitle": "MP2",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mp-lt2"
}
},
  "lastmod": "2021-06-11"
}

## Kas yra MP2 failas?

MP2 failas, dar vadinamas MPA failu, yra garso failas, suspaustas naudojant MPEG-1 arba MPEG-2 II sluoksnį; nuostolingas garso glaudinimo formatas, apibrėžtas ISO/IEC 11172-3 kartu su MPEG-1 Audio Layer I ir MPEG-1 Audio Layer III ([MP3](/audio/mp3/)), siekiant sumažinti garso failo dydį. Tuo tarpu MP3 yra populiaresnis nei MP2 dėl mažesnio dydžio ir prieinamumo internete. Todėl MP2 vis dar yra gyvybiškai svarbus garso transliavimo standartas.

## MP2 failo formatas

MPEG Audio Layer II (MP2) yra pagrindinis MP3 standartų algoritmas. MPEG-1 Audio Layer 2 kodavimas buvo gautas iš MUSICAM garso kodeko. Jis prasidėjo kaip skaitmeninio garso transliavimo (DAB) projektas Vokietijoje, kaip EUREKA tyrimų programos dalis. Eureka 147 sudarė trys pagrindiniai elementai: perdavimo kodavimas ir tankinimas, COFDM moduliavimas ir MUSICAM garso kodavimas (maskavimo modelis, universalus sub-band integruotas kodavimas ir tankinimas). MUSICAM buvo vienas iš nedaugelio kodavimo būdų, galinčių pasiekti aukštą garso kokybę, kai bitų dažnis yra nuo 64 iki 192 kbit/s vienam monofoniniam kanalui. Tikslas buvo užtikrinti mažą delsą, mažą sudėtingumą, klaidų patikimumą, trumpos prieigos blokus ir atitikti techninius transliavimo, telekomunikacijų ir įrašymo skaitmeninėse laikmenose reikalavimus.

MP2 yra antrinės juostos garso kodavimo įrenginys, kurį galima suspausti laiko srityje su mažo uždelsimo filtrų banku, generuojančiu 32 dažnių srities komponentus. Palyginimui, MP3 yra transformavimo garso kodavimo įrenginys su hibridinių filtrų banku, o tai reiškia, kad dažnio srityje taikomas glaudinimas po hibridinės transformacijos iš laiko srities. MP2 kodavimo įrenginys gali išnaudoti kanalų perteklius, naudodamas pasirenkamą jungtinio stereo intensyvumo kodavimą.

### MP2 failo formato specifikacijos

MP2 failo formatas yra pagrįstas nuosekliais skaitmeniniais kadrais su 1152 atrankos intervalais su keturiais galimais formatais:

- mono formatas
- stereo formatu
- intensyvumo koduotas jungties stereo formatas (stereo nesvarbus)
- dviejų kanalų (nekoreliuotas) formatas
Kai kurios svarbios techninės MP2 specifikacijos pateiktos toliau esančioje lentelėje:

|Specifikacija| Aprašymas|
---|---|
|**Atrankos dažnis**| 32, 44,1 ir 48 kHz|
|**Bitų sparta**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 ir 384 kbit/s|
|**Papildomi diskretizavimo dažniai**|16, 22,05 ir 24 kHz|
|**Papildomi bitų sparta**|8, 16, 24, 40 ir 144 kbit/s|
|**Kelių kanalų palaikymas**|Iki 5 viso diapazono garso kanalų ir LFE kanalas (žemo dažnio stiprinimo kanalas)|

## Nuorodos Nr.

* [MPEG-1 Audio Layer II – Vikipedija](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)


