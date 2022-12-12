{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier AWK - Fișier script AWK",
  "description":"Aflați despre formatul de fișier AWK și despre API-urile care pot crea și deschide fișiere AWK.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Ce este un fișier AWK?

Un fișier AWK este un fișier script creat pentru aplicația de procesare a textului **AWK** care vine la pachet cu sistemele de operare Unix și Linux. Conține instrucțiuni logice pentru a efectua acțiuni asupra textului sau conținutului unui fișier, cum ar fi potrivirea, înlocuirea și imprimarea textului. Acest lucru ajută la generarea de rapoarte și de text formatat din fișierul de intrare. Utilitarul awk este de obicei localizat în /usr/bin/awk pe majoritatea distribuțiilor Linux/unix.

## Cum se creează un script AWK?

Un fișier AWK poate fi creat sau deschis în orice editor de text pe sistemul de operare Linux/Unix. Un nou fișier script AWK poate fi creat după cum urmează.

```
$ vi script.awk
```

Aceasta va deschide fișierul AWK în editorul de text. Introduceți câteva afirmații în editorul de text după cum urmează.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Prima linie a acestui conținut text este explicată după cum urmează.

* \#! – denumit „Shebang”, care specifică un interpret pentru instrucțiunile dintr-un script
* /usr/bin/awk – este interpretul
* -f – opțiune de interpret, folosită pentru a citi un fișier de program

## Cum se execută scriptul AWK?

Salvați fișierul și faceți scriptul executabil lansând comanda de mai jos:
```
$ chmod +x script.awk
```

Scriptul poate fi rulat după cum urmează.

```
$ ./script.awk
```

care are ca rezultat următoarea ieșire.

```
Writing my first Awk executable script!
```

## Referință ##

* [Scrieți scripturi folosind limbajul de programare Awk](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

