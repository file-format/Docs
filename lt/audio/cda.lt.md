{
  "date": "2021-06-09",
  "keywords": [
"cda",
"failą",
"pratęsimas",
"formatu",
"kas yra cda failas",
"muzika",
"cda failo formatas",
"cda failo formato specifikacija"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie CDA failo formatą ir API, kurios gali kurti, konvertuoti ir atidaryti CDA failus.",
  "title": "CDA – kompaktinio disko garso takelio nuorodos failas",
  "linktitle": "CDA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-cda"
}
},
  "lastmod": "2021-06-09"
}

## Kas yra CDA failas?

Failas su plėtiniu .cda yra nedidelis Microsoft Windows sugeneruotas failas kiekvienam garso takeliui garso kompaktiniame diske. Šiuose failuose yra įprasta informacija, pvz., takelio laikas ir Windows nuoroda, leidžianti vartotojams pasiekti konkrečius garso takelius. CDA failai nėra muzika, bet jie nurodo muzikos failą, esantį kažkur saugykloje. Tai galime pasakyti kaip garso failo, esančio kompaktiniame diske, nuorodą.

## CDA failo formatas

CDA failo formatas naudojamas kompiuteriui nurodyti, kurį garso failą leisti kompaktiniame diske. Taigi, CDA failai tampa nenaudingi, atskirti nuo jų atstovaujamo kompaktinio disko. CDA failai paprastai laikomi RIFF ištekliais. Dabartinėje .cda failo versijoje yra tik vienas gabalas, pavadintas CDDA ir kuriame yra tik vienas duomenų blokas, vadinamas FMT. Šis blokas yra 24 baitų ilgio. Windows sukurtą identifikatorių naudoja su Windows 95 ir Windows 98 susijęs kompaktinių diskų įrenginys, o jo grotuvas negali prisijungti prie FreeDB ar CDDB. Kad jis galėtų rodyti dainos pavadinimą ir atlikėjo pavadinimą, turite rankiniu būdu įvesti šią informaciją į failą cdplayer.ini.

### CDA failo tvarkymas

Šioje lentelėje pateikiama informacija apie tipinius poslinkius:
| kompensuoti | ilgis | turinys |
---|---|---|
| 0x00 | 4 | 4 ASCII simboliai RIFF |
| 0x04 | 4 | šio gabalo dydis: visada 36 (44–8), 4 baitai (Intel tvarka) |
| 0x08 | 4 | chunk identifier: the 4 ASCII characters "CDDA"-lt |
| 0x0C | 4 | 3 ASCII simboliai fmt ir tarpas |
| 0x10 | 4 | gabalo ilgis: visada 24, 4 baitai (Intel tvarka) |
| 0x14 | 2 | version of the CD format, on 2 bytes (Intel order). In May 2006, always equal to 1. |
| 0x016 | 2 | number of the range, on 2 bytes (Intel order). The first track has the number 1. |
| 0x18 | 4 | Windows apskaičiuotas identifikatorius cdplayer.exe. |
| 0x1c | 4 | diapazono poslinkis, kadrų skaičiumi (Intel tvarka) |
| 0x20 | 4 | takelio trukmė, bendras kadrų skaičius (Intel tvarka) |
| 0x24 | 1 | diapazono padėtis: rėmeliai |
| 0x25 | 1 | diapazono padėtis: sekundės |
| 0x26 | 1 | diapazono padėtis: minutės |
| 0x27 | 1 | nulinis baitas (dvejetainė reikšmė 0) |
| 0x28 | 1 | takelio trukmė: kadrai |
| 0x29 | 1 | trasos trukmė: sekundės |
| 0x2a | 1 | trasos trukmė: minutės |
| 0x2b | 1 | nulinis baitas (dvejetainė reikšmė 0) |

## Nuorodos

* [.cda failas – pateikė Vikipedija](https://en.wikipedia.org/wiki/.cda_file)


