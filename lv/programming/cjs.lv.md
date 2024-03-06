{
  "date": "2023-10-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CJS fails — CommonJS koda fails",
  "description": "Kas ir .cjs fails un kā to atvērt?",
  "linktitle": "CJS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cj-lvs"
}
},
  "lastmod": "2023-10-26"
}

## Kas ir CJS fails?

CommonJS (CJS) fails ir fails, kas satur JavaScript kodu, kas rakstīts CommonJS sintaksē. CommonJS ir moduļu sistēma, kas paredzēta darbam ārpus priekšgala tīmekļa pārlūkprogrammām, un to bieži izmanto servera puses JavaScript vidēs, piemēram, Node.js.

## CJS faila formāts — vairāk informācijas

CJS faili ir rakstīti CommonJS sintaksē, un tos var rediģēt jebkurā teksta redaktorā, piemēram, Microsoft Notepad vai Apple TextEdit. CommonJS moduļi parasti tiek glabāti atsevišķos failos, un tie ir paredzēti, lai iekapsulētu un modulētu kodu labākai organizācijai un uzturēšanai. Šajos moduļos tiek izmantota prasība, lai importētu atkarības, un objekts module.exports vai Exports, lai atklātu vērtības un funkcijas, kuras var izmantot citas koda daļas.

### CJS koda piemērs

CommonJS moduļiem ir īpaša sintakse un struktūra, kas ietver tādus līdzekļus kā prasība citu moduļu importēšanai un module.exports vai eksportē objektus vērtību, funkciju vai objektu eksportēšanai no moduļa. Šie moduļi tiek izmantoti koda daļu iekapsulēšanai un atdalīšanai, tādējādi atvieglojot lielu JavaScript kodu bāzu pārvaldību un uzturēšanu. Šeit ir CommonJS moduļa pamata piemērs:

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

## Atsauces

* [Dizaina nodarbības programmā Visual Studio](https://en.wikipedia.org/wiki/CommonJS)


