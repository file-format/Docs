{
  "date" : "2021-07-08",
  "keywords" :[ "SYS", "extensie", "fișier", "format", "sistem", "Driver", "Fișier de sistem", "programe", "calculator", "aplicație"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Format fișier de sistem",
  "description":"Aflați despre formatul de fișier SYS și despre API-urile care pot crea și deschide fișiere SYS.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Ce este un fișier SYS? ##

Fișierele SYS sunt „fișiere de sistem” utilizate în aplicațiile Windows OS și MS-DOS. Aceste fișiere nu pot fi deschise direct și constau din driverul și configurația dispozitivului. Fișierele SYS sunt responsabile pentru conținutul fișierelor cu funcțiile de bază ale sistemului de operare. Acestea sunt considerate fișiere critice ale driverului de dispozitiv și pot fi utilizate și atunci când orice problemă a șoferului de curse urmează să fie rezolvată. Acestea sunt responsabile pentru buna funcționare a unui sistem informatic, iar fișierele .sys trebuie să fie corecte și complete.


## Specificatii tehnice ##

Fișierele .sys sunt de fapt subsetul formatului [BMP](/ro/image/bmp/), deoarece permite doar combinații specifice. Formatul obișnuit al acestor fișiere este ca LOGOS.SYS, LOGOW.SYS și LOGO.SYS. Orice alte fișiere nu au acest format.

Aceste fișiere sunt utilizate în principal în directorul *C* al Windows la momentul instalării. Cele mai multe probleme care gravitează în jurul driverelor de dispozitiv sunt rezolvate prin actualizarea sistemului de operare Windows. Detaliile și informațiile acestor fișiere pot fi vizualizate utilizând programele încorporate ale sistemului de operare Windows. Acestea cuprind, de asemenea, referințe la diferite module dintr-un sistem de operare.
Câteva dintre exemplele de fișiere de sistem sunt:

* IO.SYS ( Acestea stochează driverele de dispozitiv ale sistemului de operare pe disc)
* MSDOS.SYS (acestea conțin nucleul sau codul de bază al sistemului de operare)
* CONFIG.SYS (acestea conțin diverse opțiuni de configurare)
* KEYBOARD.SYS (acestea conțin informații legate de aspectul tastaturii)
* COUNTRY.SYS (Aceste conțin informații despre țară și pagina de coduri)

## Format fișier SYS ##

Microsoft a dezvoltat fișierele cu extensii .sys. Variabilele și funcțiile sunt incluse în fișierele SYS. Acestea sunt utilizate în principal de sistemul de operare Microsoft. Aceste fișiere se află în principal în directorul rădăcină al discului:

* C:\Windows\system32\drivers
* C:\Windows\WinSxS

Unele avertismente comune despre fișierele SYS sunt următoarele:

* Numele acestor fișiere nu trebuie schimbate, deoarece aceste fișiere sunt responsabile pentru funcțiile și variabilele de bază ale sistemului de operare
* Aceste fișiere nu trebuie șterse deoarece absența acestor fișiere poate cauza erori
* Fișierele .sys nu trebuie descărcate de pe internet până când nu sunteți sigur de legitimitatea sursei
* Nu ar trebui să se încurce cu aceste fișiere, deoarece schimbarea lor sau încurcarea cu acestea provoacă erori grave de sistem
* Dacă aceste fișiere sunt corupte de viruși sau programe malware, acestea ar trebui reinstalate

## Exemplu SYS ##

Următorul este un exemplu de fișier simplu de configurare a sistemului SYS:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
