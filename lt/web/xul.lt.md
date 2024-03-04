{
  "date": "2021-05-24",
  "keywords": [
"xul",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Failo plėtinys",
"XML vartotojo sąsajos kalba"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XUL – XML vartotojo sąsajos kalbos failas",
  "description": "Sužinokite apie XUL failo formatą ir API, kurios gali kurti ir atidaryti XUL failus.",
  "linktitle": "XUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xu-ltl"
}
},
  "lastmod": "2021-05-24"
}

## Kas yra XUL failas?

Failas su plėtiniu .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) reiškia XML vartotojo sąsajos kalbą) yra [XML](/web/xml/) pagrįstas žymėjimo kalbos failas, skirtas vartotojo sąsajoms kurti. Ją sukūrė Mozilla, kad kūrėjai galėtų kurti grafinės vartotojo sąsajos elementus, panašius į kitas žymėjimo kalbas, naudojamas kuriant tinklalapius. XUL plačiai naudojo Mozilla savo Firefox naršyklėje, kur naudojo Mozilla kodų bazę. XUL atvaizdavimas atliekamas naudojant
[Gecko engine](https://en.wikipedia.org/wiki/Gecko_(software)). Firefox šakutės, tokios kaip Pale Moon, Basilisk ir Waterfox, palaiko XUL priedus. XUL failai identifikuojami pagal MIME tipą: application/vnd.mozilla.xul+xml.

## XUL failo formatas

XUL failai parašyti paprastu tekstu pagal XML failo formatą ir pateikiami naudojant Gecko variklį. Trys pagrindinės XUL struktūros dalys yra:

 * Turinys – tai apima lango deklaracijas ir juose esančius vartotojo sąsajos elementus.
 * Oda – apima bet kokius stiliaus lapus, vaizdus ir kitus su tema susijusius failus. Lango išvaizda aprašyta stiliaus lapuose.
 * Lokalė – lange rodomas tekstas saugomas atskirai ir vartotojai gali naudoti kelis kalbinių failų rinkinius.

### XUL pavyzdys

Toliau pateiktame pavyzdyje sukurti trys mygtukai, kurie yra vienas ant kito vertikalia kryptimi.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Nuorodos

* [XUL – Vikipedija](https://en.wikipedia.org/wiki/XUL)

* [XUL archyvuota dokumentacija – „Mozilla“](https://wiki.mozilla.org/XUL:Home_Page)


