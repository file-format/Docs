{
  "date": "2021-09-14",
  "keywords": [
"mrc",
"fil",
"udvidelse",
"filformat",
"mrc implementering",
"Programmeringsvejledning",
"mrc eksempel",
"mIRC",
"mIRC scriptsprog",
"filer af INI",
"mSL scriptsprog",
"mIRC sprog",
"mIRC scripts",
"scriptsprog"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "MRC - mIRC Script sprogfil",
  "description": "Lær om MRC filformat og API'er, der kan oprette og åbne MRC filer.",
  "linktitle": "MRC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mr-dac"
}
},
  "lastmod": "2021-09-14"
}

## Hvad er en MRC fil?

mIRC er et scriptsprog, der er indlejret som en IRC-klient (Internet Relay Chat) i Windows-operativsystemet. Det giver en mulighed for beskyttelse mod spamming til personlig brug og kanalbrug. For at give en bedre oplevelse af brugerkompatibilitet tillader dette mIRC-scriptsprog oprettelsen af dialogvinduer. De filer, der indeholder scripts, for det meste i almindeligt tekstformat, gemmes med forlængelsen af MRC eller som filerne til [INI](/system/ini/). Funktioner i dette sprog er kendt som kommandoer og identifikatorer (når de returnerer værdi).

mIRC sprog giver indlæsning af flere scriptfiler på én gang. På den anden side kan en fil forårsage, at den anden ikke længere bruges, når den indlæses samtidigt. Kommandoer gemmes, og de kan eksistere i IRC automatisk. De kommandoer og aliaser, der bruges på dette sprog, har ikke forrang for nogen af tegnene.

mIRC bruges i vid udstrækning til at få bots til at styre en kanal automatisk, men det kan også modificeres af mSL-scriptsproget. Det kan introducere mange nye funktioner som makroer, musikafspilningsevne, små makroer og funktioner, grundlæggende spil eller betjening af små applikationer.


## Kort historie ##

Dette scriptsprog blev først udviklet i 1995 af Khaled Adam Bey. Designet af scriptsproget blev også skabt af Khalid. Målet for dette sprog var begivenhedsdrevet programmering. Oprindeligt var filtypen, der blev brugt til filerne i dette programmeringssprog, .mrc og .ini. Desuden blev det udviklet under licens af proprietær software.

## Teknisk specifikation ##

Nogle funktioner er brugerdefinerede scripts gennem dette mIRC-sprog og er kendt som aliaser. Når disse aliaser returnerer værdier, er de kendt som brugerdefinerede identifikatorer. Alle variabler indeholdt i dette mIRC-sprog er dynamisk indtastet. Sigils bruges af mIRC scripts. En anden funktion ved dette scriptsprog er pop-ups. Brugerne kan kalde pop-ups ved blot at vælge dem. Fjernbetjeninger er specificeret til bestemte begivenheder. Fjernbetjeningerne kaldes, når den relative hændelse indtræffer.

Mellemrumsafgrænsede tokens bruges til at bryde hver linje kode på dette sprog. Der er nogle andre populære udvidelser, der bruges til mIRC-filer, såsom MDX (mIRC Dialog Extension) og DCX (Dialog Control Extension). Begge disse er dialogudvidelser og er forholdsvis mere populære. Sprogkonstruktionerne henvises til af nomenklaturen for dette scriptsprog. mIRC-sproget involverer forskellige aspekter af et scriptsprog såsom lokale og globale variabler, binære variabler, hashtabeller og filhåndtering.


## MRC filformat eksempel ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Reference ##

* [MIRC - af Wikipedia](https://en.wikipedia.org/wiki/MIRC_scripting_language)




