{
  "date": "2021-08-05",
  "keywords": [
"gsm",
"failą",
"pratęsimas",
"formatu",
"Garsas",
"Pasaulinė mobiliojo garso sistema",
"gsm plėtinys",
"gsm failus"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie GSM failų formatą ir API, kurios gali kurti ir atidaryti GSM failus.",
  "title": "GSM – pasaulinė mobiliojo garso failų formato sistema",
  "linktitle": "GSM",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-gs-ltm"
}
},
  "lastmod": "2021-08-05"
}

## Kas yra GSM failas?

GSM yra failo plėtinys, susietas su Global System for Mobile Audio Format Files. Failus su GSM plėtiniais galima atidaryti Linux, Windows ir Mac OS platformose. GSM failo formatas priklauso garso failų kategorijai.

GSM failas yra užkoduotas naudojant nuostolingą CBR (pastovios bitų spartos) garso glaudinimo kodeką. GSM garso failo atrankos sparta yra 8000 mėginių per sekundę, o duomenų perdavimo sparta yra apie 13 kbps. GSM failų bitų sparta užtikrina kokybę balso įrašymo metu. Be to, GSM failo formatas taip pat žinomas kaip pasaulinis standartinis formatas, naudojamas mobiliuosiuose telefonuose, o WAV failus taip pat galima lengvai užkoduoti naudojant GSM failo formatą. Bet kokias GSM failo problemas gali lengvai išspręsti pats vartotojas, nesikreipdamas į ekspertą.

Vartotojai taip pat gali konvertuoti GSM failus į [MP3](/audio/mp3/) ir [MP4](/video/mp4/) formatus.

## Trumpa GSM failo formato istorija

GSM yra garso failo formatas, sukurtas interneto telefonijai Europoje. Jį sukūrė Europos telekomunikacijų standartų institutas (ETSI), kad jis būtų naudojamas kaip 2G skaitmeninis mobilusis telefonas, naudojamas mobiliuosiuose telefonuose ir planšetiniuose kompiuteriuose. Šiandien jis naudojamas telefono pokalbių ir balso pranešimų įrašams saugoti.

## GSM failo formato specifikacijos ##

GSM darbas struktūrizuotame tinkle, kurį sudaro šie skyriai:

- **Moduliavimas**: tai įvesties duomenų transformavimo į formatą, kurį būtų galima lengvai perduoti, procesas. Perduoti duomenys demoduliuojami priėmimo gale
- **Perdavimo sparta** : GSM yra skaitmeninė sistema, kurios bitų sparta viršija 270 kbps
- **Prisijungimo dažnių diapazonas** : 933–960 MHz
- **Siuntimo dažnių diapazonas**: 890–915 MHz
– **Kanalų atstumas**: reiškia atstumą tarp gretimų užtvarų, kuris turėtų būti apie 200 kHz
- **Dvipusis atstumas**: tai tarpas tarp aukštyn ir žemyn nukreiptų dažnių, kuris turėtų būti 80 MHz.
- **Kalbos kodavimas**: GSM naudoja linijinį nuspėjamąjį kodavimą (LPC). LPC suspaudžia bitų spartą. Kai garso signalas praeina per filtrą ir imituoja balso taką. GSM koduoja kalbą 13 kbps greičiu

| Garso suspaudimo formatas | Algoritmas | Mėginių dažnis | Bitų spartos transformacija | Vėlavimas | CBR | VBR | Stereo | Daugiakanalis |
| ------------------------- | --------- | ----------- | ------------------- | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8 kHz | 5,6 kbit/s | 25 ms | Taip | Ne | Ne | Ne |
| GSM-FR | RPE-LTP | 8 kHz | 13 kbit/s | 20–30 ms | Taip | Ne | Ne | Ne |
| GSM-EFR | ACELP | 8 kHz | 12,2 kbit/s | 20–30 ms | Taip | Ne | Ne | Ne |

## Nuorodos Nr.

* [GSM – Vikipedija](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)


