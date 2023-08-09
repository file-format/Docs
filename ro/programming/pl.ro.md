{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "fișier", "extensie", "format", "Perl", "limbaj Perl", "fișiere PL", "programare"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier PL și despre API-urile care pot crea și deschide fișiere PL.",
  "title" :"Fișier PL - Format de fișier script Perl",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## Ce este un fișier PL?

Un fișier cu extensia .pl este un fișier Perl Script care este un limbaj de scripting. Acestea sunt compilate și rulate folosind software-ul Perl Interpreter. Un fișier script PL conține linii de cod, variabile și comentarii. Limbajele de scriptare sunt relativ dificil de utilizat
înțelegeți alte formate de fișiere de programare, cum ar fi [PHP](/ro/programming/php/). Fișierele PL pot fi create și sunt compatibile cu Windows, macOS și Linux.

## Scurt istoric al limbajului de scriptare Perl

Acest limbaj a fost folosit pentru prima dată în 1987, astfel încât aceste fișiere și-au luat originea în acel an. În 1989 a fost lansat Perl 2. Mai târziu, acesta a fost actualizat și a fost modificat până la versiunea 5.35, iar următoarea versiune urmează să fie lansată anul viitor.

În fiecare actualizare, au fost adăugate instrumente despre funcționalitatea, performanța și aspectul limbii și fișierelor. Au fost multe revizuiri ale versiunilor în acești ani. Inițial a fost un limbaj de scripting de bază, dar acum cuprinde și multe alte module. Inițial, era un limbaj foarte simplu, dar scripturile acestui limbaj erau destul de greu de înțeles deoarece erau compacte.

## Specificații de extensie a formatului de fișier Perl

Există unele proprietăți sau specificații ale acestor fișiere de programare, unele dintre ele sunt după cum urmează:

* Codul inclus în aceste fișiere este în format text simplu și este folosit pentru dezvoltarea scripturilor
* Scriptarea serverului, analizarea textului și administrarea serverului sunt principalele aspecte pe care le acoperă scriptul acestui limbaj
* Multe programe populare care sunt asociate cu acest limbaj sunt Active State Active Perl și Bare Bones BBEdit (compatibil cu Mac OS)
* Această limbă este considerată o limbă de nivel înalt
* Pentru Win32, utilizatorul poate fi nevoit să instaleze distribuția binară nativă a limbii
* Este nevoie de unele instrumente de scripting pentru a deveni executabile în diferite kituri de resurse Windows
* Visual Studio .NET este un cadru faimos pentru dezvoltarea limbajelor de programare. Instrumentul Active State cunoscut sub numele de Visual Perl este folosit pentru a adăuga Perl în Visual Studio
* În fișiere, prima linie a codului sursă descrie informațiile interpretului utilizat. Fișierele PL încep de obicei cu linia **#!/usr/bin/perl** care spune computerului să ruleze acest script folosind un interpret Perl instalat în computer


## Exemple de script PL

```
#!/usr/bin/perl
print "Hello, world\n";
```

Aceasta se va imprima

```
Hello, World
```

### Comentariu pe un singur rând ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Comentariu pe mai multe rânduri ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Atribuire variabile ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Alocarea variabilelor scalare ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Operații scalare simple ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Referințe ##

- [Python (limbaj de programare) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

