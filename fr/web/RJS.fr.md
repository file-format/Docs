{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Fichier", "Extension", "Format de fichier", "Extension de fichier", "RJS", "Fichier Ruby Javascript"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Fichier Ruby Javascript",
  "description":"En savoir plus sur le format de fichier RJS et les API qui peuvent créer et ouvrir des fichiers RJS.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Qu'est-ce qu'un fichier RJS ?

Un fichier avec l'extension .rjs est une combinaison de code Ruby et JavsScript qui permet aux développeurs Rails d'utiliser Ruby pour produire du code JavaScript dynamique. Le code Ruby est intégré dans les fonctions Java et est compilé sur le serveur Web qui nécessite que le moteur Ruby soit exécuté sur le serveur. RJS est similaire à [RHTML](/fr/web/rhtml/); la seule différence est que le latéral contient du code Ruby dans [HTML](/fr/web/html/) alors qu'il contient du code Ruby dans les fonctions Javascript.

## Format de fichier RJS

Les fichiers RJS sont codés en texte brut comme tout autre langage de script ou de programmation. Lorsqu'une telle page est demandée par le client, le code Ruby est exécuté sur le serveur, et seuls les codes HTML et Javascript sont renvoyés au navigateur du client. La syntaxe du fichier RJS est similaire à celle de la combinaison de la syntaxe Ruby et JavaScript, de sorte que seul le code Ruby est intégré dans les fonctions JavaScript.

### Exemple RJS

L'exemple suivant montre un code Ruby simple indépendamment puis intégré dans une fonction JavaScript.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
et voici le RubyJS :
```Ruby
# here you go!

foo = -> { "bar" }
```
## Références

* [RJS](https://github.com/makevoid/rjs)

