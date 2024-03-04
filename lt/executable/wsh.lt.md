{
  "date": "2021-08-27",
  "keywords": [
"wsh failą",
"wsh failo formatas",
"kas yra wsh failas",
"failą",
"wsh pavyzdys",
"wsh failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie WSH failo formatą ir API, kurios gali kurti ir atidaryti WSH failus.",
  "title": "WSH – „Windows“ scenarijaus failas",
  "linktitle": "WSH",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ws-lth"
}
},
  "lastmod": "2021-08-27"
}

## Kas yra WSH failas?
Failas su plėtiniu .wsh turi tam tikros programavimo kalbos scenarijaus, pvz., VB arba VBS, ypatybes ir parametrus. Tikrasis WSH poreikis yra naudoti juos tam tikrų scenarijų vykdymui pritaikyti. Norint paleisti, reikia WScript arba CScript, ir jie abu yra įtraukti į Windows operacinę sistemą. WSH failai iš pradžių buvo pateikti Windows 95 diegimo diskuose kaip pasirenkamas konfigūruojamas ir įdiegiamas valdymo skydelyje, o vėliau kaip numatytasis Windows 98 komponentas.

## WSH failo formatas
WSH (Windows Script Host) gali būti naudojamas įvairiems tikslams, įskaitant administravimą, prisijungimo scenarijus ir bendrą automatizavimą. WSH sukuria scenarijų paleidimo aplinką. jis iškviečia tinkamą scenarijaus variklį ir paskiria paslaugų bei objektų rinkinį, su kuriuo scenarijus galėtų dirbti. Šiuos scenarijus galima paleisti GUI režimu, iš COM objekto arba komandinės eilutės režimo, suteikiant vartotojui lankstumo tiek interaktyviems, tiek neinteraktyviems scenarijus.

### Pavyzdžiai
Čia yra labai paprastas pavyzdys, rodantis kai kuriuos VBScript, kuris naudoja šakninį WSH COM objektą WScript, kad būtų rodomas pranešimas su mygtuku Gerai. Kai šis scenarijus bus paleistas, bus iškviestas CScript arba WScript variklis ir bus sukurta vykdymo aplinka.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Nuorodos 

* [Windows Script Host – pateikė Vikipedija](https://en.wikipedia.org/wiki/Windows_Script_Host)




