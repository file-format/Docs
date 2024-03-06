{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SHSH fails — iPhone/iPod Touch SHSH Blob faila formāts",
  "description":"Uzziniet, kas ir SHSH fails.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh-lv",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Kas ir SHSH fails?

SHSH fails, kas pazīstams arī kā Signature HaSH, ir digitālais paraksts, ko Apple izmanto, lai autentificētu un pārbaudītu programmaparatūras atjauninājumus iOS ierīcēm, piemēram, iPhone, iPad un iPod.

## Atšķirība starp SHSH un SHSH2 failu formātiem

Tāpat kā SHSH2 fails, arī SHSH fails satur unikālu ierīces identifikatoru, ko sauc par ECID (Exclusive Chip ID), kā arī informāciju par ierīcē instalēto programmaparatūras versiju. Tomēr SHSH faili tika izmantoti vecākās iOS versijās (pirms iOS 10), un kopš tā laika tie ir aizstāti ar SHSH2 failiem.

## SHSH faila formāts — vairāk informācijas

SHSH faili tiek saglabāti diskā binārā faila formātā. Šī faila formāta iekšējās failu struktūras informācija nav pieejama publiski.

SHSH faili ir svarīgi lietotājiem, kuri vēlas pazemināt savas ierīces programmaparatūras versiju uz iepriekšējo versiju, kuru Apple vairs neparaksta. Saglabājot SHSH failus noteiktai programmaparatūras versijai, kad Apple to joprojām paraksta, lietotāji vēlāk var tos izmantot, lai apietu Apple paraksta verifikāciju un instalētu šo programmaparatūras versiju savā ierīcē. Šis process ir pazīstams arī kā jailbreaking.

## Atsauces

* [SHSH Blob — Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)

* [TSS Saver](https://tsssaver.1conan.com/v2/)


