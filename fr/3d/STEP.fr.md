---
date: 2019-10-11
keywords: step, .step, format de fichier step, comment ouvrir les fichiers step, extension .step, extension step
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier STEP
linktitle: STEP
description: "Découvrez le format de fichier STEP et les API qui peuvent créer et ouvrir des fichiers STEP."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Qu'est-ce qu'un fichier STEP ?

Le fichier STEP est un format d'échange de données largement utilisé pour la conception assistée par ordinateur (CAO). Elle a été normalisée en 1994 par le comité ISO sous le nom de "ISO 10303-21". L'ISO 10303-21 définit le mécanisme de codage pour représenter les données dans le langage de modélisation de données EXPRESS. Un fichier STEP est également appelé fichier p21 et fichier physique STEP. Les extensions de fichier utilisées pour le fichier STEP sont .stp et .step.

## Histoire de base

En 1994, la spécification originale de la partie 21 a été publiée. Il contient quelques bogues qui ont été corrigés par le corrigendum technique publié en 1996. La deuxième édition a été publiée en 2002 et comprenait le corrigendum et les extensions de plusieurs sections de données. La troisième édition a été publiée en 2016 et a ajouté des sections d'ancrage et de référence permettant de stocker des entités et des valeurs dans des fichiers externes. Le support UTF-8 a été ajouté des chaînes. Des signatures numériques ont été ajoutées pour vérifier le contenu du fichier et pour valider les informations d'identification. La prise en charge de la compression et du stockage de la structure d'échange à l'aide de ZIP a également été ajoutée.

## Format de fichier STEP

Le format de texte brut d'un fichier STEP consiste en une séquence d'enregistrements. Le jeu de caractères est défini sous forme de points de code de la norme ISO 10646. "ISO-10303-21 ;" sont les premiers caractères du premier enregistrement. Les commentaires sont entourés des caractères "/*" et "*/". Le dernier enregistrement contient "END-ISO-10303-21 ;" si le fichier STEP est conforme à la version 2002. Dans le cas où il est conforme à la version 2016, il peut y avoir une ou plusieurs signatures numériques après le "END-ISO-10303-21 ;" terminateur. Les sauts de ligne sont désignés par "\N\" et les sauts de page sont désignés par "\F\".

Le fichier STEP est divisé en sections et leurs noms sont des termes réservés. Toutes les sections se terminent par l'enregistrement "ENDSEC" et doivent être dans l'ordre indiqué ci-dessous.

- **HEADER** : Il s'agit d'une section obligatoire et non répétable. Il se compose des entités suivantes :
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR** : il s'agit d'une section non répétitive facultative qui a été introduite dans la version 2016. Il définit les noms externes des instances afin qu'elles puissent être référencées.
- **RÉFÉRENCE** : il s'agit d'une section facultative non répétitive qui a également été introduite dans la version 2016. Chaque entrée de cette section associe un nom d'instance d'entrée/valeur à une instance/valeur dans un fichier externe.
- **DATA** : il s'agit d'une section répétable facultative qui contient le contenu principal de l'instance de modèle.
- **SIGNATURE** : Il s'agit d'une section répétable facultative qui a été introduite dans la version 2016. Il détient la signature numérique pour vérifier le contenu du fichier ou pour valider les informations d'identification.

## Références

- [ISO 10303-21 - Wikipédia](https://en.wikipedia.org/wiki/ISO_10303-21)

