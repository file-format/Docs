
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"4e bestand - Forth-taalbestandsformaat",
  "description":"Leer meer over wat het .4th-bestandsformaat is met voorbeelden en API's die 4th-bestanden kunnen maken en openen.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Wat is een 4e bestand?

Een bestand met de bestandsextensie .4th is een programmeerbestand gemaakt voor de **Forth Programming Language**. Het bevat de broncode voor programma's die zijn geschreven in de programmeertaal Forth en genereert de uitvoer wanneer het programma wordt uitgevoerd. Het is gewoon een ander programmeertaalbestand dat lijkt op het bronbestand [C](/nl/programming/c/) en [C++](/nl/programming/cpp/).

## 4e bestandsformaat - Meer informatie


### 4e programmeertaalcodevoorbeeld

Hier is een voorbeeld van een eenvoudig programma geschreven in Forth dat de faculteit van een bepaald getal berekent:

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

In dit voorbeeld neemt het factoriële woord één enkel argument n en retourneert de faculteit ervan. Het dup-woord dupliceert de waarde bovenaan de stapel, drop gooit de waarde bovenaan de stapel weg en * vermenigvuldigt de twee waarden bovenaan de stapel. De if- en begin/until-constructies bepalen de stroom van het programma.

Om dit programma te gebruiken, voert u de definitie in de Forth-interpreter in en roept u vervolgens het faculteitswoord aan met het getal waarvan u de faculteit wilt vinden:

```
10 factorial .
```
Dit zou resulteren in de uitvoer 3628800, wat de faculteit van 10 is.

## Referenties

* [Forth programmeertaal](https://en.wikipedia.org/wiki/Forth_(programming_language))

