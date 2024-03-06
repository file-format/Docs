{
  "date": "2021-08-17",
  "keywords": [
"udf fails",
"udf faila formātā",
"kas ir udf fails",
"failu",
"udf piemērs",
"udf faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par UDF failu formātu un API, kas var izveidot un atvērt UDF failus.",
  "title": "UDF - universālā diska formāta fails",
  "linktitle": "UDF",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-ud-lvf"
}
},
  "lastmod": "2021-08-17"
}

## Kas ir UDF fails?
Fails ar paplašinājumu .udf ir diska attēlveidošanas formāts, ko parasti izmanto failu saglabāšanai optiskajos datu nesējos; var izmantot DVD, kompaktdisku un citu optisko datu nesēju ierakstīšanai; saglabā failu kolekciju, izmantojot UDF standartā noteikto direktoriju struktūru; ļauj dzēst un modificēt failus mērķa diskā pat pēc to ierakstīšanas. Optiskās krātuves tehnoloģiju asociācija uzstādīja UDF failu sistēmu kā standartu, lai izveidotu kopēju failu sistēmu visiem optiskajiem datu nesējiem, piemēram, atkārtoti ierakstāmiem optiskajiem datu nesējiem un tikai lasāmiem datu nesējiem.

## UDF faila formāts 
UDF faila formāts ir atvērta pārdevēja neitrāla failu sistēma datoru datu glabāšanai plašam datu nesēju klāstam. To parasti izmanto DVD un jaunākiem optisko disku formātiem. Parasti programmatūra UDF failu sistēmu apgūst pakešprocesā un ieraksta to optiskajā datu nesējā vienā piegājienā. Tomēr, ierakstot paketes pārrakstāmos datu nesējos, UDF ļauj izveidot, dzēst un mainīt failus diskā līdzīgi kā vispārējas nozīmes failu sistēmās to darītu noņemamajos datu nesējos, piemēram, zibatmiņas diskos vai disketēs.
### UDF specifikācijas
UDF standarts definē šādas trīs failu sistēmas variācijas:

- **Vienkārša uzbūve**: šis ir oriģinālais formāts, kas tiek atbalstīts visās UDF versijās. Tas tika ieviests standarta pirmajā versijā, šo formātu var izmantot jebkura veida diskā, kas nodrošina nejaušu lasīšanas vai rakstīšanas piekļuvi, piemēram, DVD+RW, cietajiem diskiem un DVD-RAM datu nesējiem.
- **VAT build**: Used specifically for writing to write-once media. The VAT is an additional structure on the disc that allows packet writing; that is, remapping physical blocks when files or other data on the disc are modified or deleted. For write-once media, the entire disc is virtualized, making the write-once nature transparent for the user; the disc can be treated the same way one would treat a rewritable disc.
- **Spared (RW) build**: izmanto īpaši rakstīšanai uz pārrakstāmu datu nesēju. Tā pievieno papildu taupīšanas tabulu, lai pārvaldītu kļūdas, kas galu galā radīsies diska daļās, kas ir vairākas reizes pārrakstītas. Šī tabula saglabā nolietoto sektoru izsekošanu un pārveido tos uz strādājošiem. UDF defektu pārvaldība neattiecas uz sistēmām, kurās jau ir ieviests cits defektu pārvaldības veids, piemēram, Mount Rainier (MRW) optiskajiem diskiem vai diska kontrolleris cietajam diskam.
 



## Atsauces 

* [Windows attēlveidošanas formāts — Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)



