
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "4. tiedosto - Forth Language -tiedostomuoto",
  "description":"Opi .4. tiedostomuodosta esimerkin ja sovellusliittymien avulla, jotka voivat luoda ja avata 4. tiedostoja.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th-fi",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Mikä on neljäs tiedosto?

Tiedosto, jonka tunniste on .4, on ohjelmointitiedosto, joka on luotu **Forth-ohjelmointikielelle**. Se sisältää lähdekoodin Forth-ohjelmointikielellä kirjoitetuille ohjelmille ja tuottaa tulosteen, kun ohjelma suoritetaan. Se on vain toinen ohjelmointikielitiedosto, joka muistuttaa lähdetiedostoa [C](/programming/c/) ja [C++](/programming/cpp/).

## 4. tiedostomuoto – lisätietoja


### Neljännen ohjelmointikielen koodiesimerkki

Tässä on esimerkki yksinkertaisesta Forthilla kirjoitetusta ohjelmasta, joka laskee tietyn luvun kertoimen:

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

In this example, the factorial word takes a single argument n and returns its factorial. The dup word duplicates the value on top of the stack, drop discards the value on top of the stack, and * kertoo kaksi pinon päällä olevaa arvoa. If- ja start/ontil-konstruktit ohjaavat ohjelman kulkua.

Käyttääksesi tätä ohjelmaa sinun tulee kirjoittaa määritelmä Forth-tulkkiin ja kutsua sitten faktoriaalisanaa numerolla, josta haluat löytää faktoriaalin:

```
10 factorial .
```
Tämä johtaisi ulostuloon 3628800, joka on kertoimella 10.

## Viitteet

 * [Forth Programming Language](https://en.wikipedia.org/wiki/Forth_(programming_language))

