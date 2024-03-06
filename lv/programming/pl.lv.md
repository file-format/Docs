{
  "date": "2021-07-23",
  "keywords": [
"PL",
"failu",
"pagarinājumu",
"formātā",
"Perl",
"Perl valoda",
"PL faili",
"programmēšana"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par PL faila formātu un API, kas var izveidot un atvērt PL failus.",
  "title": "PL fails — Perl skripta faila formāts",
  "linktitle": "PL",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-p-lvl"
}
},
  "lastmod": "2021-07-23"
}

## Kas ir PL fails?

Fails ar paplašinājumu .pl ir Perl Script fails, kas ir skriptu valoda. Tie tiek apkopoti un palaisti, izmantojot Perl Interpreter programmatūru. PL skripta failā ir koda rindas, mainīgie un komentāri. Skriptu valodas ir salīdzinoši grūti lietojamas
saprast citus programmēšanas failu formātus, piemēram, [PHP](/programming/php/). PL failus var izveidot, un tie ir saderīgi ar Windows, macOS un Linux.

## Īsa Perl skriptu valodas vēsture

Šī valoda pirmo reizi tika izmantota 1987. gadā, tāpēc šie faili radās šajā gadā. 1989. gadā tika izlaists Perl 2. Vēlāk tā tika atjaunināta un pārveidota līdz 5.35 versijai, un nākamās versijas izlaišana ir paredzēta nākamajā gadā.

Katrā atjauninājumā ir pievienoti rīki par valodas un failu funkcionalitāti, veiktspēju un izskatu. Šajos gados ir veiktas daudzas versijas pārskatītas. Sākotnēji tā bija pamata skriptu valoda, taču tagad tajā ir iekļauti arī daudzi citi moduļi. Sākotnēji tā bija ļoti vienkārša valoda, taču šīs valodas raksti bija diezgan grūti saprotami, jo tie bija kompakti.

## Perl faila formāta paplašinājuma specifikācijas

Šiem programmēšanas failiem ir daži rekvizīti vai specifikācijas, daži no tiem ir šādi:

* Šajos failos iekļautais kods ir vienkārša teksta formātā un tiek izmantots skriptu izstrādei
* Servera skriptēšana, teksta parsēšana un servera administrēšana ir galvenie aspekti, ko aptver šīs valodas skripts
* Daudzas populāras programmas, kas ir saistītas ar šo valodu, ir Active State Active Perl un Bare Bones BBEdit (saderīgas ar Mac OS)
* Šī valoda tiek uzskatīta par augsta līmeņa valodu
* Win32 lietotājam, iespējams, būs jāinstalē valodas vietējais binārais sadalījums
* Ir nepieciešami daži skriptēšanas rīki, lai tie kļūtu izpildāmi dažādos Windows resursu komplektos
* Visual Studio .NET ir slavens programmēšanas valodu izstrādes ietvars. Active State rīks, kas pazīstams kā Visual Perl, tiek izmantots, lai pievienotu Perl programmai Visual Studio
* Failos avota koda pirmajā rindā ir aprakstīta izmantotā tulka informācija. PL faili parasti sākas ar rindiņu **#!/usr/bin/perl**, kas liek datoram palaist šo skriptu, izmantojot datorā instalēto Perl tulku.


## PL skriptu piemēri

```
#!/usr/bin/perl
print "Hello, world\n";
```

Tas tiks izdrukāts

```
Hello, World
```

### Vienas rindiņas komentārs ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Vairāku rindiņu komentārs ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Mainīgo piešķiršana ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Skalārā mainīgā piešķiršana ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Vienkāršas skalārās darbības ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Atsauces Nr.

- {{HIPERSAITE1}})

