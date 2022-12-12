{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Manual Unix",
  "description":"Aflați despre formatul de fișier FODT și despre API-urile care pot crea și deschide fișiere MAN.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## Ce este un fișier MAN?

Un fișier cu extensia .man reprezintă pagina de manual, care este un manual al utilizatorului de programare Unix sub formă de documentație software. Este folosit de utilitarul `Man`, inclus în Unix, care este folosit pentru a vizualiza documentația. Documentația software conține informații în secțiuni și pagini care pot fi preluate folosind utilitarul Man din terminalul de comandă prin lansarea de comenzi. Fiind disponibil în computer ca copie software a documentației, nu necesită nicio copie tipărită sau conexiune la internet pentru a o accesa.

## Unix Manual Man File Format - Mai multe informații

Paginile de manual sunt stocate în format text simplu și pot fi create și deschise în orice editor de text pentru vizualizare sau editare. În UNIX, informațiile din paginile Man sunt preluate prin lansarea de comenzi de la terminal care include referințe la numerele de secțiune și de pagină din manual.

### Secțiuni și pagini

Unix man este manualul sistemului în care fiecare argument de pagină al comenzii se referă la numele unui program, utilitar sau funcție. comanda, dacă este furnizată cu informații despre secțiune, va căuta pagina în acea secțiune specifică. Cu toate acestea, comportamentul implicit este de a căuta pagina în toate secțiunile și de a afișa prima pagină, indiferent dacă aceasta există în mai multe secțiuni.

### Numerele secțiunii

Mai jos sunt informații despre numerele de secțiuni ale manualului, urmate de tipurile de pagini pe care le conțin.

|Numărul secțiunii|Tipul paginilor|
---|---|
|1|Programe executabile sau comenzi shell|
|2|Apeluri de sistem (funcții furnizate de kernel)|
|3|Apeluri de bibliotecă (funcții din bibliotecile de programe)|
|4|Fișiere speciale (se găsesc de obicei în /dev)|
|5|Formate de fișiere și convenții, de exemplu /etc/passwd|
|6|Jocuri|
|7|Diverse (inclusiv pachete macro și convenții), de exemplu man(7), groff(7)|
|8|Comenzi de administrare a sistemului (de obicei numai pentru root)|
|9|Rutine kernel [Nestandard]|

## Exemplu - Cum se citesc paginile MAN?

Iată un exemplu despre cum să preluați informații despre comanda MkDir folosind comanda Man.

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

## Referințe

* [OpenDocument Technical Specifications - By Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — Pagina de manual Linux](https://man7.org/linux/man-pages/man1/man.1.html)

