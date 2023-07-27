---
date: 2020-11-11
keywords: myi, .myi, format de fichier myi, comment ouvrir les fichiers myi, extension .myi, extension myi
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier MYI
linktitle: MYI
description: "Découvrez le format de fichier MYI et les API qui peuvent créer et ouvrir des fichiers MYI."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Qu'est-ce qu'un fichier MYI ? ##

MYI est également connu sous le nom de fichier d'index MySQL MyISAM. Il est utilisé pour stocker les index de la table MyISAM par MySQL. L'index de la base de données MySQL définit la structure de la table et contient le mécanisme de contrôle pour vérifier l'intégrité des tables.

## Format de fichier MYI ##

Le fichier MYI comporte deux parties, l'en-tête et les valeurs de clé.

### En-tête MYI ###

L'en-tête contient des informations sur les options, la taille des fichiers et les clés. Les clés dans MySQL sont créées avec une commande comme

```sql
CREATE [UNIQUE] INDEX.
```

Les fichiers qui lisent et écrivent les fichiers MYI se trouvent dans le répertoire ./myisam. Il contient les fichiers suivants :

- mi_open.c : Ce fichier contient les routines qui écrivent chaque section de l'en-tête.
- mi_create.c : ce fichier contient les routines qui appellent les routines mi_open.c.
- myisamdef.h : Ce fichier contient les définitions de structure.

L'en-tête comporte les sections suivantes :

- état : L'état est écrit par mi_open.c, mi_state_info_write(). Cette structure apparaît une fois dans le fichier.
- base : La base est écrite par mi_open.c, mi_base_info_write(). Le MI_BASE_INFO est la structure correspondante pour la base dans myisamdef.h. Cette structure apparaît une fois dans le fichier.
- keydef : Le keydef est écrit par mi_open.c, mi_keydef_write(). Le MI_KEYDEF est la structure correspondante pour le keydef dans myisamdef.h. Il s'agit d'une structure à occurrences multiples qui apparaît pour chaque index.
- recinfo : Le recinfo est écrit par mi_open.c, mi_recinfo_write(). Le MI_COLUMNDEF est la structure correspondante pour le recinfo dans myisamdef.h. Il s'agit d'une structure à occurrences multiples qui apparaît une fois pour chaque champ apparaissant dans une clé.

### Valeurs clés ###

Les pages dans MySQL sont appelées blocs. Les valeurs clés sont en blocs. Un bloc contient des informations provenant d'un seul index. Chaque clé contient le contenu entier de toutes les colonnes. La longueur de bloc normale est de 0x0400 (1024) octets. Le pointeur a un numéro de taille fixe (4 octets) pour les tables à lignes fixes qui contient un numéro de ligne ordinal. Si la clé est nulle, l'octet est 0x00. Un bloc normal est plein à au moins 65 % et généralement à 80 %.

Le fichier myisamdef.h contient les informations suivantes exprimées en constantes. Le nombre maximal de clés est de 32 (MI_MAX_KEY) et le nombre maximal de segments dans une clé est de 16 (MI_MAX_KEY_SEG). La longueur maximale de la clé est de 500 (MI_MAX_KEY_LENGTH). La longueur maximale du bloc est de 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Références ##

- [Le fichier .MYI](https://dev.mysql.com/doc/dev/mysql-server/latest/)

