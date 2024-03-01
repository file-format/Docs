{
  "date": "2023-10-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CJS-tiedosto - CommonJS-kooditiedosto",
  "description": "Mikä on .cjs-tiedosto ja kuinka se avataan?",
  "linktitle": "CJS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cj-fis"
}
},
  "lastmod": "2023-10-26"
}

## Mikä on CJS-tiedosto?

CommonJS (CJS) -tiedosto on tiedosto, joka sisältää CommonJS-syntaksilla kirjoitetun JavaScript-koodin. CommonJS on moduulijärjestelmä, joka on suunniteltu toimimaan käyttöliittymän verkkoselaimien ulkopuolella, ja sitä käytetään usein palvelinpuolen JavaScript-ympäristöissä, kuten Node.js.

## CJS-tiedostomuoto - lisätietoja

CJS-tiedostot on kirjoitettu CommonJS-syntaksilla, ja niitä voidaan muokata missä tahansa tekstieditorissa, kuten Microsoft Notepad tai Apple TextEdit. CommonJS-moduulit tallennetaan tyypillisesti erillisiin tiedostoihin, ja ne on tarkoitettu kapseloimaan ja moduloimaan koodia paremman organisoinnin ja ylläpidettävyyden parantamiseksi. Nämä moduulit käyttävät request-funktiota riippuvuuksien tuontiin ja module.exports tai exports -objekti paljastaakseen arvoja ja toimintoja, joita koodin muut osat voivat käyttää.

### CJS-koodiesimerkki

CommonJS-moduuleilla on erityinen syntaksi ja rakenne, joka sisältää ominaisuuksia, kuten edellytystoiminnon muiden moduulien tuomiseksi, ja module.exports tai vie objekteja arvojen, funktioiden tai objektien viemiseksi moduulista. Näitä moduuleja käytetään koodin osien kapseloimiseen ja erottamiseen, mikä helpottaa suurten JavaScript-koodikantojen hallintaa ja ylläpitoa. Tässä on perusesimerkki CommonJS-moduulista:

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

## Viitteet

* [Visual Studion suunnittelukurssit](https://en.wikipedia.org/wiki/CommonJS)


