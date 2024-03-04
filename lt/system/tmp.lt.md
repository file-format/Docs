{
  "date": "2021-07-15",
  "keywords": [
"TMP",
"pratęsimas",
"failą",
"formatu",
"sistema",
"TMP failą",
"TMP dokumentai",
"TMP failai",
"Laikinasis failas",
"taikymas",
"programas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "TMP – laikinas failo formatas",
  "description": "Sužinokite apie TMP failo formatą ir API, kurios gali kurti ir atidaryti TMP failus.",
  "linktitle": "TMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-tm-ltp"
}
},
  "lastmod": "2021-07-15"
}

## Kas yra TMP failas? ##

TMP failas reiškia laikiną atsarginę kopiją, saugyklą ar kitą failų sistemą, sukurtą programinės įrangos programos. Jis kartais sukuriamas kaip nematomas failas ir dažnai sunaikinamas, kai programa uždaroma. TMP failai taip pat gali būti naudojami laikinai saugoti informaciją, kol kuriamas naujas failas.

## TMP failo formatas ##

TMP failą paprastai sudaro neapdoroti duomenys, kurie naudojami kaip medžiagos konvertavimo iš vieno stiliaus į kitą proceso fazė. Microsoft Word ir Apple Safari yra dvi programos, kurios gali sukurti ir naudoti TMP failo formatą.

Sugeneruoti TMP dokumentai teoriškai turėtų būti automatiškai pašalinti, kai programa uždaroma arba įrenginys išjungiamas. Praktiškai tai ne visada būna. Todėl naršydami programos dokumentus galite susidurti su trumpalaikiais failais, kurių sistema ar kita programinė įranga aktyviai nenaudoja.

### Pagalbinė atmintis ###

Virtualioji atmintis naudojama operacinėse sistemose, tačiau programoms, kurios naudoja didžiulius informacijos kiekius, gali tekti sukurti laikinus dokumentus.

### Bendravimas tarp procesų ###

Daugumoje operacinių sistemų yra primityvūs duomenų perdavimo tarp programų, pvz., vamzdžiai, lizdai ar pagrindinė atmintis, primityviai, tačiau paprasčiausias būdas yra perkelti failus į laikinąjį failą ir informuoti priimančiąją programą apie laikinojo failo vietą.


## Techninė specifikacija Nr.

Išskirtinius laikinus dokumentų pavadinimus paprastai suteikia operacinės sistemos ir programinės įrangos programos.
Laikinus failus galima saugiai generuoti POSIX sistemose naudojant mkstemp arba tmpfile bibliotekos funkcijas. Kai kuriose sistemose yra ankstesnė POSIX (nuo to laiko) mktemp programa. Šie failai paprastai randami įprastame laikinajame kataloge Unix platformose /TMP arba %TEMP% (tai būdinga prisijungimui) Windows kompiuteriuose.

Kai programa sustoja arba dokumentas uždaromas, trumpalaikis failas, sukurtas naudojant tmpfile, automatiškai pašalinamas. GetTempFileName (Windows) arba tmpnam (POSIX) galima naudoti norint sukurti laikiną failo pavadinimą, kuris truks ilgiau nei jį sukūrusios programos.

## Nuoroda ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
