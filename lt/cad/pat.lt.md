{
  "date": "2020-03-16",
  "keywords": [
"PAT failas",
"Formatas",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie PAT failo formatą ir API, kurios gali kurti ir atidaryti PAT failus.",
  "title": "PAT failo formatas",
  "linktitle": "PAT",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-pa-ltt"
}
},
  "lastmod": "2020-10-25"
}

## Kas yra PAT failas?

Failas su plėtiniu .pat yra CAD failas, kurį naudoja AutoCAD programinė įranga. Programos, kurios gali atidaryti PAT failus, naudoja šiuose failuose saugomą liuko šabloną, gauna informaciją apie srities tekstūrą / užpildymą. Pateikti raštai suteikia informacijos apie nupieštų objektų medžiagos išvaizdą. PAT failus galima atidaryti tokiose programose kaip Autodesk AutoCAD, CorelDRAW Graphics Suite ir Ketron Software. PAT failus galima konvertuoti į įvairius vaizdo formatus, tokius kaip JPG, PNG, BMP ir kt.

## PAT failo formatas

PAT failai yra parašyti paprasto teksto formatu ir gali būti atidaryti bet kuriame teksto rengyklėje. Šių failų brūkšnio šablonai yra pagrįsti vektoriais ir atitinka sintaksę, nurodytą AutoCAD dokumentacijoje.

Visi raštai prasideda taške 0,0, raštas apskaičiuojamas taip, kad apimtų perėjimo ribą.

### Šablono apibrėžimas

Visi modelio apibrėžimai susideda iš šių laukų:
 * \*
 * Vardas – pavadinime negali būti tarpų, skyrybos ženklų, skliaustų ar pasvirųjų brūkšnių.
 * A description

The standard format for hatch patterns is `<\*><name><, description>`. The name and the description are separated by a comma and descriptions cannot exceed the eighty character line length. The hatch patterns are defined after this information.

### Liukų modelio pavyzdžiai
Toliau pateikiamas kvadratinio modelio pavyzdys
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Kitas pavyzdys, rodantis lygiagretainį modelį, yra toks.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Nuorodos Nr.

 * [Autodesk maišos šablonai](https://help.autodesk.com/view/ACDLT/2018/ENU/?guid=GUID-A6F2E6FF-1717-44B6-A476-0CA817ADD77E)

