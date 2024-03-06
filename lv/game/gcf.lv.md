{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Uzziniet par GCF faila formātu un API, kas var izveidot un atvērt GCF failus.",
  "title" : "GCF fails — Nadeo spēles GCF formāts",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf-lv",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## Kas ir GCF fails?

.gcf fails ir spēļu kešatmiņas fails, ko izmanto Steam spēļu platforma. Tajā ir spēļu dati, piemēram, faktūras, modeļi un citi faili, ko izmanto spēle. Šie faili tiek glabāti lietotāja datorā un tiek izmantoti, lai samazinātu lejupielādējamo datu apjomu, atjauninot vai instalējot spēli. .gcf failus var izmantot arī, lai izveidotu spēles instalācijas dublējumus vai pārsūtītu spēli starp datoriem.

GCF failus var lasīt un rakstīt atvērtā pirmkoda C++ programmēšanas bibliotēkā **HLLib**.

## GCF faila formāts

GCF faili tiek saglabāti diskā kā bināri faili. Sākotnēji GCF tika izmantots kā Grid Cache File saīsinājums (Steam agrīnais koda nosaukums bija Grid), bet vēlāk tas tika pieņemts kā Game Cache File. GCF fails ir arhīva fails, kurā tiek glabātas Steam spēles. Viss oficiālais saturs tiek lejupielādēts kā GCF faili. GCF failus var arī koplietot starp spēlēm.

PIEZĪME. GCF ir [VPK file format](/game/vpk/) priekštecis.
## Atsauces

* [Valve Software](https://www.valvesoftware.com/en/)

* [GCF faila formāts](https://developer.valvesoftware.com/wiki/GCF)

* [HLLib — atvērtā pirmkoda C++ programmēšanas bibliotēka GCF failu lasīšanai](https://developer.valvesoftware.com/wiki/HLLib)


