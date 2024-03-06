{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SHSH2 fails — iOS SHSH Blob faila formāts",
  "description":"Uzziniet, kas ir SHSH2 fails.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2-lv",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Kas ir SHSH2 fails?

SHSH2 fails, kas pazīstams arī kā SHSH blob vai ECID SHSH, ir digitālais paraksts, ko Apple izmanto, lai autentificētu un pārbaudītu programmaparatūras atjauninājumus iOS ierīcēm, piemēram, iPhone, iPad un iPod. Tajā ir unikāls ierīces identifikators, kas pazīstams kā ECID (Exclusive Chip ID). Tajā ir arī informācija par ierīcē instalēto programmaparatūras versiju.

## SHSH2 faila formāts — vairāk informācijas

SHSH2 faili tiek saglabāti diskā binārā faila formātā, un šī faila formāta iekšējās failu struktūras informācija nav publiski pieejama.

Kad Apple ierīcē, piemēram, iPhone, iPad vai Mac, tiek instalēta jauna iOS versija, tiek ģenerēts SHSH2 fails. Šis SHSH2 fails tiek nosūtīts uz Apple serveriem, kas nolasa un pārbauda šo ciparparaksta failu. Pamatojoties uz šo informāciju, serveris atļauj vai neļauj instalēt.

Tas pats notiek, kad tiek pieprasīts atjauninājums. Kad lietotājs pieprasa savas ierīces atjauninājumu vai atjaunošanu, izmantojot iTunes vai citu programmatūru, Apple serveri pirms atjaunināšanas atļaušanas pārbaudīs, vai SHSH2 fails atbilst ierīces ECID un programmaparatūras versijai.

## Atsauces

* [SHSH Blob — Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)

* [TSS Saver](https://tsssaver.1conan.com/v2/)


