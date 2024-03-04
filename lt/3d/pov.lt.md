
{
  "date": "2023-01-05",
  "keywords": [
"pov failas",
"pov failo formatas",
"kas yra pov failas",
"failą",
"pov pavyzdys",
"pov failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie POV failo formatą ir API, kurios gali atidaryti ir kurti POV failus.",
  "title": "POV – regėjimo failas",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-ltv"
}
},
  "lastmod": "2023-01-05"
}

## Kas yra POV failas?

POV failas yra paprasto teksto failas, kuriame yra POV-Ray spindulių sekimo programinės įrangos instrukcijos. Šios instrukcijos parašytos specialia skriptų kalba, kuri būdinga POV-Ray. Jis nurodo atvaizduojamą sceną, įskaitant 3D objektus, medžiagas, apšvietimą ir kitas ypatybes, kurios apibrėžia scenos išvaizdą. POV failai naudoja specialią scenarijų kalbą, kuri yra būdinga POV-Ray ir gali būti naudojama sudėtingoms ir išsamioms 3D scenoms kurti. POV failo plėtinys paprastai yra .pov arba .povray. Kai atidarote POV failą POV-Ray, programinė įranga nuskaito faile esančias instrukcijas ir naudoja jas, kad sukurtų pateiktą scenos vaizdą.

Menininkai ir dizaineriai dažnai naudoja .pov failus kurdami 3D grafiką ir animaciją įvairioms programoms, įskaitant filmus, televiziją, vaizdo žaidimus ir rinkodaros medžiagą.

## POV failo formatas

**.pov failas** paprastai prasideda **#include** teiginiais, kurie naudojami įtraukti iš anksto nustatytų spalvų, tekstūrų ir kitų išteklių, kuriuos galima naudoti scenoje, bibliotekas. Tada failas apibrėžia objektus, medžiagas ir kitas scenos savybes, naudodamas blokų seriją. Yra daug kitų tipų objektų, medžiagų ir kitų ypatybių, kurias galite nurodyti .pov faile, taip pat galite naudoti kilpas ir sąlyginius teiginius, kad sukurtumėte sudėtingesnes ir detalesnes scenas.

## POV programinės įrangos programos

.pov failo formatą naudoja POV-Ray spindulių sekimo programinė įranga, todėl pagrindinė .pov failų atidarymo programa yra pati POV-Ray programinė įranga. Naujausią POV-Ray versiją galite atsisiųsti iš oficialios svetainės adresu https://www.povray.org/.

Be POV-Ray, yra daugybė kitų programų, kurios gali atidaryti ir redaguoti .pov failus, įskaitant:

– BRL-CAD: atvirojo kodo 3D modeliavimo programinė įranga, galinti importuoti ir eksportuoti .pov failus
- MeshLab: 3D tinklelio apdorojimo programinė įranga, galinti importuoti ir eksportuoti .pov failus
– Blender: populiari atvirojo kodo 3D grafikos programinė įranga, galinti importuoti ir eksportuoti .pov failus

Gali būti ir kitų programinės įrangos programų, kurios taip pat gali atidaryti .pov failus, todėl galbūt norėsite pabandyti naudoti failų peržiūros priemonę arba keitiklio įrankį, jei negalite atidaryti .pov failo su aukščiau nurodytomis programomis.

## POV pavyzdys

Pavyzdžiui, čia yra .pov failo pavyzdys, kuriame apibrėžiama scena su vienu mėlynu cilindru:

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

Šiame pavyzdyje kameros blokas nurodo kameros padėtį ir orientaciją scenoje, blokas light_source deklaruoja šviesos šaltinį ir nurodo jo padėtį bei spalvą, o cilindro blokas deklaruoja cilindrinį objektą ir nurodo jo galinius taškus, spindulys ir medžiagos savybės. Kai atidarysite šį .pov failą POV-Ray programinėje įrangoje, jis pateiks vieno mėlyno cilindro vaizdą.

## Nuorodos
 * [POV-Ray – Vikipedija](https://en.wikipedia.org/wiki/POV-Ray)
 * [Dokumentacijos POV-Ray svetainė] (http://www.povray.org/documentation/)

