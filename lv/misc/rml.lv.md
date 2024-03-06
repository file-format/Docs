{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "RML — Elixir atskaites veidnes fails",
  "description":"Uzziniet par RML failiem un API, kas var izveidot un atvērt RML failus.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml-lv",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Kas ir RML fails?

RML fails ir atskaites veidnes fails ar [Elixir Repertoire](https://elixirtech.com/repertoire-2/) ziņošanas programmu. Veidnes fails tiek izmantots, lai ģenerētu pārskatus ar datu avotu, kas ir savienots ar Elixir FileSystem. Dati tiek nolasīti un aizpildīti RML veidnes failā, un tos var eksportēt uz vairākiem dažādiem failu formātiem, piemēram, [PDF](/pdf/), [RTF](/word-processing/rtf/) un izklājlapu [XLS](/spreadsheet/xls/). Elixir repertuāra ziņošanas dzinēju var savienot ar dažādiem JDBC datu avotiem.

## RML faila formāts

RML faila formāta iekšējās failu struktūras informācija nav pieejama publiski. Failus ģenerē un iekšēji saglabā lietojumprogramma Elixir Repertoire, lai ģenerētu atskaites ar datiem, kas aizpildīti no pievienotajiem datu avotiem. RML veidnes fails satur no datiem ģenerējamā gala pārskata vispārējo izkārtojumu un vietturu informāciju.

## Kā izveidot RML veidnes failu?

Lai ģenerētu RML veidni Elixir repertuārā, var veikt šādas darbības.

1. Pievienojiet JDBC datu avotu failu sistēmai.
1. Palaidiet atskaites veidnes vedni
1. Izmantojiet programmatūru, lai atrastu datu avota .ds failu
1. Kā eksporta izvēli izvēlieties tabulas pārskatu
1. Atlasiet laukus, kas jāiekļauj pārskata veidnē
1. Visbeidzot, noklikšķinot uz pogas Pabeigt, First report.rml tiek pievienots krātuvei un tiek atvērts, lai parādītu cilni Izkārtojums.

## Atsauces

* [Eliksīru repertuārs](https://elixirtech.com/repertoire-2/)


