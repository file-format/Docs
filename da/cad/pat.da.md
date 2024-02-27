{
  "date": "2020-03-16",
  "keywords": [
"PAT fil",
"Format",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om PAT-filformat og API'er, der kan oprette og åbne PAT-filer.",
  "title": "PAT filformat",
  "linktitle": "PAT",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-pa-dat"
}
},
  "lastmod": "2020-10-25"
}

## Hvad er en PAT fil?

En fil med filtypenavnet .pat er en CAD-fil, som bruges af AutoCAD-software. Programmer, der kan åbne PAT-filer, bruger det skraveringsmønster, der er gemt i disse filer, og får information om tekstur/fyldning af et område. De indeholdte mønstre giver information om udseendet af materiale til tegnede genstande. PAT-filer kan åbnes i programmer som Autodesk AutoCAD, CorelDRAW Graphics Suite og Ketron Software. PAT-filer kan konverteres til forskellige billedformater som JPG, PNG, BMP osv.

## PAT filformat

PAT-filer er skrevet i almindeligt tekstformat og kan åbnes i enhver teksteditor. Skraveringsmønstrene i disse filer er vektorbaserede og følger syntaksen skitseret af AutoCAD-dokumentationen.

Alle mønstre starter ved punktet 0,0, mønsteret er beregnet til at dække skraveringsgrænsen.

### Mønsterdefinition

Alle mønsterdefinitioner består af følgende felter:
 * En ledende '\*
 * Et navn - Navnet må ikke have mellemrum, tegnsætningstegn, parenteser eller skråstreger.
 * A description

The standard format for hatch patterns is `<\*><name><, description>`. The name and the description are separated by a comma and descriptions cannot exceed the eighty character line length. The hatch patterns are defined after this information.

### Eksempler på lugemønster
Følgende er et eksempel på kvadratisk mønster
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Et andet eksempel, der viser parallelogrammønster, er som følger.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Referencer ##

 * [Hash-mønstre fra Autodesk](https://help.autodesk.com/view/ACDLT/2018/ENU/?guid=GUID-A6F2E6FF-1717-44B6-A476-0CA817ADD77E)

