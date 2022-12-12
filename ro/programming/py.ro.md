---
date: 2019-10-11
keywords: py, python, .py, format de fișier py, cum se deschide fișierul py, cum se rulează fișierele py, cum se rulează fișierele python, cum se rulează python
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier PY
linktitle: PY
description: "Aflați despre formatul de fișier PY și despre API-urile care pot crea și deschide fișiere PY."
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## Ce este un fișier PY? ##

Fișierele cu extensia .py conțin codul sursă Python. Limbajul Python a devenit un limbaj foarte faimos acum. Poate fi folosit pentru scripturi de sistem, dezvoltare web și software și matematică. Python acceptă compatibilitatea între platforme; înseamnă că aplicațiile dezvoltate în Python pot funcționa pe diferite platforme precum Windows, MAC, Linux, Raspberry Pi etc. Python oferă o sintaxă simplă și ușor de citit, care este similară cu limba engleză. Dezvoltatorii pot scrie o aplicație software rezonabilă scriind câteva rânduri de cod Python. Deoarece Python rulează pe un sistem interpret, codul poate fi executat imediat ce este scris, ceea ce îl face foarte bun pentru prototipare.

## Scurt istoric ##

Python a fost conceput la sfârșitul anilor 1980 de Guido van Rossum ca un succesor al limbajului de programare ABC. Implementarea sa a început în decembrie 1989 cu Van Rossum ca unic dezvoltator principal. A lucrat pe python până la 12 iulie 2018. În ianuarie 2019, dezvoltatorii activi de bază Python au ales un „Consiliu de conducere” format din cinci membri, compus din Nick Coghlan, Brett Cannon, Carol Willing, Barry Warsaw și Van Rossum pentru a conduce proiectul.

### Versiuni ###

- Python 2.0 a fost lansat pe 16 octombrie 2000.
- Python 3.0 a fost lansat pe 3 decembrie 2008.

## Cum se rulează fișierul py ##

Pentru a verifica versiunea de Python instalată, puteți utiliza următoarea comandă:

```cmd
python --version
```

Aceasta va scoate versiunea pe consolă ca

```cmd
Python 3.7.4
```

Dacă Python nu este instalat pe computer, puteți accesa [python.org](https://www.python.org/) și puteți descărca și instala Python pentru sistemul dvs. de operare relevant.

Pentru a executa un script Python, puteți folosi următoarea comandă:

```cmd
python helloworld.py
```

*helloworld.py* este un fișier script care conține următorul cod

```py
print("Hello World from Python")
```

Aceasta va imprima următoarele în fereastra consolei.

```cmd
Hello World from Python
```

Notă: Dacă utilizați IDE-uri, acestea oferă butoane pe ecran sau diferite comenzi rapide de la tastatură pentru a rula Python. De exemplu, un buton de redare este afișat în jgheab cu editorul din PyCharm, care vă permite să executați scriptul Python.

## Format fișier PY ##

Python a fost conceput pentru a fi lizibil și are asemănări cu engleza și matematica. Python folosește linii noi pentru a indica comanda completă, spre deosebire de punctele și virgulă sau parantezele utilizate în alte limbi. Pentru domenii, bucle și funcții, Python se bazează pe indentare și spații albe, spre deosebire de acolade folosite în alte limbi.

### Sintaxă ###

Următorul este un exemplu de sintaxă Python.

```py
print("Hello World")

#Variables
name = "John"
age = 25
print(name)
print(age)

#While Loop
i = 1
while i < 3:
  print(i)
  i += 1
  
#For Loop
names = ["John", "Harry", "Tom"]
for name in names:
  print(name)
```

## Referințe ##

- [Python (limbaj de programare) - Wikipedia](https://en.wikipedia.org/wiki/Python_(limbaj_de_programare))

