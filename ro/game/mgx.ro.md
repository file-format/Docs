{
  "date" : "2021-09-08",
  "keywords" :[ "fișier mgx", "format fișier mgx", "ce este un fișier mgx", "fișier", "exemplu mgx", "extensie fișier mgx", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier MGX Age of Empires 2 Expansion Replay și despre API-urile care pot crea și deschide fișiere MGX.",
  "title" :"MGX - Age of Empires 2 Expansion Replay",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Ce este un fișier MGX?

Un fișier cu extensia .mgx este un fișier înregistrat pentru jocul Age of Empires II: The Conquerors care poate fi rejucat în cadrul programului Age of Empires II. Conține înregistrarea completă a campaniei redate de utilizator. Poate fi încărcat și redat în programul Age of Empires II. Odată rejucat, jocul arată toate evenimentele și scenariile pe care utilizatorul le-a planificat pentru campanie și le-a jucat.

## Format de fișier MGX - Mai multe informații

Formatul de fișier intern al fișierului MGX a fost elaborat și disponibil ca informații parțial validate în [Age of Empires 2: The Conquerors — Specificația formatului fișierului Savegame](https://github.com/stefan-kolb/aoc-mgx- format). Specificațiile conturează detaliile în secțiunile următoare.

### Definiții structurii

Se crede că definițiile structurii formatului de fișier GPX se bazează pe [declarațiile BinData Ruby Gem](https://github.com/dmendel/bindata/wiki) care oferă o modalitate de a citi și scrie date binare structurate. Acest lucru permite programatorului să specifice formatul datelor binare care sunt apoi citite și scrise de BinData.

### Mesaje MGX

Mesageria MGX se bazează pe două tipuri de mesaje.

* GAMESTART - specifică comenzile de pornire a jocului și nu este validat până în prezent
* CHAT - descrie mesajele de chat din joc. Atât jucătorii, cât și jocul în sine (Gaia) pot emite mesaje în joc.

### ACȚIUNI DE JOC

Există mai multe [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) care au fost preluate și ale căror detalii sunt disponibile.

## Referințe

* [Age of Empires 2: The Conquerors — Specificația formatului fișierului Savegame](https://github.com/stefan-kolb/aoc-mgx-format)

