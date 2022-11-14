---
date: 2019-10-11
keywords: toml, .toml, format de fichier toml, comment ouvrir les fichiers toml, extension .toml, extension toml
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier TOML
linktitle: TOML
description: "Découvrez le format de fichier TOML et les API qui peuvent créer et ouvrir des fichiers TOML."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Qu'est-ce qu'un fichier TOML ? ##

TOML (Tom's Obvious Minimal Language) est un format de fichier de configuration minimal qui utilise l'extension .toml. TOML vise à être facile à lire, à mapper sans ambiguïté sur les dictionnaires et à être facile à analyser dans différentes structures de données. TOML a une spécification open-source qui a reçu des contributions de la communauté. TOML est pris en charge par de nombreux langages de programmation tels que C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift, etc. Le type MIME pour les fichiers TOML est *application/toml*.


## Format de fichier TOML ##

Les fichiers TOML se composent principalement de paires clé/valeur, de sections/tables, de commentaires et doivent être un document Unicode encodé UTF-8 valide. TOML prend en charge les types de données String, Integer, Float, Boolean, Datetime, Array et Table (hash table/dictionary). TOML est un langage sensible à la casse.

### Syntaxe ###

- **Paires clé-valeur** : les paires clé-valeur sont séparées par le signe égal (=). Chaque paire doit être sur une nouvelle ligne.

```toml
premier = "Tom"
dernier = "Preston-Werner"
```

- **Commentaires** : les commentaires commencent par le symbole dièse (#).

```toml
# Ceci est un document TOML.
```

- **Chaînes** : les chaînes sont entourées de guillemets (").

```toml
string = "Exemple de chaîne"
```

- **Chaînes multilignes** : les chaînes multilignes sont entourées de trois guillemets (""").

```toml
[adresse du domicile]
rue = """123 Allée des Tornades
Suite 16"""
city = "East Centerville"
état = "KS"
```

- **Entiers/Flottants**

```toml
entier = 20
flottant = 20,5
```

- **Booléens** : les booléens sont toujours en minuscules.

```toml
bool1 = vrai
bool2 = faux
```

- **Date-Heure** : Pour DateTime, vous pouvez utiliser une date-heure au format RFC 3339, comme indiqué dans l'exemple ci-dessous.

```toml
décalage_date_heure = 1979-05-27 07:32:00Z
date_heure_locale = 27/05/1979T07:32:00
date_locale = 1979-05-27
heure_locale = 07:32:00
```

- **Tableaux** : les tableaux sont entourés de crochets avec des éléments séparés par des virgules (,).

```toml
couleurs = [ "rouge", "jaune", "vert" ]
```

- **Tableaux** : les tableaux sont des ensembles de paires clé/valeur définies par des en-têtes sur une nouvelle ligne entourés de crochets ([]). Le tableau se termine lorsqu'un nouvel en-tête est fourni ou lorsque le fichier se termine.

```toml
[adresse du domicile]
rue = """123 Allée des Tornades
Suite 16"""
city = "East Centerville"
état = "KS"

[Adresse de bureau]
rue = """123 Allée des Tornades
Suite 16"""
city = "East Centerville"
état = "KS"
```

Les tableaux en ligne sont entourés d'accolades ({}) avec chaque paire clé/valeur séparée par une virgule (,).

```toml
nom = { premier = "Tom", dernier = "Pitt" }
```

## Références ##

- [TOML - Wikipédia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

