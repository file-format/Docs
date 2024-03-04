{
  "date": "2021-07-23",
  "keywords": [
"PL",
"failą",
"pratęsimas",
"formatu",
"Perl",
"Perlo kalba",
"PL failai",
"programavimas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie PL failo formatą ir API, kurios gali kurti ir atidaryti PL failus.",
  "title": "PL failas – Perl scenarijaus failo formatas",
  "linktitle": "PL",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-p-ltl"
}
},
  "lastmod": "2021-07-23"
}

## Kas yra PL failas?

Failas su plėtiniu .pl yra Perl Script failas, kuris yra scenarijų kalba. Jie sudaromi ir vykdomi naudojant Perl Interpreter programinę įrangą. PL scenarijaus faile yra kodo eilučių, kintamųjų ir komentarų. Scenarijų kalbas yra gana sunku
suprasti kitus programavimo failų formatus, pvz., [PHP](/programming/php/). PL failus galima sukurti ir jie yra suderinami su Windows, MacOS ir Linux.

## Trumpa „Perl“ scenarijų kalbos istorija

Ši kalba pirmą kartą buvo naudojama 1987 m., todėl šie failai atsirado tais metais. 1989 m. buvo išleistas Perl 2. Vėliau ji buvo atnaujinta ir modifikuota iki 5.35 versijos, o kitą versiją planuojama išleisti kitais metais.

Kiekviename atnaujinime buvo pridėta įrankių, susijusių su kalbos ir failų funkcionalumu, našumu ir išvaizda. Šiais metais buvo atlikta daug versijų peržiūrų. Iš pradžių tai buvo pagrindinė scenarijų kalba, tačiau dabar ji apima ir daugybę kitų modulių. Iš pradžių tai buvo labai paprasta kalba, tačiau šios kalbos raštus buvo gana sunku suprasti, nes jie buvo kompaktiški.

## Perl failo formato plėtinio specifikacijos

Yra keletas šių programavimo failų savybių arba specifikacijų, kai kurios iš jų yra tokios:

* Į šiuos failus įtrauktas kodas yra paprasto teksto formatu ir naudojamas scenarijui kurti
* Serverio scenarijų kūrimas, teksto analizavimas ir serverio administravimas yra pagrindiniai aspektai, kuriuos apima šios kalbos scenarijus
* Daugelis populiarių programų, susijusių su šia kalba, yra Active State Active Perl ir Bare Bones BBEdit (suderinama su Mac OS)
* Ši kalba laikoma aukšto lygio kalba
* Win32 naudotojui gali tekti įdiegti savąjį dvejetainį kalbos paskirstymą
* Tam, kad būtų galima vykdyti įvairius Windows išteklių rinkinius, reikalingi kai kurie scenarijų rašymo įrankiai
* Visual Studio .NET yra garsi programavimo kalbų kūrimo sistema. Active State įrankis, žinomas kaip Visual Perl, naudojamas Perl įtraukimui į Visual studio.
* Failuose pirmoje šaltinio kodo eilutėje aprašoma naudojamo vertėjo informacija. PL failai paprastai prasideda **#!/usr/bin/perl** eilute, kuri nurodo kompiuteriui paleisti šį scenarijų naudojant kompiuteryje įdiegtą Perl interpretatorių


## PL scenarijaus pavyzdžiai

```
#!/usr/bin/perl
print "Hello, world\n";
```

Tai bus išspausdinta

```
Hello, World
```

### Vienos eilutės komentaras ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Kelių eilučių komentaras ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Kintamojo priskyrimas ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Skaliarinio kintamojo priskyrimas ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Paprastos skaliarinės operacijos ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Nuorodos Nr.

- [Python (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

