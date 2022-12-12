{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "soubor", "rozšíření", "formát", "Perl", "jazyk Perl", "soubory PL", "programování"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru PL a rozhraních API, která mohou vytvářet a otevírat soubory PL.",
  "title" :"PL File - Perl Script File Format",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## Co je soubor PL?

Soubor s příponou .pl je soubor skriptu Perl, což je skriptovací jazyk. Ty jsou kompilovány a spouštěny pomocí softwaru Perl Interpreter. Soubor skriptu PL obsahuje řádky kódu, proměnné a komentáře. Skriptovací jazyky jsou poměrně obtížné
rozumět jiným formátům programovacích souborů, jako je [PHP](/cs/programming/php/). Soubory PL lze vytvářet a jsou kompatibilní s Windows, macOS a Linux.

## Stručná historie skriptovacího jazyka Perl

Tento jazyk byl poprvé použit v roce 1987, takže tyto soubory vznikly v tomto roce. V roce 1989 vyšel Perl 2. Později byla aktualizována a upravena až na verzi 5.35 a další verze by měla být vydána příští rok.

V každé aktualizaci byly přidány nástroje týkající se funkčnosti, výkonu a vzhledu jazyka a souborů. V těchto letech došlo k mnoha revizím verzí. Původně to byl základní skriptovací jazyk, ale nyní obsahuje mnoho dalších modulů. Původně to byl velmi jednoduchý jazyk, ale písma tohoto jazyka byla poměrně složitá na pochopení, protože byla kompaktní.

## Specifikace rozšíření formátu souboru Perl

Existují některé vlastnosti nebo specifikace těchto programovacích souborů, některé z nich jsou následující:

* Kód obsažený v těchto souborech je ve formátu prostého textu a používá se pro vývoj skriptů
* Skriptování serveru, analýza textu a správa serveru jsou hlavní aspekty, které skript tohoto jazyka pokrývá
* Mnoho populárních programů, které jsou spojeny s tímto jazykem, jsou Active State Active Perl a Bare Bones BBEdit (kompatibilní s Mac OS)
* Tento jazyk je považován za jazyk na vysoké úrovni
* Pro Win32 může být nutné nainstalovat nativní binární distribuci jazyka
* Vyžaduje některé skriptovací nástroje, aby se staly spustitelnými v různých sadách Windows Resource Kit
* Visual Studio .NET je známý framework pro vývoj programovacích jazyků. Nástroj Active State známý jako Visual Perl se používá k přidání Perlu do Visual studia
* V souborech první řádek zdrojového kódu popisuje informace o použitém interpretu. Soubory PL obvykle začínají řádkem **#!/usr/bin/perl**, který říká počítači, aby spustil tento skript pomocí interpretu Perl nainstalovaného v počítači.


## Příklady skriptů PL

```
#!/usr/bin/perl
print "Hello, world\n";
```

Toto se vytiskne

```
Hello, World
```

### Jednořádkový komentář ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Víceřádkový komentář ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Přiřazení proměnné ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Přiřazení skalární proměnné ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Jednoduché skalární operace ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Reference ##

- [Python (programovací jazyk) - Wikipedie](https://en.wikipedia.org/wiki/Python_(programming_language))

