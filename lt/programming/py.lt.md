---
date: 2019-10-11
keywords: py, python, .py, py file format, how to open py file, how to run py files, how to run python files, how to run python
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PY failo formaat
linktitle: PY
description: Luždirbti apie PY failo formatą ir API, kurios gali sukurti ir atidaryti PY failąs.
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## Kas yra PY failas? ##

Failuose su plėtiniu .py yra Python šaltinio kodas. Python kalba šiais laikais tapo labai žinoma kalba. Jis gali būti naudojamas sistemos scenarijų kūrimui, žiniatinklio ir programinės įrangos kūrimui bei matematikai. Python palaiko kelių platformų suderinamumą; reiškia, kad Python sukurtos programos gali veikti įvairiose platformose, tokiose kaip Windows, MAC, Linux, Raspberry Pi ir kt. Python pateikia paprastą ir lengvai skaitomą sintaksę, panašią į anglų kalbą. Kūrėjai gali parašyti pagrįstą programinę įrangą parašydami kelias Python kodo eilutes. Kadangi Python veikia interpretatoriaus sistemoje, kodas gali būti vykdomas iškart po jo parašymo, todėl jis labai tinka prototipams kurti.

## Trumpa istorija ##

Python was conceived in the late 1980s by Guido van Rossum as a successor to ABC programming language. Its implementation began in December 1989 with Van Rossum as the sole lead developer. He worked on python until 12 July 2018. 2019 m. sausį aktyvūs Python pagrindiniai kūrėjai išrinko penkių narių Valdymo tarybą, kurią sudaro Nickas Coghlanas, Brettas Cannonas, Carol Willing, Barry Warsaw ir Van Rossum, vadovauti projektui.

### Versijos ###

- Python 2.0 buvo išleista 2000 m. spalio 16 d.
- Python 3.0 buvo išleista 2008 m. gruodžio 3 d.

## Kaip paleisti py failą ##

Norėdami patikrinti įdiegtą Python versiją, galite naudoti šią komandą:

```cmd
python --version
```

Taip bus išvesta versija konsolėje

```cmd
Python 3.7.4
```

Jei Python neįdiegtas jūsų kompiuteryje, galite eiti į [python.org](https://www.python.org/) ir atsisiųsti bei įdiegti Python, skirtą atitinkamai operacinei sistemai.

Norėdami vykdyti Python scenarijų, galite naudoti šią komandą:

```cmd
python helloworld.py
```

*helloworld.py* yra scenarijaus failas, kuriame yra šis kodas

```py
print("Hello World from Python")
```

Tai išspausdins šiuos konsolės lange.

```cmd
Hello World from Python
```

Pastaba: jei naudojate IDE, jie pateikia mygtukus ekrane arba skirtingus sparčiuosius klavišus, kad paleistumėte Python. Pavyzdžiui, latake rodomas paleidimo mygtukas su PyCharm redaktoriumi, leidžiančiu vykdyti Python scenarijų.

## PY failo formatas ##

Python buvo sukurtas taip, kad būtų skaitomas ir panašus į anglų kalbą ir matematiką. Python naudoja naujas eilutes, kad nurodytų visą komandą, o ne kabliataškius ar skliaustus, naudojamus kitose kalbose. Apimčių, kilpų ir funkcijų atveju Python remiasi įtrauka ir tarpais, o ne kitose kalbose naudojamais riestiniais skliaustais.

### Sintaksė ###

Toliau pateikiamas Python sintaksės pavyzdys.

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

## Nuorodos Nr.

- [Python (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

