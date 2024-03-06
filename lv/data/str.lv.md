{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "STR fails — dBASE struktūras saraksta objekta fails — kas ir .str fails un kā to atvērt?",
  "description" : "Uzziniet par STR dBASE struktūras saraksta objektu failu un to, kā to atvērt.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-lv",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Kas ir STR fails?

STR faila formāts parasti tiek saistīts ar dBASE, datu bāzes pārvaldības sistēmu. Programmā dBASE .str fails parasti ir struktūras saraksta objekta fails. Šis fails satur datu bāzes tabulas struktūru, ieskaitot informāciju par laukiem (kolonnām) un to īpašībām.

Struktūras saraksta objekta fails (.str) satur metadatus, piemēram, lauku nosaukumus, datu tipus, lauku garumus un citus rekvizītus, kas saistīti ar katru lauku datu bāzes tabulā. To izmanto, lai definētu datu bāzes tabulas struktūru, nesaturot faktiskos datu ierakstus.

Programmas, piemēram, dBASE vai citi datu bāzes pārvaldības rīki, var izmantot šo failu, lai izprastu datu bāzes tabulas izkārtojumu un veiktu tādas darbības kā vaicājumi, atjaunināšana vai jaunu ierakstu izveide, pamatojoties uz šo struktūru.

Šeit ir pamata piemērs tam, ko var saturēt STR fails:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Šajā piemērā ir aprakstīta tabula ar četriem laukiem: ID, Vārds, Vecums un DOB, kā arī to attiecīgie datu veidi un garumi.

## Kā atvērt STR failu?

Galvenais veids, kā atvērt .str failus, ir izmantot pašu dBASE, īpaši Windows operētājsistēmās. dBASE spēj nolasīt un interpretēt šo failu saturu, ļaujot lietotājiem skatīt un strādāt ar datu bāzes struktūru.

Tā kā .str faili būtībā ir vienkārša teksta faili, kas satur informāciju par datu bāzes struktūru, tos var atvērt arī, izmantojot teksta redaktoru. Teksta redaktoru piemēri ir Microsoft Notepad operētājsistēmā Windows un Apple TextEdit operētājsistēmā Mac. Atverot teksta redaktorā, varēsiet redzēt faila saturu, tostarp lauku nosaukumus, datu tipus un citu strukturālo informāciju, cilvēkiem lasāmā formātā.

## Atsauces
* [dBase](https://en.wikipedia.org/wiki/DBase)


