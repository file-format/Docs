{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "bestand", "extensie", "format", "Perl", "Perl-taal", "PL-bestanden", "programmeren"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over PL-bestandsindelingen en API's die PL-bestanden kunnen maken en openen.",
  "title" :"PL-bestand - Perl-scriptbestandsindeling",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## Wat is een PL-bestand?

Een bestand met de extensie .pl is een Perl-scriptbestand dat een scripttaal is. Deze worden gecompileerd en uitgevoerd met behulp van Perl Interpreter-software. Een PL-scriptbestand bevat regels code, variabelen en opmerkingen. Scripttalen zijn relatief moeilijk te
begrijpen met andere programmeerbestandsindelingen zoals [PHP](/nl/programming/php/). PL-bestanden kunnen worden gemaakt en zijn compatibel met Windows, macOS en Linux.

## Korte geschiedenis van de Perl-scripttaal

Deze taal werd voor het eerst in gebruik gehouden in 1987, dus deze bestanden kregen in dat jaar hun oorsprong. In 1989 werd de Perl 2 uitgebracht. Later is het bijgewerkt en aangepast tot de 5.35-versie, en het is de bedoeling dat de volgende versie volgend jaar wordt uitgebracht.

In elke update zijn er tools toegevoegd over de functionaliteit, prestaties en het uiterlijk van de taal en bestanden. Er zijn in deze jaren veel herzieningen geweest over de versies. Het was oorspronkelijk een eenvoudige scripttaal, maar bevat nu ook veel andere modules. Oorspronkelijk was het een heel eenvoudige taal, maar de scripts van deze taal waren vrij moeilijk te begrijpen omdat ze compact waren.

## Specificaties Perl-bestandsindeling extensie

Er zijn enkele eigenschappen of specificaties van deze programmeerbestanden, sommige zijn als volgt:

* De code in deze bestanden is in platte tekst en wordt gebruikt voor scriptontwikkeling
* Scripting van de server, het ontleden van tekst en serverbeheer zijn de belangrijkste aspecten die het script van deze taal behandelt
* Veel populaire programma's die aan deze taal zijn gekoppeld, zijn Active state Active Perl en Bare Bones BBEdit (compatibel met Mac OS)
* Deze taal wordt beschouwd als een taal op hoog niveau
* Voor Win32 moet de gebruiker mogelijk native binaire distributie van de taal installeren
* Er zijn enkele scripttools nodig om uitvoerbaar te worden in verschillende Windows Resource Kits
* Visual Studio .NET is een beroemd raamwerk voor de ontwikkeling van programmeertalen. De Active State-tool die bekend staat als Visual Perl wordt gebruikt om Perl toe te voegen aan Visual Studio
* In de bestanden beschrijft de eerste regel van de broncode de informatie van de tolk die wordt gebruikt. De PL-bestanden beginnen meestal met de regel **#!/usr/bin/perl** die uw computer vertelt dit script uit te voeren met behulp van een Perl-interpreter die op de computer is geïnstalleerd


## PL-scriptvoorbeelden

```
#!/usr/bin/perl
print "Hello, world\n";
```

Dit wordt afgedrukt

```
Hello, World
```

### Enkele regel commentaar ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Commentaar met meerdere regels ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Variabele toewijzing ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Scalaire variabele toewijzing ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Eenvoudige scalaire bewerkingen ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Referenties ##

- [Python (programmeertaal) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programmeertaal))

