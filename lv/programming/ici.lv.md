{
  "date": "2021-09-13",
  "keywords": [
"ici",
"failu",
"pagarinājumu",
"faila formātā",
"ICI ieviešana",
"Programmēšanas rokasgrāmata",
"ici piemērs",
"ICI programmēšanas valoda",
"ICI moduļi",
"ICI datu modelis",
"ICI dokumentācija",
"ICI valoda"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "ICI — programmēšanas valodas fails",
  "description": "Uzziniet par ICI failu formātu un API, kas var izveidot un atvērt ICI failus.",
  "linktitle": "ICI",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ic-lvi"
}
},
  "lastmod": "2021-09-13"
}

## Kas ir ICI fails?

Universāla programmēšanas valoda, kas tiek interpretēta un satur vairākas funkcijas, piemēram, dinamisko rakstīšanu, kā arī elastīgus datu tipus, ir pazīstama kā ICI (nevis saīsinājums) programmēšanas valoda. Tiek uzskatīts, ka tā ir līdzīga valodai [Perl](/programming/pl/). Šī ICI valoda ietver plūsmas vadības konstrukcijas, kā arī dažus C valodas operatorus. Tā nav uz objektu orientēta valoda, bet dažas no OOP funkcijām var sasniegt, izmantojot īpašu mantošanas metodi, kas pazīstama kā virsbūves. Līdzīgi kā [C](/programming/c), šai ICI programmēšanas valodai ir tāds pats sistēmas interfeiss un standarta bibliotēka iebūvētajām funkcijām.


## Īsa vēsture ##

Astoņdesmito gadu beigās to izstrādāja Tims Longs kā vispārējas nozīmes interpretējamu programmēšanas valodu. Lielākā daļa šīs valodas funkciju ir līdzīgas C, un tā var arī sasniegt dažas funkcijas, izmantojot dažas īpašas metodes. Šī valoda pieder kā publiskam domēnam un ir pieejama kā tālākpārdodama valoda, un nevienam nav pienākums minēt, no kurienes viņš ieguvis avota kodu. Uz ICI dokumentāciju attiecas Canon Information System Research Australia autortiesības.

## Tehniskā specifikācija Nr.

Šajā valodā tiek izmantoti divi dažādi datu veidi. Šie divi ir primitīvie un apkopotie datu veidi. Abi šie izteicieni ietver dažādus izteicienus atbilstoši to iepriekš noteiktajam sastāvam valodā. Šī valoda atbalsta dažādus moduļus, piemēram, ligzdotos un apakšprogrammas. Tā kā dažas tās īpašības ir līdzīgas Perl, tai ir stingra integrācija ar regulārajām izteiksmēm.

Kopas var būt neviendabīgas un ligzdotas. Šīs kopas nodrošina atbalstu bieži lietotām kopu operācijām, piemēram, Union un Intersection utt. Tā galvenokārt tiek izmantota kā valoda daudznacionālām organizācijām piederošo lietojumprogrammu pamata ieviešanai.

Šajā valodā var rakstīt gandrīz visu veidu programmas, un galvenokārt īpašās programmas, kas ietver sarežģītas datu struktūras, tiek rakstītas ICI programmēšanas valodā. Lietojumprogrammas var ietvert ICI ieviešanu tā, lai tās tajā būtu ierakstītas. Lietojumprogrammas funkcionālās daļas var ieviest ar ICI moduļiem. ICI valoda nedaudz atgādina C valodu, bet ICI datu modelis ir diezgan augstāks līmenis un atšķiras ar tādiem veidiem kā vārdnīcas (struct), kopas, dinamiskie masīvi, regulārās izteiksmes un (reālās) virknes.


## ICI faila formāta piemērs ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Atsauce Nr.

* [ICI programmēšanas valoda](http://atrn.org/ici/doc/ici.html)




