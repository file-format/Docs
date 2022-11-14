---
date: 2019-10-11
keywords: json, .json, format de fichier json, comment ouvrir des fichiers json, notation d'objet javascript, format de données json, format de fichier .json
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier JSON - Qu'est-ce qu'un fichier JSON ?
linktitle: JSON
description: "Découvrez le format de fichier JSON et les API qui peuvent créer et ouvrir des fichiers JSON."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Qu'est-ce qu'un fichier JSON ?

JSON (JavaScript Object Notation) est un format de fichier standard ouvert pour le partage de données qui utilise du texte lisible par l'homme pour stocker et transmettre des données. Les fichiers JSON sont stockés avec l'extension .json. JSON nécessite moins de formatage et constitue une bonne alternative pour [XML](/fr/web/xml/). JSON est dérivé de JavaScript mais est un format de données indépendant du langage. La génération et l'analyse de JSON sont prises en charge par de nombreux langages de programmation modernes. *application/json* est le type de média utilisé pour JSON.

## Format de fichier JSON - Bref historique

Il y avait un besoin de communication serveur-client en temps réel qui a conduit à la création de JSON. Le format JSON a été spécifié pour la première fois par Douglas Crockford en mars 2001. JSON était basé sur la norme ECMA-262 3e édition, décembre 1999, qui est un sous-ensemble de JavaScript.

La première édition de la norme JSON ECMA-404 a été publiée en octobre 2013 par Ecma International. La RFC 7159 est devenue la principale référence pour les usages Internet de JSON en 2014. En novembre 2017, l'ISO/IEC 21778:2017 a été publiée en tant que norme internationale. La RFC 8259 a été publiée le 13 décembre 2017 par The Internet Engineering Task Force, qui est la version actuelle de la norme Internet STD 90.

## Structure des fichiers JSON

Les données JSON sont écrites dans des paires **clé/valeur**. La clé et la valeur sont séparées par deux-points (:) au milieu avec la clé à gauche et la valeur à droite. Les différentes paires clé/valeur sont séparées par une virgule (,). La clé est une chaîne entourée de guillemets doubles, par exemple "nom". Les valeurs peuvent être des types suivants.

- 'Numéro'
- `String` : séquence de caractères Unicode entourée de guillemets doubles.
- 'Booléen' : vrai ou faux.
- `Array` : une liste de valeurs entourées de crochets, par exemple

```json
[ "Pomme", "Banane", "Orange" ]
```

- `Object` : une collection de paires clé/valeur entourées d'accolades, par exemple

```json
{"name": "Jack", "age": 30, "Sport préféré" : "Football"}
```

Les objets JSON peuvent également être imbriqués pour représenter la structure des données. Vous trouverez ci-dessous un exemple d'objet JSON.

### Exemple de format JSON

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Quelle est la taille maximale du fichier JSON ?

Il n'y a pratiquement aucune limite à la taille maximale d'un fichier JSON. Elle peut être aussi longue que l'espace requis par le contenu à stocker.

Lorsqu'il s'agit d'utiliser le format de fichier JSON pour transférer des données sur Internet, il faut faire attention aux ressources disponibles de l'ordinateur. Si des données JSON volumineuses sont transférées, le transfert sera affecté si le navigateur client dispose d'une mémoire limitée.


Il n'y a pas de limite stricte définie par les spécifications, mais vous devez faire attention à ne pas épuiser les ressources sur les ordinateurs de vos utilisateurs, car cela dégradera rapidement leur expérience utilisateur et ils seront susceptibles d'abandonner votre application.

## JSON contre XML

**XML** est un autre format de fichier courant et largement utilisé pour l'échange de données sur Internet. Lorsqu'il s'agit d'échanger des données entre applications, les développeurs ont la possibilité d'utiliser les formats de fichiers XML et JSON. Cependant, JSON est adopté comme le moyen le plus pratique pour l'échange de données entre les applications sur Internet pour les raisons suivantes.

1. JSON donne une vue claire et plus facile à lire des données par rapport aux formats de fichiers XML
1. JSON réduit la surcharge de transfert de données sur Internet car il a moins de caractères pour définir le même ensemble de données par rapport à XML
1. Les langages de programmation modernes fournissent des analyseurs intégrés pour analyser la réponse JSON sur le Web.

## Le saviez-vous?

Vous pouvez devenir un contributeur sur FileFormat.com pour tenir la communauté des formats de fichiers au courant de vos découvertes. Si vous devez partager quoi que ce soit sur les formats de fichiers JSON ou Web, vous pouvez publier vos découvertes dans la section [Nouvelles sur les formats de fichiers Web](https://news.fileformat.com/t/Web) pour que les utilisateurs puissent en savoir plus.

## Références

- [JSON - Wikipédia](https://en.wikipedia.org/wiki/CSS)
- [Une introduction à JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

