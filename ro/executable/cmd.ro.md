{
  "date" : "2021-07-12",
  "keywords" :[ "fișier cmd", "ce este un fișier cmd", "fișier", "exemplu cmd", "extensie fișier cmd", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier CMD și despre API-urile care pot crea și deschide fișiere CMD.",
  "title" :"CMD - Windows Command File Format",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## Ce este un fișier CMD?
Un fișier CMD constă dintr-un script care conține una sau mai multe comenzi sub formă de text simplu, care sunt executate pentru a executa diverse sarcini. Este similar cu un fișier [BAT](/ro/executable/bat/), care este, de asemenea, utilizat în general pentru a stoca un lot de comenzi executabile. Fișierele CMD sunt utilizate pe scară largă în sistemul de operare Microsoft Windows. Aceste fișiere au fost introduse aproape în anii 90, dar încă folosite în cel mai recent sistem de operare Windows. Aceste fișiere sunt în general scrise pentru a executa mai multe comenzi într-o secvență.

## Format de fișier CMD
CMD este un format de fișier folosit de programele executabile în stil CP/M. În general, este comparabil cu [COM](/ro/executable/com/) în CP/M-80 și [EXE](/ro/executable/exe/) în DOS. Un fișier CMD conține 1 până la 8 grupuri de cod sau date și un antet de 128 de octeți. Fiecare grup poate avea o dimensiune de până la 1 mb. Fișierele CMD pot conține, de asemenea, informații despre relocare și extensii de sistem rezident (RSX) în versiunile sale ulterioare. CMD este un nou venit în comparație cu fișierul [BAT](/ro/executable/bat/); folosit pentru MS-DOS înainte de lansarea Windows În MS-DOS. Deși, încă puteți salva fișierele cu extensia .bat astăzi, mulți oameni folosesc extensia .cmd pentru a-și salva scripturile executabile.

### Specificație format CMD

Începutul antetului conține lista grupurilor prezente în fișier împreună cu tipurile acestora. Fiecare tip poate fi folosit cel mult o singură dată. Aceste tipuri sunt:

- Cod
- Date
- Extra
- Grămadă
- Utilizatorul 1
- Utilizatorul 2
- Utilizatorul 3
- Utilizatorul 4
- Cod partajat

De asemenea, Prefixul de segment de program în DOS, primii 256 de octeți ai grupului de date sunt zero. Acestea vor fi populate de CP/M-86 cu pagina zero. Dacă nu există un grup de date, atunci primii 256 de octeți ai grupului de cod vor fi utilizați în schimb.
## Exemplu de fișier CMD
Urmează un exemplu de script CMD pentru a afișa informații despre sisteme.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Referințe

* [Cum se scrie un script CMD](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [Fișier CMD (CP/M) - de la Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

