{
  "date": "2021-07-23",
  "keywords": [
"PL",
"fil",
"udvidelse",
"format",
"Perl",
"Perl sprog",
"PL filer",
"programmering"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om PL filformat og API'er, der kan oprette og åbne PL filer.",
  "title": "PL-fil - Perl Script-filformat",
  "linktitle": "PL",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-p-dal"
}
},
  "lastmod": "2021-07-23"
}

## Hvad er PL fil?

En fil med filtypenavnet .pl er en Perl Script-fil, der er et scriptsprog. Disse kompileres og køres ved hjælp af Perl Interpreter-software. En PL-scriptfil indeholder kodelinjer, variabler og kommentarer. Skriptsprog er forholdsvis svære at bruge
forstå andre programmeringsfilformater såsom [PHP](/programming/php/). PL-filer kan oprettes og er kompatible med Windows, macOS og Linux.

## Kort historie om Perl Scripting Language

Dette sprog blev først holdt i brug i 1987, så disse filer fik deres oprindelse i det år. I 1989 blev Perl 2 udgivet. Senere er den blevet opdateret og er blevet ændret op til 5.35-versionen, og den næste version er målrettet til at blive frigivet næste år.

I hver opdatering er der tilføjet værktøjer om sprogets og filernes funktionalitet, ydeevne og udseende. Der har været mange revisioner af versionerne i disse år. Det var oprindeligt et grundlæggende scriptsprog, men nu omfatter det også mange andre moduler. Oprindeligt var det et meget simpelt sprog, men manuskripterne til dette sprog var ret svære at forstå, da de var kompakte.

## Perl filformatudvidelsesspecifikationer

Der er nogle egenskaber eller specifikationer for disse programmeringsfiler, nogle af dem er som følger:

* Koden inkluderet i disse filer er i almindeligt tekstformat og bruges til scriptudvikling
* Scripting af server, parsing af tekst og serveradministration er de vigtigste aspekter, som scriptet på dette sprog dækker
* Mange populære programmer, der er forbundet med dette sprog, er Active State Active Perl og Bare Bones BBEdit (kompatibel med Mac OS)
* Dette sprog betragtes som et sprog på højt niveau
* For Win32 skal brugeren muligvis installere native binær distribution af sproget
* Det kræver nogle scriptværktøjer at blive eksekverbare i forskellige Windows-ressourcesæt
* Visual Studio .NET er en berømt ramme for udvikling af programmeringssprog. Active State-værktøjet kendt som Visual Perl bruges til at tilføje Perl til Visual Studio
* I filerne beskriver den første linje i kildekoden informationen om den tolk, der bruges. PL-filerne starter normalt med **#!/usr/bin/perl** linje, der fortæller din computer at køre dette script ved hjælp af en Perl-fortolker installeret på computeren


## PL script eksempler

```
#!/usr/bin/perl
print "Hello, world\n";
```

Dette udskrives

```
Hello, World
```

### Enkeltlinjekommentar ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Kommentar med flere linjer ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Variabel tildeling ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Skalær variabel tildeling ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Simple skalaroperationer ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Referencer ##

- [Python (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

