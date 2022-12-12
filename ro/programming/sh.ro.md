{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH – Fișier script Bash Shell",
  "description":"Aflați despre formatul de fișier SH și despre API-urile care pot crea și deschide fișiere SH.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Ce este un fișier SH?

Un fișier cu extensia .sh este un fișier de comenzi în limbajul de scripting care conține un program de calculator care urmează să fie rulat de shell Unix. Poate conține o serie de comenzi care rulează secvențial pentru a efectua operațiuni precum procesarea fișierelor, execuția programelor și alte astfel de sarcini. Acestea sunt executate din interfața liniei de comandă de către utilizator sau în lot pentru a efectua mai multe operațiuni în același timp. Fișierele script pot fi deschise în editori de text precum Notepad, Notepad++, Vim, Apple Terminal și alte aplicații similare pe Windows, MacOS și Linux OS.

## Format de fișier SH

Fișierele SH sunt scrise în text simplu, urmând sintaxa definită. Aceste fișiere script acceptă:

* `Comentarii` - Comentariile încep cu # și sunt ignorate de shell.
* `Shortcuts` - Acestea pot fi folosite pentru a redenumi o comandă pentru o execuție scurtă și ușoară.
* `Locuri de muncă` - Mai multe comenzi pot fi executate automat, care altfel ar trebui introduse manual. Acest lucru elimină nevoia de a aștepta ca un utilizator să declanșeze fiecare etapă a secvenței.
* `Generalizare` - Folosind bucle simple, se realizează mult mai multă generalizare pentru operațiuni precum conversia imaginilor dintr-un format în altul.

## Exemplu de fișier SH

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## Cum se rulează fișierul SH?
Fișierele SH rulează de obicei pe Linux, chiar și în Windows trebuie să vă conectați la un terminal Linux folosind software-uri precum Putty pentru a rula fișierele sh. Următorii sunt pașii pentru a rula un fișier SH pe un terminal Linux.

1. Deschideți terminalul Linux și mergeți la directorul în care se află fișierul SH.
2. Folosind comanda `chmod`, setați permisiunea de execuție pe script-ul dvs. (dacă nu este deja setată).
3. Rulați scriptul utilizând una dintre următoarele
1. `./filename.sh`
2. `sh filename.sh`
3. `bash script-name-here.sh`

## Referințe

* [Bashscripting pentru începători](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

