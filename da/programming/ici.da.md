{
  "date": "2021-09-13",
  "keywords": [
"ici",
"fil",
"udvidelse",
"filformat",
"ICI implementering",
"Programmeringsvejledning",
"ici eksempel",
"ICI programmeringssprog",
"moduler af ICI",
"datamodel af ICI",
"dokumentation af ICI",
"ICI sprog"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "ICI - Programmeringssprogsfil",
  "description": "Lær om ICI-filformat og API'er, der kan oprette og åbne ICI-filer.",
  "linktitle": "ICI",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ic-dai"
}
},
  "lastmod": "2021-09-13"
}

## Hvad er en ICI fil?

Et programmeringssprog til generelle formål, der fortolkes og indeholder flere funktioner såsom dynamisk indtastning sammen med de fleksible datatyper, er kendt som ICI (ikke et akronym) programmeringssprog. Det anses for at ligne sproget [Perl](/programming/pl/). Dette ICI-sprog omfatter flowkontrolkonstruktioner og indeholder også nogle operatører af C-sproget. Det er ikke et objektorienteret sprog, men nogle af funktionerne i OOP kan opnås ved en specifik arvemetode kendt som overbygninger. I lighed med [C](/programming/c) har dette ICI-programmeringssprog den samme systemgrænseflade og et standardbibliotek for indbyggede funktioner.


## Kort historie ##

I slutningen af 1980'erne blev det udviklet af Tim Long som et fortolket programmeringssprog til generelle formål. De fleste af funktionerne i dette sprog ligner C, og det kan også opnå nogle af funktionerne ved at anvende nogle specielle metoder. Dette sprog ejes som et offentligt domæne og er tilgængeligt som et gensalgbart sprog, og ingen er bundet til at nævne, hvor han fik kildekoden fra. Dokumentationen til ICI er under copyright af Canon Information System Research Australia.

## Teknisk specifikation ##

Der bruges to forskellige datatyper på dette sprog. Disse to er Primitive og Aggregate datatyper. Begge disse inkluderer forskellige udtryk i henhold til deres foruddefinerede sammensætning i sproget. Forskellige moduler såsom indlejrede og subrutiner understøttes af dette sprog. Da nogle af dens egenskaber ligner Perl, har den en streng integration med de regulære udtryk.

Sæt er begrænset til at være heterogene og indlejrede. Disse sæt understøtter almindeligt anvendte sætoperationer som f.eks. Union og Intersection osv. Det bruges mest som et sprog af hensyn til kerneimplementeringen af applikationer ejet af multinationale organisationer.

Næsten alle typer programmer kan skrives på dette sprog, og for det meste er de specifikke programmer, der involverer komplekse datastrukturer, skrevet i ICI-programmeringssproget. Ansøgninger kan involvere ICI-implementeringen på en måde, så de bør skrives i den. Funktionelle dele af applikationen kan implementeres af modulerne i ICI. Sproget i ICI ligner noget C-sprog, men datamodellen for ICI er et ret højere niveau og anderledes med typer som ordbøger (struct), sæt, dynamiske arrays, regulære udtryk og (rigtige) strenge.


## Eksempel på ICI-filformat ##

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

## Reference ##

* [ICI-programmeringssprog](http://atrn.org/ici/doc/ici.html)




