{
  "date": "2023-10-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Comhad CJS - Comhad Cóid CommonJS",
  "description": "Cad is comhad .cjs ann agus conas é a oscailt?",
  "linktitle": "CJS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cj-gas"
}
},
  "lastmod": "2023-10-26"
}

## Cad is comhad CJS ann?

Is comhad é comhad CommonJS (CJS) ina bhfuil cód JavaScript scríofa i gcomhréir CommonJS. Is córas modúil é CommonJS atá deartha chun oibriú i dtimpeallachtaí lasmuigh de bhrabhsálaithe gréasáin frontend, agus is minic a úsáidtear é i dtimpeallachtaí JavaScript ar thaobh an fhreastalaí, cosúil le Node.js.

## Formáid Chomhaid CJS - Tuilleadh Eolais

Tá comhaid CJS scríofa i gcomhréir CommonJS agus is féidir iad a chur in eagar in aon eagarthóir téacs ar nós Microsoft Notepad nó Apple TextEdit. Go hiondúil déantar modúil CommonJS a stóráil i gcomhaid ar leith agus tá siad ceaptha chun cód a chuimsiú agus a mhodúlú le haghaidh eagrúcháin agus cothabhála níos fearr. Úsáideann na modúil seo an fheidhm riachtanach chun spleáchais a allmhairiú agus cuireann an modúl.exports nó onnmhairí réad chun luachanna agus feidhmeanna a nochtadh is féidir le codanna eile den chód a úsáid.

### Sampla Cód CJS

Tá comhréir agus struchtúr ar leith ag modúil CommonJS a áiríonn gnéithe mar an fheidhm a éilíonn chun modúil eile a allmhairiú agus an modúl.onnmhairíonn nó onnmhairíonn rudaí chun luachanna, feidhmeanna nó réada ó mhodúl a onnmhairiú. Úsáidtear na modúil seo chun píosaí cód a chuimsiú agus a scaradh, rud a fhágann go bhfuil sé níos éasca bunchóid mhóra JavaScript a bhainistiú agus a chothabháil. Seo sampla bunúsach de mhodúl CommonJS:

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

## Tagairtí

* [Ranganna Dearaidh sa Stiúideo Amharc](https://en.wikipedia.org/wiki/CommonJS)


