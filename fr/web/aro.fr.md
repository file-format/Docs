{
  "date" : "2021-12-09",
  "keywords" :[ "aro","fichier .aro", "format de fichier aro", "un type de fichier", "fichier", "type", "qu'est-ce qu'un fichier .aro" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier ARO - Fichier d'application Web SteelArrow",
  "description" :"Découvrez ce qu'est un fichier ARO et les API qui peuvent créer et ouvrir des fichiers ARO.",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Qu'est-ce qu'un fichier ARO ?

Un fichier ARO est un fichier de page Web côté serveur généré avec SteelArrow Web Application. Il contient des balises et des scripts [HTML](/fr/web/html/) et SteelArrow. Ceux-ci sont exécutés sur le serveur pour générer une page de réponse complète avant de les envoyer au navigateur de l'utilisateur. Les fichiers ARO contiennent près de 95 % du contenu HTML, tandis que le reste est constitué de code SteelArrow. Pour que les fichiers ARO fonctionnent pour vous, le serveur d'applications Web SteelArrow doit être installé et exécuté sur la machine du serveur Web.

## Format de fichier ARO

Les fichiers ARO sont écrits dans un fichier de langage de balisage HTML avec du code JavaScript intégré et des applets Java. [Les balises SteelArrow](http://www.steelarrow.com/docs/basics1.aro) sont les éléments de base pour le développement de pages Web. Bien que ceux-ci ne modifient pas l'affichage de la page, ils sont utilisés pour remplir la page avec des données. En outre, ils peuvent également être utilisés pour contrôler la sortie avec des instructions conditionnelles.

### Exemple de balise ARO

La<SAOUTPUT> La balise ARO permet aux développeurs de générer des valeurs de données à n'importe quel endroit d'un script. Par exemple, il peut être utilisé pour obtenir la sortie de la table PARAM avec<SAOUTPUT VALUE=PARAM[]> qui peut être affiché dans le HTML<BODY> étiquette.

## Références

* [Balises SteelArrow](http://www.steelarrow.com/docs/basics.aro)

