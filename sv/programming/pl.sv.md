{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "fil", "tillägg", "format", "Perl", "Perl-språk", "PL-filer", "programmering"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om PL-filformat och API:er som kan skapa och öppna PL-filer.",
  "title" :"PL-fil - Perl-skriptfilformat",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## Vad är PL fil?

En fil med filändelsen .pl är en Perl Script-fil som är ett skriptspråk. Dessa kompileras och körs med Perl Interpreter-programvara. En PL-skriptfil innehåller rader med kod, variabler och kommentarer. Skriptspråk är jämförelsevis svåra att
förstå till andra programmeringsfilformat som [PHP](/sv/programming/php/). PL-filer kan skapas och är kompatibla med Windows, macOS och Linux.

## Kort historia om Perl Scripting Language

Detta språk användes först 1987, så dessa filer fick sitt ursprung det året. 1989 släpptes Perl 2. Senare har den uppdaterats och modifierats upp till 5.35-versionen, och nästa version är tänkt att släppas nästa år.

I varje uppdatering har det lagts till verktyg om funktionalitet, prestanda och utseende på språket och filerna. Det har gjorts många ändringar av versionerna under dessa år. Det var ursprungligen ett grundläggande skriptspråk men nu innehåller det många andra moduler också. Ursprungligen var det ett mycket enkelt språk, men manusen på detta språk var ganska svåra att förstå eftersom de var kompakta.

## Specifikationer för Perl filformatstillägg

Det finns några egenskaper eller specifikationer för dessa programmeringsfiler, några av dem är följande:

* Koden som ingår i dessa filer är i vanligt textformat och används för skriptutveckling
* Skriptning av server, tolkning av text och serveradministration är de viktigaste aspekterna som skriptet på detta språk täcker
* Många populära program som är associerade med detta språk är Active State Active Perl och Bare Bones BBEdit (kompatibelt med Mac OS)
* Detta språk anses vara ett språk på hög nivå
* För Win32 kan användaren behöva installera inbyggd binär distribution av språket
* Det kräver vissa skriptverktyg för att bli körbart i olika Windows Resource Kits
* Visual Studio .NET är ett känt ramverk för utveckling av programmeringsspråk. Verktyget Active State som kallas Visual Perl används för att lägga till Perl i Visual studio
* I filerna beskriver den första raden i källkoden informationen om tolken som används. PL-filerna börjar vanligtvis med **#!/usr/bin/perl** rad som talar om för din dator att köra det här skriptet med en Perl-tolk installerad i datorn


## PL-skriptexempel

```
#!/usr/bin/perl
print "Hello, world\n";
```

Detta kommer att skrivas ut

```
Hello, World
```

### Enradskommentar ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Flerradskommentar ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Variabel tilldelning ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Skalär variabeltilldelning ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Enkla skalära operationer ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Referenser ##

- [Python (programmeringsspråk) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

