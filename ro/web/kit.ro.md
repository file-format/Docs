{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier KIT și despre API-urile care pot crea și deschide fișiere KIT.",
  "title" :"Format fișier KIT - fișier CodeKit",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Ce este un fișier KIT?

Un fișier cu extensia .kit este un fișier HTML care este creat cu aplicația de limbaj de programare [CodeKit](https://codekitapp.com/). Conține „importuri” și „variabile” în plus față de fișierele [HTML](/ro/web/html/) existente, ceea ce îl face ideal pentru site-urile statice. CodeKit compilează fișierele KIT în HTML, care pot fi utilizate cu ușurință ca fișiere statice de site-uri web.

## Format de fișier KIT

Fișierele KIT sunt fișiere HTML care includ în plus importuri și variabile. Acestea sunt stocate ca fișiere text simplu și pot fi deschise cu orice editor de text sau editor de fișiere web.

### Import de fișiere KIT

Aproape orice tip de fișier poate fi importat într-un fișier Kit. Mai jos este sintaxa de import utilizată pentru a importa fișiere într-un fișier .kit.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Când un import este adăugat la un fișier KIT și salvat, acesta este înlocuit cu textul fișierului importat. De asemenea, puteți utiliza @include în loc de @import.

### Importuri multiple într-un fișier KIT

De asemenea, puteți importa mai multe fișiere simultan, folosind o listă separată prin virgulă:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Referințe

* [Ce este Kit?](https://codekitapp.com/help/kit/)

