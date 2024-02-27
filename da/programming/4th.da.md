
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "4. fil - Forth Language File Format",
  "description":"Lær om, hvad .4. filformat er med eksempler og API'er, der kan oprette og åbne 4. filer.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th-da",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Hvad er en 4. fil?

En fil med filtypenavnet .4. er en programmeringsfil oprettet til **Fjerde programmeringssprog**. Den indeholder kildekode til programmer skrevet i programmeringssproget Forth og genererer output, når programmet køres. Det er bare endnu en programmeringssprogsfil, der ligner [C](/programming/c/) og [C++](/programming/cpp/) kildefil.

## 4. filformat - flere oplysninger


### Eksempel på 4. programmeringssprogkode

Her er et eksempel på et simpelt program skrevet i Forth, der beregner fakultetet af et givet tal:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

In this example, the factorial word takes a single argument n and returns its factorial. The dup word duplicates the value on top of the stack, drop discards the value on top of the stack, and * gange de to værdier på toppen af stakken. Hvis og start/til-konstruktionerne styrer programmets flow.

For at bruge dette program skal du indtaste definitionen i Forth-fortolkeren og derefter kalde det faktorielle ord med det nummer, du ønsker at finde fakultetet af:

```
10 factorial .
```
Dette ville resultere i output 3628800, som er faktoren på 10.

## Referencer

 * [Forth Programming Language](https://en.wikipedia.org/wiki/Forth_(programming_language))

