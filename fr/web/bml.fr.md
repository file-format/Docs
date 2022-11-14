{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier BML - Fichier de langage de balisage de bean",
  "description":"En savoir plus sur le format de fichier BML et les API qui peuvent créer et ouvrir des fichiers BML.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## Qu'est-ce qu'un fichier BML ?

Un fichier avec l'extension .bml est un fichier Bean Markup Language qui stocke les classes Java pour la prise en charge des applications Java. Cela permet d'accéder aux objets et aux méthodes Java et n'a pas besoin de créer de nouvelles fonctionnalités à l'aide de classes Java. Il spécifie comment les composants sont connectés les uns aux autres pour effectuer des tâches utiles. BML a été développé par IBM alphaWorks pour décrire les relations entre les structures et les composants. Les fichiers BML peuvent être ouverts et visualisés à l'aide de n'importe quel éditeur de texte tel que les navigateurs Web, Microsoft Notepad et Notepad ++.

## Format de fichier BML

Le site Web IBM alphaworks a fourni deux implémentations de BML. La première implémentation est un interpréteur qui "joue" un script BML pour générer la hiérarchie de bean souhaitée. La deuxième implémentation est un compilateur qui compile n'importe quel script BML en code Java sans réflexion. Ceci est avantageux dans le sens où cela permet de capturer la structure inter-composants de l'application à l'aide d'un langage conçu à cet effet spécifique avec la possibilité supplémentaire de le compiler en code Java "normal".

## Balises BML

Voici une explication de certaines des balises utilisées dans le langage BML :

### La<bean> étiquette:

La<bean> L'élément est utilisé pour créer de nouveaux beans ou pour rechercher des beans par leur nom. La<bean> la balise est au format :
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
Le "id" dans la balise est associé au registre d'objets pour le JavaBean.

### La<string> étiquette

La balise de chaîne peut être utilisée de deux manières :

1. Pour créer une chaîne non vide :

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Pour créer une chaîne vide :

```
<string/>
```
## Références

* [Messagerie orientée objet avec XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [Le langage de balisage physique](http://web.mit.edu/mecheng/pml/standards.htm)
* [Le langage de balisage Bean] (https://all4dev.blogspot.com/2019/06/bean-markup-language-tutorial.html)

