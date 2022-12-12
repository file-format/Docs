{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "fișier", "extensie", "format fișier", "implementare mrc", "Ghid de programare", "exemplu mrc", "mIRC", "limbaj de scripting mIRC", "fișiere INI", " limbaj de scripting mSL", "limbaj de scripting mIRC", "scripturi mIRC", "limbaj de scripting" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - fișierul limbaj de script mIRC",
  "description":"Aflați despre formatul fișierului MRC și despre API-urile care pot crea și deschide fișiere MRC.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## Ce este un fișier MRC?

mIRC este un limbaj de scripting care este încorporat ca client IRC (Internet Relay Chat) în sistemul de operare Windows. Oferă o facilitate de protecție împotriva spam-ului pentru uz personal și canal. Pentru a oferi o experiență mai bună de compatibilitate cu utilizatorii, acest limbaj de scripting mIRC permite crearea de ferestre de dialog. Fișierele care conțin scripturi, majoritatea în format text simplu, sunt stocate cu extensia MRC sau ca fișiere [INI](/ro/system/ini/). Funcțiile acestui limbaj sunt cunoscute ca comenzi și identificatori (când returnează valoare).

Limbajul mIRC asigură încărcarea mai multor fișiere script simultan. Pe de altă parte, un fișier poate face ca celălalt să nu mai fie utilizat atunci când este încărcat simultan. Comenzile sunt salvate și pot exista automat în IRC. Comenzile și aliasurile utilizate în această limbă nu au prioritate pentru niciunul dintre caractere.

mIRC este utilizat pe scară largă pentru a face ca boții să gestioneze un canal în mod automat, dar poate fi modificat și prin limbajul de scripting mSL. Poate introduce multe funcții noi, cum ar fi macrocomenzi, capacitatea de redare a muzicii, macrocomenzi și funcții mici, jocuri de bază sau operarea aplicațiilor mici.


## Scurt istoric ##

Acest limbaj de scripting a fost dezvoltat pentru prima dată în 1995 de Khaled Adam Bey. Designul limbajului de scripting a fost, de asemenea, creat de Khalid. Ținta acestui limbaj a fost programarea bazată pe evenimente. Inițial, extensia de fișier folosită pentru fișierele acestui limbaj de programare a fost .mrc și .ini. Mai mult, a fost dezvoltat sub licența unui software proprietar.

## Specificatii tehnice ##

Unele funcții sunt personalizate prin scripturi prin acest limbaj mIRC și sunt cunoscute sub numele de alias. Când aceste aliasuri returnează valori, ele sunt cunoscute ca identificatori personalizați. Toate variabilele conținute în acest limbaj mIRC sunt tipărite dinamic. Sigilurile sunt folosite de scripturile mIRC. O altă caracteristică a acestui limbaj de scripting sunt ferestrele pop-up. Utilizatorii pot apela ferestre pop-up prin simpla selectare a acestora. Telecomenzile sunt specificate pentru anumite evenimente. Telecomenzile sunt apelate atunci când are loc evenimentul relativ.

Jetoanele delimitate de spațiu sunt folosite pentru a sparge fiecare linie de cod a acestui limbaj. Există și alte extensii populare utilizate pentru fișierele mIRC, cum ar fi MDX (mIRC Dialog Extension) și DCX (Dialog Control Extension). Ambele sunt extensii de dialog și sunt comparativ mai populare. Construcțiile limbajului sunt menționate de nomenclatura acestui limbaj de scripting. Limbajul mIRC implică diferite aspecte ale unui limbaj de scripting, cum ar fi variabile locale și globale, variabile binare, tabele hash și gestionarea fișierelor.


## Exemplu de format de fișier MRC ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/ro/echo) 'Hello World!' into the active window(-a)
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

## Referință ##

* [MIRC - de la Wikipedia](https://en.wikipedia.org/wiki/MIRC_scripting_language)



