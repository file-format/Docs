{
  "date" : "2019-10-11",
   "keywords" :[ "apkg","fișier apkg", "format fișier apkg", "tip fișier apkg", "fișier", "tip", "Ce este un fișier APKG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Format de fișier Anki Flashcard Deck",
  "description" :"Aflați despre ce este un fișier APKG și API-urile care le pot crea și deschide.",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## Ce este un fișier APKG?

Un fișier cu extensia .apkg este un pachet de carduri flash generate pentru a fi utilizate în aplicația software [Anki](https://ankiweb.net/about), care este un program de învățare bazat pe carduri. Conține [HTML](/ro/web/html/) text pentru a fi încărcat și afișat în aplicația Anki și poate avea în plus imagini și sunete pentru învățare vizuală și sonoră. Anki permite utilizatorilor să-și creeze propriile pachete de carduri Anki, precum și să importe pachetele de carduri ale altor utilizatori.

## Format de fișier APKG

Pachetele de cărți Anki sunt create din șabloane care sunt scrise în HTML, un limbaj faimos și comun pentru crearea de pagini web. Stilizarea cărților de pachet se face folosind CSS, care este limbajul folosit pentru stilarea paginilor web. Stilul include modificări la:

* font-family - Numele fontului care va fi folosit pe card.
* font-size - Mărimea fontului în pixeli.
* text-align - Definește dacă textul trebuie aliniat în centru, stânga sau dreapta.
* culoare - Definește culoarea textului care poate fi nume de culori simple, cum ar fi „albastru”, „roșu”, etc. sau coduri de culoare HTML.
* culoare de fundal - Definește culoarea de fundal a cardului

Informațiile de stil sunt partajate între toate cardurile, afectând toate cardurile atunci când se face o modificare. Următorul exemplu va folosi un fundal galben pe toate cărțile, cu excepția primei:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Redimensionarea imaginilor într-un card Anki poate fi controlată după cum urmează.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Încorporarea Javascript în cardurile Anki

Este posibil să încorporați [Javascript](/ro/web/js/) într-un card Anki folosind șabloanele de card. Cu toate acestea, datorită nivelului avansat de Javascript, suportul acestuia nu este oferit. Mai mult, dispozitivele de randare pot arăta în mod diferit efectele implementării Javascript pe card, ceea ce duce la necesitatea testării implementării pe toate dispozitivele. Anumite caracteristici Javascript, cum ar fi window.alert, fac dificilă depanarea codului Javascript pe care l-ați scris.

## Referințe ##

* [Documentația Anki](https://docs.ankiweb.net/intro.html)

