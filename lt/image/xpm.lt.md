{
  "date": "2019-10-11",
  "keywords": [
"xpm failą",
"xpm failo formatas",
"kas yra xpm failas",
"failą",
"xpm pavyzdys",
"xpm failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XPM – X PixMap failo formatas",
  "description": "Sužinokite apie XPM failo formatą ir API, kurios gali kurti ir atidaryti XPM failus.",
  "linktitle": "XPM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-xp-ltm"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra XPM failas?

Failas su plėtiniu .xpm yra vaizdo failo formatas, kurį naudojo X Windows sistema. Jis palaiko skaidrius pikselius ir paprastai yra skirtas piktogramų pikselių kūrimui. Jis palaiko nespalvotus, gražaus mastelio ir spalvotus pixmap duomenis. Jie buvo sukurti taip, kad juos būtų galima redaguoti rankiniu būdu, ir juos galima įtraukti į [C](/programming/c/) kodą. Šiuo tikslu XPM failai yra paprasto teksto failo formatu ir atitinka C programavimo kalbos sintaksę. XPM failus galima atidaryti naudojant įvairias vaizdų peržiūros programas, pvz
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView ir Canvas X.

## XPM failo formatas

XPM failo formatas naudoja C sintaksę, kad jie būtų integruoti į C ir C++ programas. Jį sudaro šeši skirtingi skyriai.

 * \<Values>
 * \<Colors>
 * \<Pixels>
 * \<Extensions>

Skyriai iš tikrųjų yra eilučių masyvas, kaip nurodyta toliau.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Toliau pateikiama išsami informacija apie kiekvieną skyrių.

`<Values> ` – Ši sekcija yra eilutė, kurioje yra keturi arba šeši sveikieji skaičiai, esantys 10 bazėje ir atitinkantys:

 * pixmap plotis ir aukštis
 * Spalvų skaičius
 * simbolių skaičius pikselyje
 * pasirenkamos viešosios interneto prieigos taško koordinatės ir XPMEXT žyma

`<Colors> ` – Šiame skyriuje yra tiek eilučių, kiek yra spalvų. Kiekviena eilutė yra tokia:

```
<chars>{<key><color> }+
```
`<Pixels> ` – šią skiltį sudaro<height> stygos ir<width> \*<chars_per_pixel> personažai. kas<chars_per_pixel> ilgio eilutė turi būti viena iš anksčiau nustatytų grupių<Colors> skyrius.

`<Extension> ` - Plėtinio skiltis turi būti pažymėta, jei ji nėra tuščia<Values> skyrius. Jį gali sudaryti keletas<Extension> poskyriai, kurie gali būti šių dviejų tipų:

 * viena atskira eilutė, sudaryta taip: XPMEXT<extension-name><extension-data>
 * arba blokas, sudarytas iš kelių eilučių: XPMEXT<extension-name><related extension-data composed of several strings>

## Nuorodos

* [XPM – Vikipedija](https://en.wikipedia.org/wiki/X_PixMap)

* [XPM vadovas](http://www.xfree86.org/current/xpm.pdf)


