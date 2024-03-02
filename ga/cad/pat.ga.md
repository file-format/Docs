{
  "date": "2020-03-16",
  "keywords": [
"Comhad PAT",
"Formáid",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid PAT agus APIanna ar féidir leo comhaid PAT a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid PAT",
  "linktitle": "PAT",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-pa-gat"
}
},
  "lastmod": "2020-10-25"
}

## Cad is comhad PAT ann?

Is comhad CAD é comhad le síneadh .pat a úsáideann bogearraí AutoCAD. Úsáideann feidhmchláir ar féidir leo comhaid PAT a oscailt an patrún gorlainne atá stóráilte sna comhaid seo faisnéis a fháil faoi uigeacht/ líonadh limistéir. Tugann na patrúin atá ann eolas ar chuma an ábhair do réada tarraingthe. Is féidir comhaid PAT a oscailt in feidhmchláir mar Autodesk AutoCAD, CorelDRAW Graphics Suite, agus Ketron Software. Is féidir comhaid PAT a thiontú go formáidí íomhá éagsúla cosúil le JPG, PNG, BMP, etc.

## Formáid Chomhaid PAT

Scríobhtar comhaid PAT i bhformáid gnáth-théacs agus is féidir iad a oscailt in aon eagarthóir téacs. Tá na patrúin hatch sna comhaid seo bunaithe ar veicteoir agus leanann siad an chomhréir atá leagtha amach i gcáipéisíocht AutoCAD.

Tosaíonn na patrúin go léir ag an bpointe 0,0, ríomhtar an patrún chun an teorainn goir a chlúdach.

### Sainmhíniú Patrún

Tá na réimsí seo a leanas i ngach sainmhíniú patrún:
 * \*' chun tosaigh
 * Ainm - Ní féidir spásanna, marcanna poncaíochta, lúibíní ná slais a bheith ar an ainm.
 * A description

The standard format for hatch patterns is `<\*><name><, description>`. The name and the description are separated by a comma and descriptions cannot exceed the eighty character line length. The hatch patterns are defined after this information.

### Samplaí Hatch Patrún
Seo a leanas sampla de phatrún cearnach
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Seo a leanas sampla eile a léiríonn patrún comhthreomharáin.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Tagairtí ##

 * [Patrúin Hash le Autodesk](https://help.autodesk.com/view/ACDLT/2018/ENU/?guid=GUID-A6F2E6FF-1717-44B6-A476-0CA817ADD77E)

