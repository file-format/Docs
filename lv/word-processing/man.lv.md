{
  "date": "2021-07-25",
  "keywords": [
"vīrietis",
"failu",
"pagarinājumu",
"veids",
"formātā",
"Unix rokasgrāmata"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MAN - Unix rokasgrāmata",
  "description": "Uzziniet par FODT faila formātu un API, kas var izveidot un atvērt MAN failus.",
  "linktitle": "MAN",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-ma-lvn"
}
},
  "lastmod": "2021-07-25"
}

## Kas ir MAN fails?

Fails ar paplašinājumu .man apzīmē man lapu, kas ir Unix programmēšanas lietotāja rokasgrāmata programmatūras dokumentācijas formā. To izmanto utilīta Man, kas iekļauta Unix un tiek izmantota dokumentācijas skatīšanai. Programmatūras dokumentācijā sadaļās un lapās ir ietverta informācija, ko var izgūt, izmantojot utilītu Man no komandu termināļa, izdodot komandas. Tā kā tā ir pieejama datorā kā dokumentācijas mīksta kopija, tai nav nepieciešama drukāta kopija vai interneta savienojums, lai tai piekļūtu.

## Unix Manual Man faila formāts — vairāk informācijas

Man lapas tiek glabātas vienkārša teksta formātā, un tās var izveidot un atvērt jebkurā teksta redaktorā apskatei vai rediģēšanai. Operētājsistēmā UNIX informācija no Man lapām tiek izgūta, izdodot komandas no termināļa, kas ietver atsauci uz rokasgrāmatas sadaļu un lappušu numuriem.

### Sadaļas un lapas

Unix man ir sistēmas rokasgrāmata, kurā katrs komandas lapas arguments attiecas uz programmas, utilīta vai funkcijas nosaukumu. komanda, ja tiek nodrošināta sadaļas informācija, meklēs lapu šajā konkrētajā sadaļā. Tomēr noklusējuma darbība ir meklēt lapu visās sadaļās un parādīt pirmo lapu neatkarīgi no tā, vai tā pastāv vairākās sadaļās.

### Sadaļu numuri

Tālāk ir sniegta informācija par rokasgrāmatas sadaļu numuriem, kam seko tajās ietverto lapu veidi.

|Sadaļas numurs|Lapu veids|
---|---|
|1|Izpildāmās programmas vai čaulas komandas|
|2|Sistēmas izsaukumi (kodola nodrošinātās funkcijas)|
|3|Bibliotēkas izsaukumi (funkcijas programmu bibliotēkās)|
|4|Īpaši faili (parasti atrodami mapē /dev)|
|5|Failu formāti un konvencijas, piemēram, /etc/passwd|
|6|Spēles|
|7|Dažādi (tostarp makro pakotnes un konvencijas), piemēram, man(7), groff(7)|
|8|Sistēmas administrēšanas komandas (parasti tikai root)|
|9|Kodola rutīnas [Nestandarta]|

## Piemērs — kā lasīt MAN lapas?

Šeit ir piemērs, kā izgūt informāciju par MkDir komandu, izmantojot komandu Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Atsauces

* [OpenDocument tehniskās specifikācijas — Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)

* [man(1) — Linux rokasgrāmatas lapa](https://man7.org/linux/man-pages/man1/man.1.html)


