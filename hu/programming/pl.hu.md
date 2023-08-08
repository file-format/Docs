{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "file", "extension", "format", "Perl", "Perl nyelv", "PL fájlok", "programozás"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a PL fájlformátumról és az API-król, amelyek PL fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"PL fájl - Perl Script fájlformátum",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## Mi az a PL fájl?

A .pl kiterjesztésű fájl egy Perl Script fájl, amely egy szkriptnyelv. Ezeket a Perl Interpreter szoftverrel fordítják és futtatják. A PL szkriptfájl kódsorokat, változókat és megjegyzéseket tartalmaz. A szkriptnyelvek viszonylag nehezen használhatók
megérteni más programozási fájlformátumokat, például [PHP](/hu/programing/php/). PL fájlok hozhatók létre, és kompatibilisek a Windows, a macOS és a Linux rendszerrel.

## A Perl szkriptnyelv rövid története

Ezt a nyelvet először 1987-ben használták, így ezek a fájlok ebben az évben keletkeztek. 1989-ben adták ki a Perl 2-t. Később frissítették és módosították az 5.35-ös verzióig, a következő verzió pedig a tervek szerint jövőre jelenik meg.

Minden frissítés tartalmaz eszközöket a nyelv és a fájlok funkcionalitására, teljesítményére és megjelenésére vonatkozóan. Ezekben az években sok átdolgozás történt a verziókkal kapcsolatban. Eredetileg egy alap szkriptnyelv volt, de ma már sok más modult is tartalmaz. Eredetileg ez egy nagyon egyszerű nyelv volt, de ennek a nyelvnek a szövegét meglehetősen nehéz volt megérteni, mivel tömörek voltak.

## Perl fájlformátum-kiterjesztés specifikációi

Ezeknek a programozási fájloknak van néhány tulajdonsága vagy specifikációja, ezek közül néhány a következő:

* Az ezekben a fájlokban található kód sima szöveges formátumú, és a szkriptek fejlesztésére szolgál
* A szerver szkriptelése, a szöveg elemzése és a szerver adminisztrációja a fő szempont, amelyet ennek a nyelvnek a szkriptje lefed
* Számos népszerű program, amely ehhez a nyelvhez kapcsolódik, az Active State Active Perl és a Bare Bones BBEdit (kompatibilis a Mac OS rendszerrel)
* Ez a nyelv magas szintű nyelvnek számít
* Win32 esetén előfordulhat, hogy a felhasználónak telepítenie kell a nyelv natív bináris terjesztését
* Szükség van néhány parancsfájl-készítő eszközre, hogy végrehajthatóvá váljon a különböző Windows Resource Kitekben
* A Visual Studio .NET a programozási nyelvek fejlesztésének híres keretrendszere. A Visual Perl néven ismert Active State eszköz a Perl Visual stúdióba való hozzáadására szolgál
* A fájlokban a forráskód első sora a használt értelmező információit írja le. A PL fájlok általában a **#!/usr/bin/perl** sorral kezdődnek, amely arra utasítja a számítógépet, hogy futtassa ezt a szkriptet a számítógépre telepített Perl értelmező segítségével.


## PL szkript példák

```
#!/usr/bin/perl
print "Hello, world\n";
```

Ez kinyomtatja

```
Hello, World
```

### Egysoros megjegyzés ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Többsoros megjegyzés ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Változó hozzárendelés ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Skaláris változó hozzárendelés ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Egyszerű skaláris műveletek ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Hivatkozások ##

- [Python (programozási nyelv) - Wikipédia](https://en.wikipedia.org/wiki/Python_(programming_language))

