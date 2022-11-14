{
  "date" : "2021-06-30",
  "keywords" :[ "fichier mst", "format de fichier mst", "qu'est-ce qu'un fichier mst", "fichier", "exemple mst", "extension de fichier mst","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier MST et les API qui peuvent créer et ouvrir des fichiers MST.",
  "title" :"MST - Fichier de package d'installation Windows",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Qu'est-ce qu'un fichier MST ?
Les fichiers avec l'extension .mst sont utilisés pour transformer le contenu d'un package MSI. Ils sont couramment utilisés par les administrateurs système pour appliquer les paramètres personnalisés à un fichier MSI existant. Les fichiers MST sont utilisés avec le package MSI d'origine dans leurs systèmes de distribution de logiciels tels que les stratégies de groupe. Les fichiers MST sont généralement utilisés dans le développement et les tests de logiciels pour configurer leurs versions en cours de développement du logiciel.

## Format de fichier MST
Un fichier MST ou Transform est utilisé pour collecter les options d'installation des programmes qui utilisent Microsoft Windows Installer dans un fichier. Ces fichiers sont couramment utilisés sur la ligne de commande du programme d'installation (MSIEXEC.EXE) ou utilisés dans une stratégie de groupe d'installation de logiciels ; dans un domaine Microsoft Active Directory. Les fichiers MST peuvent également être utilisés avec des programmes d'installation exécutables enveloppés. Un cas général est que quelqu'un veut passer des paramètres de ligne de commande au programme d'installation encapsulé. Pour ce faire, vous avez besoin d'un fichier MST qui ajoute la propriété WRAPPED_ARGUMENTS à la table des propriétés. Ces fichiers ne peuvent pas être créés ou modifiés à l'aide d'éditeurs généraux. Des outils spécifiques sont disponibles à cet effet.

### Comment utiliser les fichiers MST ?
Les fichiers MST peuvent être générés à l'aide de divers outils et Ocra est généralement utilisé pour générer un fichier MST. Ensuite, les paramètres peuvent être personnalisés en fonction des besoins et enregistrés à un emplacement spécifique. Après cela, les fichiers MST peuvent être utilisés conjointement avec les fichiers MSI. Si vous voulez tester ces fichiers; utilisez la syntaxe suivante sur la ligne de commande

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### Propriété TRANSFORME

Vous pouvez également utiliser la propriété **TRANSFORMS** du programme d'installation de Windows qui est en fait une liste des transformations que le programme d'installation applique lors de l'installation du package. Le programme d'installation exécute les transformations dans le même ordre qu'elles sont répertoriées dans la propriété TRANSFORM. Les transformations peuvent être spécifiées par nom de fichier avec l'extension .mst ou le chemin complet. Pour spécifier plusieurs transformations, séparez chaque nom de fichier ou un point-virgule comme dans l'exemple suivant.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Références

* [Fichiers de transformation MST](https://www.exemsi.com/documentation/mst-transformation-files/)
* [Propriété TRANSFORMS](https://docs.microsoft.com/en-us/windows/win32/msi/transforms)


