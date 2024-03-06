{
  "date": "2021-08-27",
  "keywords": [
"wsh fails",
"wsh faila formātā",
"kas ir wsh fails",
"failu",
"wsh piemērs",
"wsh faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par WSH faila formātu un API, kas var izveidot un atvērt WSH failus.",
  "title": "WSH - Windows skripta fails",
  "linktitle": "WSH",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ws-lvh"
}
},
  "lastmod": "2021-08-27"
}

## Kas ir WSH fails?
Fails ar paplašinājumu .wsh satur rekvizītus un parametrus noteiktai programmēšanas valodas skriptam, piemēram, VB vai VBS utt. Faktiskā WSH nepieciešamība ir izmantot tos noteiktu skriptu izpildes pielāgošanai. Lai palaistu, ir nepieciešams WScript vai CScript, un tie abi ir iekļauti Windows operētājsistēmā. WSH faili sākotnēji tika nodrošināti operētājsistēmā Windows 95 instalācijas diskos kā izvēles konfigurējams un instalējams vadības panelim, un pēc tam kā Windows 98 noklusējuma komponents.

## WSH faila formāts
WSH (Windows Script Host) var izmantot dažādiem mērķiem, tostarp administrēšanai, pieteikšanās skriptiem un vispārējai automatizācijai. WSH izveido vidi skriptu palaišanai. tas izsauc piemērotu skriptu dzinēju un piešķir pakalpojumu un objektu kopu skriptam darbam. Šos skriptus var palaist GUI režīmā no COM objekta vai komandrindas režīma, nodrošinot lietotājam elastību gan interaktīviem, gan neinteraktīviem skriptiem.

### Piemēri
Šeit ir ļoti vienkāršs piemērs, kas parāda dažus VBScript, kas izmanto saknes WSH COM objektu WScript, lai parādītu ziņojumu ar pogu OK. Kad šis skripts tiks palaists, tiks izsaukts CScript vai WScript dzinējs un tiks izveidota izpildlaika vide.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Atsauces 

* [Windows Script Host — Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)




