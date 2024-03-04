{
  "date": "2023-10-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CJS failas - CommonJS kodo failas",
  "description": "Kas yra .cjs failas ir kaip jį atidaryti?",
  "linktitle": "CJS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cj-lts"
}
},
  "lastmod": "2023-10-26"
}

## Kas yra CJS failas?

CommonJS (CJS) failas yra failas, kuriame yra JavaScript kodas, parašytas CommonJS sintaksė. CommonJS yra modulinė sistema, sukurta veikti ne tik priekinėse žiniatinklio naršyklėse, bet ir dažnai naudojama serverio JavaScript aplinkose, pvz., Node.js.

## CJS failo formatas – daugiau informacijos

CJS failai parašyti CommonJS sintaksė ir gali būti redaguojami bet kuriame teksto rengyklėje, pvz., Microsoft Notepad arba Apple TextEdit. CommonJS moduliai paprastai saugomi atskiruose failuose ir yra skirti kodui įterpti ir moduliuoti, kad būtų geresnis organizavimas ir priežiūra. Šie moduliai naudoja reikalavimo funkciją, kad importuotų priklausomybes, o objektas module.exports arba exports atskleis reikšmes ir funkcijas, kurias gali naudoti kitos kodo dalys.

### CJS kodo pavyzdys

CommonJS moduliai turi specifinę sintaksę ir struktūrą, kuri apima tokias funkcijas kaip reikalavimo funkcija, skirta importuoti kitus modulius, o modulis.eksportuoja arba eksportuoja objektus, kad būtų galima eksportuoti reikšmes, funkcijas ar objektus iš modulio. Šie moduliai naudojami kodo dalims įterpti ir atskirti, kad būtų lengviau valdyti ir prižiūrėti dideles JavaScript kodų bazes. Štai pagrindinis CommonJS modulio pavyzdys:

```
// Module definition in a file named "myModule.js"
const someValue = 42;

function add(a, b) {
  return a + b;
}

module.exports = {
  someValue,
  add,
};

// Using the module in another file
const myModule = require('./myModule');
console.log(myModule.someValue); // 42
console.log(myModule.add(10, 20)); // 30
```

## Nuorodos

* [Dizaino pamokos programoje Visual Studio](https://en.wikipedia.org/wiki/CommonJS)


