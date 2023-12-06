{
"data": "2023-05-24",
  "keywords": [
"fișier cba",
"Ce este un fișier cba",
"cum se creează fișierul CBA",
"ce conține fișierul CBA",
"care este formatul fișierului cba",
"fişier",
"extensie fișier cba",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format fișier CBA - Arhiva de benzi desenate",
  "description":"Aflați despre formatul CBA și despre API-urile care pot crea și deschide fișiere CBA.",
"linktitle": "CBA",
  "menu": {
    "docs": {
      "identifier": "compression-cba",
      "parent": "compression"
}
},
"lastmod": "2023-05-24"
}

## Ce este un fișier CBA?

Un fișier Comic Book Archive (CBA), cunoscut și sub numele de Comic Book Archive sau Comic Book Reader, este un format popular folosit pentru stocarea și distribuirea de benzi desenate digitale. De obicei, conține o colecție de pagini individuale de benzi desenate sau imagini grupate într-un singur fișier pentru organizare și citire ușoară.

Unul dintre formatele comune pentru crearea fișierelor Comic Book Archive este formatul TAR (Tape Archive). TAR este un format de arhivare a fișierelor utilizat în mediile Unix și Linux. Combină mai multe fișiere într-un singur fișier folosit adesea în scopuri de backup.

## Cum se creează fișierul CBA?

Pentru a crea un fișier Arhivă de benzi desenate folosind instrumentul de arhivare TAR, de obicei urmați acești pași:

1. Adunați toate paginile de benzi desenate sau imaginile pe care doriți să le includeți în arhivă.
2. Deschideți o linie de comandă sau o fereastră de terminal.
3. Navigați la directorul în care se află paginile/imaginile de benzi desenate.
4. Utilizați comanda TAR cu opțiunile adecvate pentru a crea arhiva. De exemplu, comanda ar putea arăta astfel:

```
tar -cf comicbook.cbt page1.jpg page2.jpg page3.jpg
```

În acest exemplu, opțiunea -c îi spune TAR să creeze o arhivă nouă, iar opțiunea -f specifică numele fișierului de ieșire (comicbook.cbt în acest caz). După ce specificați opțiunile, furnizați numele fișierelor pe care doriți să le includeți în arhivă (page1.jpg, pagina2.jpg, pagina3.jpg).

5. După executarea comenzii, instrumentul TAR va crea fișierul Comic Book Archive (comicbook.cbt în acest exemplu) în directorul curent.

Odată ce aveți fișierul Comic Book Archive, puteți utiliza diverse programe sau aplicații de citire a benzilor desenate pentru a deschide și a citi benzi desenate pe computer sau dispozitiv. Aceste aplicații oferă de obicei funcții precum navigarea în pagină, mărirea și marcarea de carte pentru a îmbunătăți experiența de citire.

## Ce conține fișierul CBA?

Un fișier de arhivă de benzi desenate (CBA) creat folosind instrumentul de arhivare TAR conține o colecție de pagini individuale de benzi desenate sau imagini grupate într-un singur fișier. Conținutul specific al arhivei depinde de cartea de benzi desenate care este ambalată.

De obicei, un fișier Arhivă de benzi desenate include următoarele:

- **Pagini de benzi desenate:** Conținutul principal al arhivei sunt paginile de benzi desenate în sine. Aceste pagini sunt de obicei salvate ca fișiere imagine individuale, cum ar fi JPEG sau PNG, reprezentând fiecare pagină a cărții de benzi desenate. Paginile sunt aranjate într-o anumită ordine pentru a menține fluxul narativ al benzii desenate.
- **Metadate:** Unele formate de Arhivă de benzi desenate pot include metadate despre cartea de benzi desenate, cum ar fi titlul, autorul, editorul, data publicării și descrierea. Aceste informații ajută la identificarea și clasificarea benzilor desenate.
- **Fișiere suplimentare:** În plus față de paginile de benzi desenate și metadate, arhiva poate conține și alte fișiere suplimentare legate de benzile desenate. Aceste fișiere pot include copertă, imagini promoționale, conținut bonus sau fișiere text care oferă informații sau comentarii suplimentare.

## Care este formatul fișierului CBA?

Formatul de fișier Comic Book Archive (CBA) creat folosind instrumentul de arhivare TAR este de obicei în format TAR. TAR, prescurtare de la Tape Archive, este un format de arhivare a fișierelor folosit în mod obișnuit în sistemele Unix și Linux. Nu este specific cărților de benzi desenate, ci este un format de arhivare de uz general.

Formatul TAR este o modalitate simplă de a grupa mai multe fișiere într-un singur fișier de arhivă. Nu asigură compresie de la sine, astfel încât fișierul TAR rezultat poate avea dimensiuni mari în comparație cu alte formate comprimate, cum ar fi ZIP sau RAR. Cu toate acestea, fișierele TAR pot fi comprimate folosind instrumente suplimentare sau combinate cu algoritmi de compresie precum gzip sau bzip2 pentru a reduce dimensiunea fișierului.

Formatul TAR păstrează structura fișierelor, permisiunile și marcajele de timp ale fișierelor incluse. Stochează fișierele secvenţial în arhivă, permiţând extragerea ușoară a fișierelor individuale sau a întregii arhive.

## Referințe
* [Arhiva de benzi desenate](https://en.wikipedia.org/wiki/Comic_book_archive)

