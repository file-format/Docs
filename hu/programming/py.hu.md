---
date: 2019-10-11
keywords: py, python, .py, py fájlformátum, py fájl megnyitása, py fájlok futtatása, python fájlok futtatása, python futtatása
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PY fájlformátum
linktitle: PY
description: "Ismerje meg a PY fájlformátumot és az API-kat, amelyek PY fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## Mi az a PY fájl? ##

A .py kiterjesztésű fájlok a Python forráskódot tartalmazzák. A Python nyelv manapság nagyon híres nyelvvé vált. Használható rendszerszkriptezéshez, web- és szoftverfejlesztéshez, valamint matematikához. A Python támogatja a platformok közötti kompatibilitást; azt jelenti, hogy a Pythonban kifejlesztett alkalmazások különböző platformokon működhetnek, mint a Windows, MAC, Linux, Raspberry Pi stb. A Python egyszerű és könnyen olvasható szintaxist biztosít, amely hasonló az angol nyelvhez. A fejlesztők ésszerű szoftveralkalmazást tudnak írni néhány sor Python kód írásával. Mivel a Python értelmező rendszeren fut, így a kód azonnal végrehajtható a megírása után, ami nagyon jó prototípus készítéshez.

## Rövid története ##

A Pythont az 1980-as évek végén Guido van Rossum tervezte az ABC programozási nyelv utódjaként. Megvalósítása 1989 decemberében kezdődött, Van Rossum volt az egyedüli vezető fejlesztő. 2018. július 12-ig dolgozott a pythonon. 2019 januárjában az aktív Python-mag fejlesztők egy öttagú "Irányító Tanácsot" választottak, amely Nick Coghlanből, Brett Cannonból, Carol Willingből, Barry Warsawból és Van Rossumból állt a projekt élére.

### Verziók ###

- A Python 2.0 2000. október 16-án jelent meg.
- A Python 3.0 2008. december 3-án jelent meg.

## A ## py fájl futtatása

A telepített Python verziójának ellenőrzéséhez használja a következő parancsot:

```cmd
python --version
```

Ez kiírja a verziót a konzolon, mint például

```cmd
Python 3.7.4
```

Ha a Python nincs telepítve a gépére, felkeresheti a [python.org](https://www.python.org/) webhelyet, és letöltheti és telepítheti a Python-t a megfelelő operációs rendszerhez.

Python-szkript futtatásához a következő parancsot használhatja:

```cmd
python helloworld.py
```

A *helloworld.py* egy szkriptfájl, amely a következő kódot tartalmazza

```py
print("Hello World from Python")
```

Ezzel a következőt nyomtatja ki a konzolablakba.

```cmd
Hello World from Python
```

Megjegyzés: Ha IDE-ket használ, gombokat vagy különböző billentyűparancsokat biztosítanak a képernyőn a Python futtatásához. Például egy lejátszás gomb látható a PyCharm szerkesztőjének csatornájában, amely lehetővé teszi a Python-szkript végrehajtását.

## PY fájlformátum ##

A Pythont az olvashatóságra tervezték, és hasonlóságokat mutat az angolhoz és a matematikához. A Python új sorokat használ a teljes parancs jelzésére, szemben a más nyelvekben használt pontosvesszőkkel vagy zárójelekkel. A hatókörök, ciklusok és függvények esetében a Python a behúzásra és a szóközökre támaszkodik, szemben a más nyelvekben használt kapcsos zárójelekkel.

### Szintaxis ###

A következő egy példa a Python szintaxisra.

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

## Hivatkozások ##

- [Python (programozási nyelv) - Wikipédia](https://en.wikipedia.org/wiki/Python_(programming_language))

