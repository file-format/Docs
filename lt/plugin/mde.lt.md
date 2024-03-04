{
  "date" : "2023-12-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MDE failas – kas yra MDE failas ir kaip jį atidaryti?",
  "description":"Sužinokite apie MDE failo formatą ir API, kurios gali kurti ir atidaryti MDE failus.",
  "linktitle" : "MDE",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-md-lte"
}
},
  "lastmod" : "2023-12-03"
}

## Kas yra MDE failas?

.MDE failas yra sudaryta Access duomenų bazės versija (.mdb arba .accdb). Kai kompiliuojate Access duomenų bazę į .MDE failą, jos nebegalima redaguoti naudojant standartinius Access projektavimo įrankius. Pagrindinis .MDE failo kūrimo tikslas yra platinti duomenų bazės programą neatskleidžiant originalaus šaltinio kodo.

## MDE failo formatas

MDE failas sukuriamas sudarant VBA kodą, formas, ataskaitas ir kitus objektus. Dėl to sukuriamas dvejetainis MDE failo formatas. Gautas .MDE failas gali būti platinamas vartotojams, kurie gali paleisti programą, bet negali keisti dizaino ar peržiūrėti pradinio kodo. MDE failas iš tikrųjų yra sukompiliuota [.MDA file](/database/mda/) versija. .MDE failų platinimas gali padėti apsaugoti intelektinę nuosavybę, nes neleidžia vartotojams pasiekti arba keisti šaltinio kodo. Tai taip pat gali pagerinti našumą, nes kodas yra kompiliuojamas ir optimizuojamas.

## Nuorodos

* [Prieigos specifikacijos] (https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [The Unofficial MDB Guide](http://jabakobob.net/mdb/)
