---
date: 2019-10-11
keywords: py, python, .py, py file format, how to open py file, how to run py files, how to run python files, how to run python
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PY faila veidlapaat
linktitle: PY
description: Lnopelniet par PY faila formātu un API, kas var izveidot un atvērt PY failus.
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## Kas ir PY fails? ##

Faili ar paplašinājumu .py satur Python avota kodu. Python valoda mūsdienās ir kļuvusi ļoti slavena valoda. To var izmantot sistēmas skriptēšanai, tīmekļa un programmatūras izstrādei un matemātikai. Python atbalsta vairāku platformu saderību; nozīmē, ka Python izstrādātās lietojumprogrammas var darboties dažādās platformās, piemēram, Windows, MAC, Linux, Raspberry Pi uc Python nodrošina vienkāršu un viegli lasāmu sintakse, kas ir līdzīga angļu valodai. Izstrādātāji var uzrakstīt saprātīgu lietojumprogrammu, ierakstot dažas Python koda rindiņas. Tā kā Python darbojas tulku sistēmā, kodu var izpildīt, tiklīdz tas ir uzrakstīts, kas padara to par ļoti labu prototipu veidošanai.

## Īsa vēsture ##

Python was conceived in the late 1980s by Guido van Rossum as a successor to ABC programming language. Its implementation began in December 1989 with Van Rossum as the sole lead developer. He worked on python until 12 July 2018. 2019. gada janvārī aktīvie Python kodola izstrādātāji ievēlēja piecu locekļu vadības padomi, kurā bija Niks Koglens, Brets Kanons, Kerola Vilinga, Berijs Varšava un Van Rosums, lai vadītu projektu.

### Versijas ###

- Python 2.0 tika izlaists 2000. gada 16. oktobrī.
- Python 3.0 tika izlaists 2008. gada 3. decembrī.

## Kā palaist py failu ##

Lai pārbaudītu instalēto Python versiju, varat izmantot šādu komandu:

```cmd
python --version
```

Tas izvadīs versiju konsolē, piemēram

```cmd
Python 3.7.4
```

Ja Python jūsu datorā nav instalēts, varat doties uz vietni [python.org](https://www.python.org/) un lejupielādēt un instalēt Python savai atbilstošajai operētājsistēmai.

Lai izpildītu Python skriptu, varat izmantot šādu komandu:

```cmd
python helloworld.py
```

*helloworld.py* ir skripta fails, kas satur šādu kodu

```py
print("Hello World from Python")
```

Tas konsoles logā izdrukās tālāk norādīto.

```cmd
Hello World from Python
```

Piezīme. Ja izmantojat IDE, tie nodrošina pogas uz ekrāna vai dažādus īsinājumtaustiņus, lai palaistu Python. Piemēram, teknē ar PyCharm redaktoru tiek parādīta atskaņošanas poga, kas ļauj izpildīt Python skriptu.

## PY faila formāts ##

Python tika izstrādāts lasāmībai, un tam ir līdzības ar angļu valodu un matemātiku. Python izmanto jaunas rindas, lai norādītu visu komandu, nevis semikolu vai iekavas, ko izmanto citās valodās. Attiecībā uz tvērumiem, cilpām un funkcijām Python izmanto atkāpes un atstarpes, nevis citās valodās izmantotās cirtaini iekavās.

### Sintakse ###

Tālāk ir sniegts Python sintakses piemērs.

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

## Atsauces Nr.

- [Python (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

