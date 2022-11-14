---
date: 2019-10-11
keywords: py, python, .py, format de fichier py, comment ouvrir un fichier py, comment exécuter des fichiers py, comment exécuter des fichiers python, comment exécuter python
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier PY
linktitle: PY
description: "Découvrez le format de fichier PY et les API qui peuvent créer et ouvrir des fichiers PY."
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## Qu'est-ce qu'un fichier PY ? ##

Les fichiers avec l'extension .py contiennent le code source Python. Le langage Python est devenu un langage très célèbre de nos jours. Il peut être utilisé pour les scripts système, le développement Web et logiciel et les mathématiques. Python prend en charge la compatibilité multiplateforme ; signifie que les applications développées en Python peuvent fonctionner sur différentes plates-formes telles que Windows, MAC, Linux, Raspberry Pi, etc. Python fournit une syntaxe simple et facile à lire, similaire à la langue anglaise. Les développeurs peuvent écrire une application logicielle raisonnable en écrivant quelques lignes de code Python. Étant donné que Python fonctionne sur un système d'interprétation, le code peut être exécuté dès qu'il est écrit, ce qui le rend très bon pour le prototypage.

## Bref historique ##

Python a été conçu à la fin des années 1980 par Guido van Rossum comme successeur du langage de programmation ABC. Sa mise en œuvre a commencé en décembre 1989 avec Van Rossum comme seul développeur principal. Il a travaillé sur python jusqu'au 12 juillet 2018. En janvier 2019, les développeurs actifs du noyau Python ont élu un "Conseil directeur" de cinq membres composé de Nick Coghlan, Brett Cannon, Carol Willing, Barry Warsaw et Van Rossum pour diriger le projet.

### Versions ###

- Python 2.0 est sorti le 16 octobre 2000.
- Python 3.0 est sorti le 3 décembre 2008.

## Comment exécuter le fichier py ##

Pour vérifier la version de Python installée, vous pouvez utiliser la commande suivante :

```cmd
python --version
```

Cela affichera la version sur la console comme

```cmd
Python 3.7.4
```

Si Python n'est pas installé sur votre machine, vous pouvez accéder à [python.org](https://www.python.org/) et télécharger et installer Python pour votre système d'exploitation concerné.

Pour exécuter un script Python, vous pouvez utiliser la commande suivante :

```cmd
python helloworld.py
```

*helloworld.py* est un fichier de script qui contient le code suivant

```py
print("Hello World from Python")
```

Cela imprimera ce qui suit sur la fenêtre de la console.

```cmd
Hello World from Python
```

Remarque : Si vous utilisez des IDE, ils fournissent des boutons à l'écran ou différents raccourcis clavier pour exécuter Python. Par exemple, un bouton de lecture est affiché dans la gouttière avec l'éditeur de PyCharm qui vous permet d'exécuter le script Python.

## Format de fichier PY ##

Python a été conçu pour la lisibilité et présente des similitudes avec l'anglais et les mathématiques. Python utilise de nouvelles lignes pour indiquer la commande complète par opposition aux points-virgules ou aux parenthèses utilisés dans d'autres langages. Pour les portées, les boucles et les fonctions, Python s'appuie sur l'indentation et les espaces blancs par opposition aux accolades utilisées dans d'autres langages.

### Syntaxe ###

Voici un exemple de syntaxe Python.

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

## Références ##

- [Python (langage de programmation) - Wikipédia](https://en.wikipedia.org/wiki/Python_(langage_de_programmation))

