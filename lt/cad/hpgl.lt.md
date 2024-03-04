{
  "date": "2020-07-28",
  "keywords": [
"HPGL",
"Dokumento formatas",
"Atviras",
"Skaityti",
"Sukurti",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie HPGL failo formatą ir API, kurios gali kurti ir atidaryti HPGL failus.",
  "title": "HPGL failo formatas – mokykitės iš failų formatų ekspertų!",
  "linktitle": "HPGL",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-hpg-ltl"
}
},
  "lastmod": "2020-07-28"
}

## Kas yra HPGL failas?

HPGFL (Hewlett-Packard Graphics Language) faile yra HP sukurta braižytuvo valdymo instrukcijų rinkinys. HP braižytuvai naudoja šį failą, norėdami piešti ir spausdinti vektorinį ir rastrinį turinį ant popieriaus.

### HPGL komanda

HPGL komandą sudaro šie dalykai.
 * Dviejų simbolių abėcėlės komandų skyrius
 * Parametrų skyrius
 * Terminatoriaus skyrius

Kiekvienas failo parametras turi būti atskirtas skyrikliu, jei yra keli parametrai.

### HPGL komandos pavyzdys

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Koordinačių sistema

Koordinačių sistemas sudaro dvimačiai matavimo indikatoriai, skirti nustatyti bet kurią konkrečią vietą. Šiuo tikslu HPGL naudoja braižytuvo koordinačių ir vartotojo koordinačių sistemą.

#### Ploterio koordinačių sistema

Ši koordinačių sistema naudojama braižant brėžinius, pagrįstus braižytuvo judėjimu. Tipiškas minimalaus braižytuvo judėjimo XY vienetas yra 0,025 mm. Galimas piešimo diapazonas keičiasi naudojant braižytuvo rūšis.

#### Vartotojo koordinačių sistema

Vartotojo nurodytą koordinačių sistemą galima nustatyti naudojant mastelį ir kilmę. Jos konvertuojamos į braižytuvo koordinates naudojant IP komandą ir SC komandą. Braižytuvo sistemos koordinatės naudojamos pagal numatytuosius nustatymus, jei ši konversija neatliekama.

## HPGL failo formatas
HPGL failai yra ASCII (teksto failo) formatu ir prasideda keliomis sąrankos komandomis. Taip nustatomi tam tikri braižytuvo parametrai braižymui. Tipiškas HPGL failas atrodo taip.

|Komanda|Reiškia
---|---|
|IN;|inicijuoti, pradėti braižybos darbą|
|IP;|nustatykite mastelio keitimo taškus (P1 ir P2) į numatytąsias pozicijas|
|SP1;|pasirinkite 1 rašiklį|
|PU0,0;|pakelkite rašiklį aukštyn ir pereikite prie kito veiksmo pradžios taško|
|PD100,0,100,100,0,100,0,0;|nuleiskite rašiklį ir perkelkite į šias vietas (nupieškite langelį aplink puslapį)|
|PU50,50;|Rašiklis aukštyn ir pereikite prie X,Y koordinačių 50,50|
|CI25;|nubrėžkite apskritimą, kurio spindulys 25|
|SS;|pasirinkite standartinį simbolių rinkinį|
|DT*,1;|teksto skyriklį nustatykite į žvaigždutę ir nespausdinkite (1, reiškia tiesa)|
|PU20,80;|pakelkite rašiklį ir perkelkite į 20,80|
|LBHello World*;|nupieškite etiketę|

## Nuorodos
 * [HPGL, Vikipedija](https://en.wikipedia.org/wiki/HP-GL)
 * [HPGL informacinis vadovas](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

