{
"date": "2023-05-29",
  "keywords": [
"fichier rb",
"qu'est-ce qu'un fichier rb",
"comment exécuter le script Ruby dans le fichier RB",
"que contient le fichier rb",
"quel est le format du fichier rb",
"déposer",
"extension de fichier rb",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier RB - Fichier de code source Ruby",
  "description":"Découvrez le format RB et les API permettant de créer et d'ouvrir des fichiers RB.",
"linktitle": "RB",
  "menu": {
    "docs": {
      "identifier": "programming-rb",
"parent": "programmation"
}
},
"derniermod": "2023-05-29"
}

## Qu'est-ce qu'un fichier RB ?

Une extension de fichier « .rb » est généralement associée aux fichiers du langage de programmation Ruby. Ruby est un langage de programmation dynamique orienté objet connu pour sa simplicité et sa lisibilité.

Un fichier ".rb" contient du code source Ruby, qui peut être exécuté par un interpréteur Ruby ou un environnement de développement Ruby. Ces fichiers contiennent souvent des définitions de classes, méthodes, variables et autres constructions de code Ruby.

## Comment exécuter le script Ruby dans un fichier RB ?

Pour exécuter un script Ruby enregistré dans le fichier ".rb", vous aurez besoin d'un interpréteur Ruby installé sur votre système. Voici un exemple de base de script Ruby enregistré dans un fichier nommé « example.rb » :

```
# example.rb

# Define a method to calculate the square of a number
def square(number)
  number * number
end

# Call the square method with an argument
result = square(5)

# Print the result
puts "The square of 5 is: #{result}"
```

Pour exécuter ce script, vous pouvez ouvrir votre ligne de commande ou votre terminal, accéder au répertoire où se trouve le fichier "example.rb", puis utiliser l'interpréteur Ruby :

```
ruby example.rb
```

L'exécution de la commande ci-dessus exécutera le script et le résultat sera affiché dans la console :

```
The square of 5 is: 25
```

Il s'agit d'un exemple simple, mais les fichiers « .rb » peuvent contenir du code plus complexe, notamment des classes, des modules et des structures de contrôle, vous permettant de créer des applications Ruby à part entière.

## Que contient le fichier RB ?

Le contenu spécifique du fichier ".rb" peut varier en fonction de son objectif et du programmeur qui l'a écrit. Cependant, en général, le fichier « .rb » contient le code source Ruby, qui consiste en une série d’instructions que l’interpréteur Ruby peut comprendre et exécuter.

Voici quelques éléments courants que vous pourriez trouver dans le fichier Ruby :

- **Commentaires :** Ruby prend en charge les commentaires sur une seule ligne et sur plusieurs lignes. Les commentaires sont utilisés pour ajouter des notes explicatives ou désactiver l’exécution de lignes de code spécifiques. Ils sont désignés par le caractère #.

```
# This is a single-line comment

=begin
This is a
multi-line comment
=end
```

- **Déclarations de variables :** Ruby est un langage typé dynamiquement, les variables n'ont donc pas besoin de déclarations de type explicites. Vous pouvez attribuer des valeurs aux variables à l'aide de l'opérateur d'affectation (=).

- **Méthodes :** Ruby utilise le mot-clé `def` pour définir des méthodes, qui sont des blocs de code réutilisables qui effectuent des tâches spécifiques.

- **Classes et objets :** Ruby est un langage orienté objet et les classes sont utilisées pour définir des plans d'objets. Les objets sont des instances de classes et peuvent avoir des attributs (variables d'instance) et des comportements (méthodes d'instance).

- **Structures de contrôle :** Ruby fournit diverses structures de contrôle telles que des instructions conditionnelles (si, sinon, elsif, sauf), des boucles (pendant que, jusqu'à, pour, chacun) et bien plus encore, pour contrôler le flux d'exécution dans le programme.

```
if age >= 18
  puts "You are an adult."
else
  puts "You are a minor."
end

# Output: You are an adult.
```

## Quel est le format du fichier RB ?

Le format du fichier « .rb » est du texte brut, généralement codé en UTF-8 ou ASCII. Il suit une syntaxe et une structure spécifiques définies par le langage de programmation Ruby.

## Quel est le type MIME du fichier RB ?

- `application/x-ruby`

## Les références
* [Ruby (langage de programmation)](https://en.wikipedia.org/wiki/Ruby_(programming_langage))

