{
  "date": "2019-10-11",
  "keywords": [
"ma",
"ma failą",
"ma failo formatas",
"Dokumento formatas",
"3d",
"ma failo atsisiuntimas",
".ma failą",
".ma"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie MA failo formatą ir API, kurios gali atidaryti ir kurti MA failus.",
  "title": "MA failo formatas",
  "linktitle": "MA",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-m-lta"
}
},
  "lastmod": "2021-06-04"
}

## Kas yra MA failas?

Failas su plėtiniu .ma yra 3D projekto failas, sukurtas naudojant Autodesk Maya programą. Jame yra didelis tekstinių komandų sąrašas, skirtas informacijai apie failą nurodyti. **.ma failą** galima atidaryti ir redaguoti bet kuriame teksto rengyklėje, kad būtų išspręstos su komandomis susijusios problemos, jei failas būtų sugadintas. Šiuose failuose yra informacija, skirta apibrėžti 3D scenos informaciją, pvz., geometriją, apšvietimą, animaciją ir atvaizdavimą.

## MA failo formatas

MA failai diske įrašomi ASCII teksto formatu, skirtingai nei MB failai, kurie diske išsaugomi dvejetainiu formatu. Išsamią MA failo formato nuorodą galima rasti [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) ir ją galima rasti kūrėjo nuorodai.

### MA failo antraštė

MA failo antraštė prasideda komentarų skyriumi, kuriame pateikiama failo sukūrimo informacija ir modifikavimo data. Maya failų skaitytuvai nepaiso šio bloko, nes jis naudojamas tik informaciniais tikslais. Tačiau antraštė turi prasidėti pirmaisiais šešiais simboliais kaip //Maya.

ASCII failo antraštė atrodo taip.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Failų nuorodos

.ma failo failų nuorodų skiltyje yra informacijos apie visus kitus Maya failus, kurie yra nurodyti šiame faile. Kiekvieną nurodytą failą galima nuskaityti naudojant vieną failo komandą, esančią tame pačiame faile. Failo komandos sintaksė, kai naudojama nuorodai, yra:

```
file -r -rpr prefixString fileName;
```
arba

```
file -r -ns nameSpace fileName
```
Čia yra eilutės pavyzdys.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Šiame pavyzdyje parodyta, kad saulės objektas, esantis faile saulė, būtų pasiekiamas šiame faile naudojant pavadinimą saulė_saulė.

### Reikalavimai

.ma failo skyrių Requirements sudaro daugybė reikalingų komandų ir pateikiama May informacija, pvz., versija ir papildinio informacija, reikalinga failams nuskaityti. Toliau pateikiamas reikalavimų skyriaus pavyzdys.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Kitame skyriuje nurodyti reikalavimai. Tai susideda iš reikalingų komandų serijos. Šioje failo dalyje Maya nurodoma, kokios programinės įrangos reikia norint tinkamai įkelti failą. Tiksliau, kokia Maya versija ir kokie papildiniai.

## MA failo atsisiuntimas
Šiek tiek sunku rasti ir atsisiųsti 3D modelio MA failą. Todėl galite atsisiųsti MA failo pavyzdį iš čia:

- [Sample.ma](../sample.ma)


## Nuorodos

* [Maya ASCII failų organizavimas – Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)


