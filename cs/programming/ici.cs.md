{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "soubor", "rozšíření", "formát souboru", "implementace ICI", "Průvodce programováním", "příklad ici", "programovací jazyk ICI", "moduly ICI", "datový model ICI", "dokumentace ICI", "jazyk ICI" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - Programming Language File",
  "description":"Další informace o formátu souborů ICI a rozhraních API, která mohou vytvářet a otevírat soubory ICI.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## Co je soubor ICI?

Programovací jazyk pro všeobecné použití, který je interpretován a obsahuje několik funkcí, jako je dynamické psaní spolu s flexibilními datovými typy, je známý jako programovací jazyk ICI (není zkratka). Je považován za podobný jazyku [Perl](/cs/programming/pl/). Tento jazyk ICI obsahuje konstrukce řízení toku a také obsahuje některé operátory jazyka C. Nejedná se o objektově orientovaný jazyk, ale některé vlastnosti OOP lze dosáhnout specifickou metodou dědičnosti známou jako nadstavby. Podobně jako [C](/cs/programming/c) má tento programovací jazyk ICI stejné systémové rozhraní a standardní knihovnu pro vestavěné funkce.


## Stručná historie ##

Na konci 80. let jej vyvinul Tim Long jako univerzální interpretovaný programovací jazyk. Většina funkcí tohoto jazyka je podobná jazyku C a může také dosáhnout některých funkcí použitím některých speciálních metod. Tento jazyk je vlastněn jako veřejná doména a je k dispozici jako znovu prodejný jazyk a nikdo není povinen zmínit, odkud získal zdrojový kód. Dokumentace ICI je chráněna autorským právem společnosti Canon Information System Research Australia.

## Technická specifikace ##

V tomto jazyce se používají dva různé datové typy. Tyto dva typy dat jsou primitivní a agregované. Oba zahrnují různé výrazy podle jejich předem definovaného složení v jazyce. Tento jazyk podporuje různé moduly, jako jsou vnořené a podprogramy. Protože některé jeho vlastnosti jsou podobné Perlu, má přísnou integraci s regulárními výrazy.

Množiny jsou omezeny na to, že jsou heterogenní a vnořené. Tyto sady poskytují podporu pro běžně používané operace množin, jako je Union a Intersection atd. Většinou se používá jako jazyk pro implementaci jádra pro aplikace vlastněné nadnárodními organizacemi.

V tomto jazyce lze psát téměř všechny typy programů a většinou specifické programy, které zahrnují složité datové struktury, jsou napsány v programovacím jazyce ICI. Aplikace mohou zahrnovat implementaci ICI způsobem, že by v ní měly být napsány. Funkční části aplikace mohou být implementovány moduly ICI. Jazyk ICI se trochu podobá jazyku C, ale datový model ICI je poměrně vyšší úrovně a liší se typy, jako jsou slovníky (struct), sady, dynamická pole, regulární výrazy a (skutečné) řetězce.


## Příklad formátu souboru ICI ##

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

## reference ##

* [programovací jazyk ICI](http://atrn.org/ici/doc/ici.html)



