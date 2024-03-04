{
  "date": "2021-05-25",
  "keywords": [
"DML",
"DML failą",
"DML failo formatas",
"DML failo tipas",
"failą",
"tipo",
"kas yra DML failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DML – DynaScript HTML failas",
  "description": "Sužinokite apie DML failo formatą ir API, kurios gali kurti ir atidaryti DML failus.",
  "linktitle": "DML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-dm-ltl"
}
},
  "lastmod": "2021-05-25"
}

## Kas yra DML failas?

Failas su plėtiniu .dml yra žiniatinklio scenarijaus puslapio kodo failas, sukurtas naudojant DyanScript. DynaScript yra dinaminė [HTML](/web/html/) scenarijų kalba, suderinama su ECMAScript ir teikianti daugumą tų pačių funkcijų kaip ir kita scenarijų kalba. Jis panašus į ColdFusion kodą ir Microsoft Active Server Pages (ASP) kodą. DML failus galima atidaryti ir peržiūrėti standartinėse interneto naršyklėse, panašiose į kitus HTML puslapius.

## DML failo formatas

DML failai sukuriami paprasto teksto failo formatu ir gali būti atidaromi naudojant teksto rengyklę, kad būtų galima peržiūrėti kodą. Kodo rašymas naudojant DML skriptų kalbą gali būti naudojamas dinamiškai generuoti HTML serverio priglobtuose DML puslapiuose. DynaScript sukurti iš šių kalbos elementų:


 * SCRIPT žyma – jos įterpiamos į dokumentus kaip HTML komentarai. HTML komentaras pažymėtas \
 * Literals – tai fiksuotos reikšmės DynaScript failuose. Jų pavyzdžiai yra sveikieji skaičiai, tokie kaip s 123 , 0x3F , 0123, slankiojo kablelio skaičiai, pvz., 456.789 , 3.2e-8, Būlio reikšmės, pvz., tiesa arba klaidinga, ir eilutė, pvz., Lietus Ispanijoje
 * Kintamieji – DynaScript kintamųjų nereikia apibrėžti arba priskirti jų fiksuotam duomenų tipui. Kintamasis turi turėti reikšmę prieš naudojant jį išraiškoje; kitu atveju sugeneruojamas vykdymo laikas.
 * Išraiškos – tai kintamųjų, pažodinių reikšmių, operatorių ir kitų išraiškų deriniai. Dešinė priskyrimo sakinio pusė yra išraiška.
 * Operatoriai – jie veikia pagal vieną ar daugiau išraiškų, vadinamų operandais. Tai gali būti trejopai, dvejetainiai arba vienanariai: trinariai operatoriai veikia pagal tris išraiškas, dvejetainiai operatoriai – dvi išraiškas, o vienanariai – vieną.
 * Teiginiai – šie valdo scenarijų srautą, manipuliuoja objektais ir bendrąjį programavimą. Apskritai šie teiginiai atitinka standartinę C ir Java sintaksę. Pavyzdžiai yra if-else, do-while kilpos, perjungimas, pertraukimas, tęsimas ir kt., kaip ir bet kuri kita scenarijų kalba.
* Funkcijos – Funkcijos, kaip ir bet kuri kita scenarijų kalba, leidžia vieną kartą dokumente kaip funkciją įtraukti instrukcijų rinkinį, tada kelis kartus naudoti visame dokumente (iškviečiant funkciją). „DynaScript“ taip pat palaiko funkcijas.

* Objektai – „DynaScript“ yra orientuotas į objektus ir palaiko „objektus“ bei pagrindines į objektą orientuotas inkapsuliavimo, polimorfizmo ir paveldėjimo koncepcijas.


