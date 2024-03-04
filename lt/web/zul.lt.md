{
  "date": "2021-05-24",
  "keywords": [
"zul",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Failo plėtinys",
"atviras"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZUL – ZK vartotojo sąsajos failas",
  "description": "Sužinokite apie ZUL failo formatą ir API, kurios gali kurti ir atidaryti ZUL failus.",
  "linktitle": "ZUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-zu-ltl"
}
},
  "lastmod": "2021-05-24"
}

## Kas yra ZUL failas?

Failas su plėtiniu .zul yra žiniatinklio failas, sukurtas naudojant vartotojo sąsajos žymėjimo kalbą (ZUML) ir kuriame yra vartotojo sąsajos elementų apibrėžimai. Ajax ir Java klasės palaiko naudojant [XML](/web/xml/) pagrįstą ZUML serverio pusės failams kurti. ZUL failo formatą sukūrė ZK – vartotojo sąsajos sistemą, kuri leidžia kurti žiniatinklio ir mobiliąsias programas nežinant JavaScript ar AJAX.

## ZUL failo formatas

ZUL files are XML-based, consisting of different elements to construct user interface. The ZK loader uses each XML element to create a component. The overall processing of the page elements such as page title, description, etc. are described by each XML processing instruction of ZUML.

### ZUL pavyzdys

Toliau pateiktame ZUML kodo pavyzdyje pirmoji eilutė nurodo puslapio pavadinimą, antroji eilutė sukuria šakninį komponentą su pavadinimu ir kraštine, o trečioje eilutėje sukuriamas mygtukas su etikete ir įvykių klausytojas.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
ZUL schemą galima atsisiųsti iš https://www.zkoss.org/2005/zul/zul.xsd.
## Nuorodos

* [ZUL – ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)

* [ZUL schema](https://www.zkoss.org/2005/zul/zul.xsd)


