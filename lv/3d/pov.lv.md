
{
  "date": "2023-01-05",
  "keywords": [
"pov fails",
"pov faila formāts",
"kas ir pov fails",
"failu",
"pov piemērs",
"pov faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par POV failu formātu un API, kas var atvērt un izveidot POV failus.",
  "title": "POV — redzes faila noturība",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-lvv"
}
},
  "lastmod": "2023-01-05"
}

## Kas ir POV fails?

POV fails ir vienkārša teksta fails, kurā ir norādījumi par POV-Ray staru izsekošanas programmatūru. Šīs instrukcijas ir rakstītas īpašā skriptu valodā, kas ir raksturīga POV-Ray. Tas norāda renderējamo ainu, tostarp 3D objektus, materiālus, apgaismojumu un citas īpašības, kas nosaka ainas izskatu. POV faili izmanto īpašu skriptu valodu, kas ir raksturīga POV-Ray un ko var izmantot, lai izveidotu sarežģītas un detalizētas 3D ainas. POV faila faila paplašinājums parasti ir .pov vai .povray. Atverot POV failu programmā POV-Ray, programmatūra nolasa failā esošās instrukcijas un izmanto tās, lai ģenerētu ainas attēlu.

Mākslinieki un dizaineri bieži izmanto .pov failus, lai izveidotu 3D grafiku un animācijas dažādām lietojumprogrammām, tostarp filmām, televīzijai, videospēlēm un mārketinga materiāliem.

## POV faila formāts

**.pov fails** parasti sākas ar virkni **#include** priekšrakstu, kas tiek izmantoti, lai iekļautu iepriekš definētu krāsu, faktūru un citu resursu bibliotēkas, ko var izmantot ainā. Pēc tam fails definē objektus, materiālus un citas ainas īpašības, izmantojot bloku sēriju. Ir daudz citu veidu objektu, materiālu un citu rekvizītu, ko varat norādīt .pov failā, un varat izmantot cilpas un nosacījumu paziņojumus, lai izveidotu sarežģītākas un detalizētākas ainas.

## Programmatūras lietojumprogrammas POV

.pov faila formātu izmanto POV-Ray staru izsekošanas programmatūra, tāpēc galvenā lietojumprogramma .pov failu atvēršanai ir pati POV-Ray programmatūra. Jūs varat lejupielādēt jaunāko POV-Ray versiju no oficiālās vietnes https://www.povray.org/.

Papildus POV-Ray ir vairākas citas lietojumprogrammas, kas var atvērt un rediģēt .pov failus, tostarp:

- BRL-CAD: atvērtā koda 3D modelēšanas programmatūra, kas var importēt un eksportēt .pov failus
- MeshLab: 3D tīkla apstrādes programmatūra, kas var importēt un eksportēt .pov failus
- Blender: populāra atvērtā pirmkoda 3D grafikas programmatūra, kas var importēt un eksportēt .pov failus

Var būt arī citas programmatūras lietojumprogrammas, kas var atvērt arī .pov failus, tādēļ, ja nevarat atvērt .pov failu, izmantojot iepriekš minētās lietojumprogrammas, varat mēģināt izmantot failu skatītāju vai pārveidotāja rīku.

## POV piemērs

Piemēram, šeit ir .pov faila paraugs, kas definē ainu ar vienu zilu cilindru:

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

Šajā piemērā kameras bloks norāda kameras pozīciju un orientāciju ainā, bloks light_source deklarē gaismas avotu un norāda tā pozīciju un krāsu, savukārt cilindra bloks deklarē cilindra objektu un norāda tā beigu punktus, rādiuss un materiāla īpašības. Atverot šo .pov failu POV-Ray programmatūrā, tas atveidos viena zila cilindra attēlu.

## Atsauces
 * [POV-Ray — Wikipedia](https://en.wikipedia.org/wiki/POV-Ray)
 * [Dokumentācijas POV-Ray vietne](http://www.povray.org/documentation/)

