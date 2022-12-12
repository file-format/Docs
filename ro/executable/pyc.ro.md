{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier PYC și despre API-urile care pot crea și deschide fișiere PYC.",
  "title" :"Format fișier PYC- Fișier compilat Python",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## Ce este un fișier PYC?

Un fișier PYC este un fișier de ieșire compilat generat din codul sursă scris în limbajul de programare Python. Când fișierul PY este rulat folosind interpretul Python, acesta este convertit în bytecode pentru execuție. În același timp, bytecode-ul compilat este salvat și ca fișier .pyc pentru a fi reutilizat din cache la un moment ulterior, dacă este cazul.

## Structura formatului de fișier PYC

Fișierele PYC sunt în cod de octeți, iar specificațiile lor de format de fișier nu sunt disponibile public. Cu toate acestea, investigațiile efectuate de unele surse arată că [structura unui fișier PYC](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A% 20marshalled%20code%20object.) constă din:

* `Un număr magic de patru octeți`r - Pur și simplu doi octeți care se schimbă cu fiecare modificare a codului de marshalling și apoi doi octeți de 0d0a.
* `A timestamp de modificare pe patru octeți` - Unix timestamp de modificare a fișierului sursă care a generat .pyc, astfel încât să poată fi recompilat dacă sursa se schimbă.
* `A marshaled code object` - ieșirea marshal.dump a obiectului cod care este rezultatul compilării fișierului sursă.

## Referințe

* [Structura fișierelor .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A%20marshalled%20code%20object.)

