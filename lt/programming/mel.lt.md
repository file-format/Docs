{
  "date": "2019-10-11",
  "keywords": [
".mel",
"Maya įterptoji kalba",
"failą",
"pratęsimas",
"Dokumento formatas",
"Maya 3D",
"Programavimo vadovas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MEL – Maya įterptosios kalbos failo formatas",
  "description": "Sužinokite apie MEL failo formatą ir API, kurios gali kurti ir atidaryti MEL failus.",
  "linktitle": "MEL",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-me-ltl"
}
},
  "lastmod": "2021-03-08"
}

## Kas yra MEL failas?

Failas su plėtiniu .mel (Maya Embedded Language) yra scenarijų kalba, kurią Autodesk Maya naudoja grafinėms sąsajoms kurti. Tai leidžia automatizuoti grafinių elementų kūrimą naudojant vykdomuosius scenarijus, be Maya grafinės sąsajos. MEL suteikia galimybę kurti grafines sąsajas nemokant programavimo. Tai pasiekiama kuriant makrokomandas ir pasirinktinius veiksmus, kurie pagreitina pasikartojančias užduotis. Šios procedūros ir scenarijai leidžia kurti pasirinktinį modeliavimą, animaciją, dinamiką ir užduočių atvaizdavimą. Autodesk Maya 2020 galima naudoti norint atidaryti ir peržiūrėti EML failo turinį.

## MEL failo formatas – daugiau informacijos

Programuotojo [reference manual](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) kūrėjams prieinama Maya dokumentacijos skiltyje. MEL yra pagrįsta apvalkalo scenarijų komandomis, panašiomis į UINX, kad būtų pasiekti dalykai. Dėl komandų, pagrįstų scenarijais, ji nėra svarbi įprastiniam ir objektiniam programavimui (OOP), todėl nenaudojamos duomenų struktūros, iškviečiamos funkcijos arba nenaudojamas OOP, kaip ir kitomis kalbomis.

Toliau pateikiami keli pagrindiniai klausimai apie MEL.

Komentarai – kiekvienas MEL teiginys turi baigtis kabliataškiu (;), net ir bloko pabaigoje.

Grąžinamos reikšmės – nurodant reiškinį, kuris grąžina reikšmę, reikšmė MEL automatiškai neatspausdinama. Vietoj to tai sukelia klaidą.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
Kurimo, redagavimo ir ištrynimo komandos – ta pati komanda naudojama daiktams kurti, redaguoti arba informacijos apie esamus dalykus užklausti. Tačiau vėliavėlė valdo, ką komanda atlieka (kurti, redaguoti ar pateikti užklausą).

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
Return Value from Function – funkcijos sintaksė automatiškai grąžina reikšmę. Norėdami gauti grįžtamąją reikšmę naudodami komandos sintaksę, komandą turite įdėti į kabutes.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Nuorodos

 * [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

