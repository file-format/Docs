{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier AGI - Format de fichier d'interface de passerelle Asterisk",
  "description":"Découvrez ce qu'est le format de fichier AGI avec des exemples et des API qui peuvent créer et ouvrir des fichiers AGI.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Qu'est-ce qu'un fichier AGI ?

Un fichier AGI est un fichier de script utilisé par le système de téléphonie open source, Asterisk. Il contient des informations qui peuvent être utilisées pour automatiser les processus et le plan de numérotation Asterisk. À l'aide de fichiers de script AGI, des connexions peuvent être établies avec des bases de données relationnelles telles que PostgreSQL ou MySQL. De plus, les scripts AGI peuvent également être utilisés pour accéder à d'autres ressources externes. Les scripts AGI peuvent confier le contrôle du plan de numérotation à un script AGI externe, permettant à Asterisk d'effectuer des tâches complexes.

## Format de fichier AGI - Plus d'informations

Les fichiers de script AGI sont enregistrés sous forme de fichiers texte et peuvent être ouverts dans n'importe quel éditeur de texte pour apporter des modifications.

### Modèle standard de communication AGI

Le script AGI charge les variables et leurs valeurs qui lui sont envoyées par Asterisk. Un aspect commun de ces variables est le suivant.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Ces variables sont suivies d'une ligne blanche envoyée par Asterisk, indiquant que le script AGI peut prendre le contrôle du plan de numérotation maintenant.

### Langage de programmation pour les fichiers de script AGI

Les scripts AGI peuvent généralement être écrits en Perl, [PHP](/fr/programming/php/), [C](/fr/programming/c/), Pascal ou Bourne Shell.

## Références

* [Script AGI Asterisk](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

