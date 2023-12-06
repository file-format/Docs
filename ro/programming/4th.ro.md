
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișierul al patrulea - Formatul de fișier al patrulea limbă",
  "description":"Aflați despre ce este formatul de fișier .4th cu exemple și API-uri care pot crea și deschide fișierele 4th.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Ce este al 4-lea fișier?

Un fișier cu extensia de fișier .4th este un fișier de programare creat pentru **Forth Programming Language**. Conține codul sursă pentru programele scrise în limbajul de programare Forth și generează rezultatul când programul este executat. Este doar un alt fișier de limbaj de programare similar cu fișierul sursă [C](/ro/programming/c/) și [C++](/ro/programming/cpp/).

## Al patrulea format de fișier - Mai multe informații


### Exemplu de cod al 4-lea limbaj de programare

Iată un exemplu de program simplu scris în Forth care calculează factorialul unui număr dat:

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

În acest exemplu, cuvântul factorial ia un singur argument n și returnează factorialul său. Cuvântul dup dublează valoarea de deasupra stivei, drop aruncă valoarea de deasupra stivei și * înmulțește cele două valori de deasupra stivei. Construcțiile if și begin/until controlează fluxul programului.

Pentru a utiliza acest program, trebuie să introduceți definiția în interpretul Forth și apoi să apelați cuvântul factorial cu numărul pentru care doriți să găsiți factorialul:

```
10 factorial .
```
Aceasta ar avea ca rezultat ieșirea 3628800, care este factorul de 10.

## Referințe

* [Forth Programming Language](https://en.wikipedia.org/wiki/Forth_(programming_language))

