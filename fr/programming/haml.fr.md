{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier HAML - Fichier de code source Haml",
  "description":"En savoir plus sur le format de fichier HAML et les API qui peuvent créer et ouvrir un fichier HAML.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## Qu'est-ce qu'un fichier HAML ?

Un fichier HAML est un fichier de langage de balisage d'abstraction HTML qui contient le code source écrit en langage [Haml](https://haml.info/). Il peut être utilisé en remplacement de l'ERB (scripts de modèle Ruby). Le fichier HAML contient le code source du modèle permettant de générer le code HTML d'un document Web. Les fichiers ERB peuvent être remplacés en remplaçant simplement ces fichiers dans le dossier app/views par Haml en modifiant l'extension du fichier. Les fichiers HAML peuvent être ouverts avec n'importe quel éditeur de texte tel que Microsoft Notepad, Notepad ++, Apple TextEdit,

## Format de fichier HAML

Les fichiers HAML sont des fichiers source enregistrés sur le disque sous forme de fichiers texte brut. Il contient du code écrit en syntaxe HAML. HAML remplace les balises **<>** par le signe **%** pour rendre le code plus simple et plus facile. Les fichiers ERB sont remplaçables directement par HAML, comme illustré dans l'exemple simple suivant.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### Exemple HAML

Ce qui suit est un exemple Hello World de HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
qui restitue la sortie HTML suivante.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Références

* [HAML - Github](https://github.com/haml/haml)

