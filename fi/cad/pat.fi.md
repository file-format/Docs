{
  "date": "2020-03-16",
  "keywords": [
"PAT tiedosto",
"Muoto",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi PAT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PAT-tiedostoja.",
  "title": "PAT tiedostomuoto",
  "linktitle": "PAT",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-pa-fit"
}
},
  "lastmod": "2020-10-25"
}

## Mikä on PAT-tiedosto?

Tiedosto, jonka pääte on .pat, on CAD-tiedosto, jota AutoCAD-ohjelmisto käyttää. Sovellukset, jotka voivat avata PAT-tiedostoja, käyttävät näihin tiedostoihin tallennettua luukkukuviota, saavat tietoa alueen tekstuurista/täytteestä. Mukana olevat kuviot antavat tietoa materiaalin ulkonäöstä piirretyissä esineissä. PAT-tiedostoja voidaan avata sovelluksissa, kuten Autodesk AutoCAD, CorelDRAW Graphics Suite ja Ketron Software. PAT-tiedostot voidaan muuntaa erilaisiin kuvamuotoihin, kuten JPG, PNG, BMP jne.

## PAT tiedostomuoto

PAT-tiedostot on kirjoitettu vain tekstimuodossa ja ne voidaan avata millä tahansa tekstieditorilla. Näiden tiedostojen luukkukuviot ovat vektoripohjaisia ja noudattavat AutoCAD-dokumentaation määrittelemää syntaksia.

Kaikki kuviot alkavat pisteestä 0,0, kuvio lasketaan kattamaan kuoriutumisrajan.

### Kuvion määritelmä

Kaikki kuvion määritelmät koostuvat seuraavista kentistä:
 * \*
 * Nimi – Nimessä ei saa olla välilyöntejä, välimerkkejä, sulkeita tai kauttaviivaa.
 * A description

The standard format for hatch patterns is `<\*><name><, description>`. The name and the description are separated by a comma and descriptions cannot exceed the eighty character line length. The hatch patterns are defined after this information.

### Esimerkkejä luukkukuvioista
Seuraavassa on esimerkki neliömäisestä kuviosta
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Toinen esimerkki, joka näyttää suuntaviivakuvion, on seuraava.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Viitteet ##

 * [Hash Patterns by Autodesk](https://help.autodesk.com/view/ACDLT/2018/ENU/?guid=GUID-A6F2E6FF-1717-44B6-A476-0CA817ADD77E)

