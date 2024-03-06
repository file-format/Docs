{
  "date": "2020-03-16",
  "keywords": [
"PAT fails",
"Formāts",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par PAT faila formātu un API, kas var izveidot un atvērt PAT failus.",
  "title": "PAT faila formāts",
  "linktitle": "PAT",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-pa-lvt"
}
},
  "lastmod": "2020-10-25"
}

## Kas ir PAT fails?

Fails ar paplašinājumu .pat ir CAD fails, ko izmanto AutoCAD programmatūra. Lietojumprogrammas, kas var atvērt PAT failus, izmanto šajos failos saglabāto lūku, iegūst informāciju par apgabala tekstūru/aizpildījumu. Iekļautie raksti sniedz informāciju par materiāla izskatu uzzīmētiem objektiem. PAT failus var atvērt tādās lietojumprogrammās kā Autodesk AutoCAD, CorelDRAW Graphics Suite un Ketron Software. PAT failus var pārvērst dažādos attēlu formātos, piemēram, JPG, PNG, BMP utt.

## PAT faila formāts

PAT faili ir rakstīti vienkārša teksta formātā, un tos var atvērt jebkurā teksta redaktorā. Šajos failos lūku raksti ir balstīti uz vektoru un atbilst AutoCAD dokumentācijā norādītajai sintaksei.

Visi raksti sākas punktā 0,0, paraugs tiek aprēķināts, lai aptvertu izšķilšanās robežu.

### Raksta definīcija

Visas modeļa definīcijas sastāv no šādiem laukiem:
 * Sākuma '\*
 * Nosaukums — nosaukumā nedrīkst būt atstarpes, pieturzīmes, iekavas vai slīpsvītras.
 * A description

The standard format for hatch patterns is `<\*><name><, description>`. The name and the description are separated by a comma and descriptions cannot exceed the eighty character line length. The hatch patterns are defined after this information.

### Lūku modeļu piemēri
Tālāk ir sniegts kvadrātveida raksta piemērs
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Vēl viens paralelograma modelis ir šāds.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Atsauces Nr.

 * [Autodesk jaucējkrāni](https://help.autodesk.com/view/ACDLT/2018/ENU/?guid=GUID-A6F2E6FF-1717-44B6-A476-0CA817ADD77E)

