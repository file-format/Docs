{
  "date": "2023-04-20",
  "keywords": [
"ldb failą",
"kas yra ldb failas",
"kokia informacija yra ldb",
"koks yra ldb failo tikslas",
"ldb plėtinys",
"failą",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "LDB failo formatas – „Microsoft Access Lock“ failas",
  "description": "Sužinokite apie LDB formatą ir kokia informacija jame yra.",
  "linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb-lt",
      "parent": "misc"
}
},
  "lastmod": "2023-04-20"
}

## Kas yra LDB failas?

LDB failas yra užrakto failas, naudojamas Microsoft Access, kad neleistų keliems vartotojams vienu metu redaguoti tos pačios duomenų bazės. Kai vartotojas atidaro Access duomenų bazę, Access sukuria atitinkamą LDB failą tame pačiame kataloge kaip ir duomenų bazė. Šiame faile yra informacijos apie tai, kas šiuo metu naudoja duomenų bazę ir kokius įrašus jie redaguoja.

LDB failą automatiškai sukuria Microsoft Access, kai atidaroma duomenų bazė, ir ištrinama, kai duomenų bazė uždaroma. Svarbu pažymėti, kad LDB failo niekada negalima ištrinti rankiniu būdu, nes tai gali sukelti duomenų bazės problemų.

Jei kyla problemų su Microsoft Access duomenų baze, vienas iš galimų sprendimų yra pabandyti ištrinti su ta duomenų baze susietą LDB failą. Tai pašalins visus užraktus, kurie gali trukdyti jums pasiekti duomenų bazę. Tačiau prieš bandydami tai padaryti būtinai pasidarykite atsarginę duomenų bazės kopiją, nes ištrynus LDB failą gali būti prarasti arba sugadinti duomenys, jei tai daroma netinkamai.

## LDB failo formatas – daugiau informacijos

Microsoft Access LDB faile yra informacijos apie vartotojus, kurie šiuo metu pasiekia duomenų bazę, pvz., vartotojo vardą, kompiuterio pavadinimą ir prisijungimo laiką. LDB faile taip pat yra informacijos apie visus užraktus, kurie buvo patalpinti duomenų bazėje, pvz., kokius įrašus kuris vartotojas redaguoja.

Čia yra išsamesnis informacijos, kurią galima rasti LDB faile, tipų sąrašas:

- **Vartotojo vardas** - vartotojo, kuris šiuo metu pasiekia duomenų bazę, vardas
- **Kompiuterio pavadinimas** - kompiuterio, iš kurio vartotojas pasiekia duomenų bazę, pavadinimas
- **Prisijungimo laikas** - laikas, kai vartotojas pirmą kartą atidarė duomenų bazę
- **Įrašų užraktai** - informacija apie tai, kokius įrašus kuris vartotojas šiuo metu redaguoja
– **Objektų užraktai** – informacija apie tai, kokius duomenų bazės objektus (pvz., lenteles, formas ar ataskaitas) kuris vartotojas šiuo metu redaguoja
– **Ryšio informacija** – informacija apie tai, kaip vartotojas yra prisijungęs prie duomenų bazės (pavyzdžiui, ar jis naudoja vietinį ar tinklo ryšį)

LDB failo informaciją naudoja Microsoft Access, kad neleistų keliems vartotojams vienu metu atlikti prieštaringų pakeitimų toje pačioje duomenų bazėje. Kai vartotojas bando redaguoti įrašą ar objektą, kuris jau yra užrakintas kito vartotojo, Microsoft Access parodys pranešimą, nurodantį, kad objektas jau naudojamas. LDB failas atnaujinamas, kai vartotojai atidaro ir uždaro duomenų bazę bei atlieka užrakintų objektų pakeitimus.

## Nuorodos
* [What is an LDB File?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

