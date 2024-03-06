{
  "date": "2019-10-11",
  "keywords": [
".mel",
"Maya iegultā valoda",
"failu",
"pagarinājumu",
"faila formātā",
"Maija 3D",
"Programmēšanas rokasgrāmata"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MEL — Maya iegultās valodas faila formāts",
  "description": "Uzziniet par MEL faila formātu un API, kas var izveidot un atvērt MEL failus.",
  "linktitle": "MEL",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-me-lvl"
}
},
  "lastmod": "2021-03-08"
}

## Kas ir MEL fails?

Fails ar paplašinājumu .mel (Maya Embedded Language) ir skriptu valoda, ko Autodesk Maya izmanto, lai izveidotu grafiskās saskarnes. Tas ļauj automatizēt grafisko elementu izveidi, izmantojot izpildāmos skriptus papildus Maya grafiskajam interfeisam. MEL dod jums iespēju izveidot grafiskās saskarnes, neapgūstot programmēšanu. Tas tiek panākts, izveidojot makro un pielāgotas darbības, kas paātrina atkārtotus uzdevumus. Šīs procedūras un skripti ļauj izveidot pielāgotu modelēšanu, animācijas, dinamiku un uzdevumu renderēšanu. Autodesk Maya 2020 var izmantot, lai atvērtu un skatītu EML faila saturu.

## MEL faila formāts — vairāk informācijas

Programmētāja [reference manual](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) ir pieejama izstrādātājiem Maya dokumentācijas sadaļā. MEL pamatā ir čaulas skriptu komandas, kas līdzīgas UINX, lai sasniegtu lietas. Skriptu komandas padara to neatbilstošu tradicionālajai un objektorientētajai programmēšanai (OOP), kā rezultātā netiek izmantotas datu struktūras, izsaukšanas funkcijas vai OOP kā citās valodās.

Daži galvenie punkti par MEL ir šādi.

Komentāri — katram priekšrakstam MEL ir jābeidzas ar semikolu (;) pat bloka beigās.

Vērtību atgriešana — norādot izteiksmi, kas atgriež vērtību, vērtība netiek automātiski izdrukāta MEL. Tā vietā tas rada kļūdu.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Komandas izveidei, rediģēšanai un dzēšanai` — tā pati komanda tiek izmantota, lai izveidotu lietas, rediģētu lietas vai vaicātu informāciju par esošajām lietām. Tomēr karodziņš nosaka, ko (izveidot, rediģēt vai vaicāt) komanda dara.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Atgriezt vērtību no funkcijas` — funkcijas sintakse automātiski atgriež vērtību. Lai iegūtu atgriešanas vērtību, izmantojot komandas sintaksi, komanda jāiekļauj pēdiņās.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Atsauces

 * [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

