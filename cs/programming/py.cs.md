---
date: 2019-10-11
keywords: py, python, .py, py formát souboru, jak otevřít soubor py, jak spustit soubory py, jak spustit soubory python, jak spustit python
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru PY
linktitle: PY
description: "Přečtěte si o formátu souboru PY a rozhraních API, která mohou vytvářet a otevírat soubory PY."
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## Co je soubor PY? ##

Soubory s příponou .py obsahují zdrojový kód Pythonu. Jazyk Python se stal dnes velmi známým jazykem. Může být použit pro systémové skriptování, vývoj webu a softwaru a matematiku. Python podporuje kompatibilitu napříč platformami; znamená, že aplikace vyvinuté v Pythonu mohou pracovat na různých platformách, jako jsou Windows, MAC, Linux, Raspberry Pi atd. Python poskytuje jednoduchou a snadno čitelnou syntaxi, která je podobná angličtině. Vývojáři mohou napsat rozumnou softwarovou aplikaci napsáním několika řádků kódu Pythonu. Vzhledem k tomu, že Python běží na interpretačním systému, lze kód spustit, jakmile je napsán, což jej činí velmi dobrým pro prototypování.

## Stručná historie ##

Python byl koncipován koncem 80. let Guido van Rossumem jako nástupce programovacího jazyka ABC. Jeho implementace začala v prosinci 1989 s Van Rossumem jako jediným vedoucím vývojářem. Na pythonu pracoval do 12. července 2018. V lednu 2019 aktivní vývojáři jádra Pythonu zvolili pětičlennou „Řídící radu“ ve složení Nick Coghlan, Brett Cannon, Carol Willing, Barry Warsaw a Van Rossum, aby projekt vedli.

### Verze ###

- Python 2.0 byl vydán 16. října 2000.
- Python 3.0 byl vydán 3. prosince 2008.

## Jak spustit py soubor ##

Chcete-li zkontrolovat nainstalovanou verzi Pythonu, můžete použít následující příkaz:

```cmd
python --version
```

Tím se vydá verze na konzoli jako

```cmd
Python 3.7.4
```

Pokud Python na vašem počítači není nainstalován, můžete přejít na [python.org](https://www.python.org/) a stáhnout a nainstalovat Python pro váš příslušný operační systém.

Chcete-li spustit skript Python, můžete použít následující příkaz:

```cmd
python helloworld.py
```

*helloworld.py* je soubor skriptu, který obsahuje následující kód

```py
print("Hello World from Python")
```

To vytiskne následující v okně konzoly.

```cmd
Hello World from Python
```

Poznámka: Pokud používáte IDE, poskytují tlačítka na obrazovce nebo různé klávesové zkratky pro spuštění Pythonu. Například tlačítko přehrávání je zobrazeno ve sloupci s editorem v PyCharm, který vám umožňuje spustit skript Python.

## Formát souboru PY ##

Python byl navržen pro čitelnost a má podobnosti s angličtinou a matematikou. Python používá nové řádky k označení celého příkazu na rozdíl od středníků nebo závorek používaných v jiných jazycích. U oborů, smyček a funkcí se Python spoléhá na odsazení a mezery na rozdíl od složených závorek používaných v jiných jazycích.

### Syntaxe ###

Následuje příklad syntaxe Pythonu.

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

## Reference ##

- [Python (programovací jazyk) - Wikipedie](https://en.wikipedia.org/wiki/Python_(programming_language))

