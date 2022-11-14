{
  "date" : "2019-10-11",
  "keywords" :[ "XSLFO", "Objets de mise en forme XSL", "Fichier", "Extension", "Format de fichier", "Langage de feuille de style extensible"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"En savoir plus sur le format de fichier XSLFO et les API qui peuvent créer et ouvrir des fichiers XSLFO.",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Qu'est-ce qu'un fichier XSL-FO ? ##

XSL-FO (XSL Formatting Objects) est un puissant langage de feuille de style pour le formatage des documents XML. La sémantique de la forme délimitée du papier et de l'impression est exprimée par XSL-FO lorsque les dimensions sont fixes. Contrairement à HTML, qui représente la sémantique de la forme illimitée d'une fenêtre de navigateur aux dimensions variables. Les documents XML formatés par XSL-FO sont principalement utilisés pour générer des fichiers PDF. XSL (Extensible Stylesheet Language) est un ensemble de technologies W3C complètes en fonctionnalités destinées à la conception pour le formatage et l'échange de documents XML et XSL-FO faisant partie de ce langage. XSLT et XPath sont également d'autres parties de XSL.

Il est proposé que les documents XML soient d'abord transformés en XSL-FO, PDF étant un exemple de ce critère. En PDF, les résultats sont d'abord rendus à l'aide de XSLT, puis du formateur XSL-FO. De cette façon, les documents XML peuvent être formatés de manière aléatoire. Bien que XSL-FO profite de l'utilisation des propriétés de feuille de style en cascade (CSS) et de leur extension là où cela est nécessaire pour le format réel, il héberge la fourniture de modèles de page appelés maîtres de page dans la terminologie de XSL-FO. XSL-FO fournit également un formatage pour des documents assez sophistiqués et prend en charge la génération d'index.

## Histoire et concepts de base ##

En janvier 2012, le projet de travail de XSL-FO a été mis à jour pour la dernière fois, et en novembre 2013, son groupe de travail a été fermé. Une feuille de style XSL spécifie la présentation d'une classe de documents XML en décrivant comment une instance de la classe est transformée en un document XML qui utilise le vocabulaire de formatage. XSL-FO est un langage de présentation intégré et n'a pas de balisage sémantique utilisé en HTML. De plus, ce langage stocke toutes les données du document en lui-même, contrairement au CSS qui modifie les paramètres par défaut d'un document HTML ou XML externe.

Le critère général d'utilisation de XSL-FO est que l'utilisateur écrit un document dans un langage XML plutôt que d'écrire en FO. Après cela, une transformation XSLT se produit. Cette transformation XSLT est responsable de la conversion de XML en XSL-FO. Dès que le document XSL-FO est généré, il est alors transmis à une application appelée processeur FO. Les sous-traitants FO sont chargés de transformer ce document en un document lisible et imprimable. Les fichiers PDF ou PS sont des exemples de la sortie la plus courante de XSL-FO. Mais cela ne signifie pas que le processeur FO ne peut produire que ces deux types de format en sortie. Certains processeurs FO peuvent produire des fichiers RTF ou même une fenêtre peut apparaître dans l'interface graphique de l'utilisateur, cette fenêtre affiche la séquence de la page et son contenu.

Un document XSL-FO est différent d'un PDF ou d'un PS dans le sens où il ne définit finalement pas la disposition du texte sur différentes pages. Peut-être, il stylise les pages et détermine les endroits où afficher le contenu. De plus, un processeur FO organise le texte dans les limites spécifiées par le document FO. Cette spécification permet même à différents processeurs FO de se comporter en fonction des pages créées résultantes. Un exemple d'un tel comportement est la césure, peu de processeurs FO peuvent couper les mots afin d'économiser de l'espace lorsqu'une ligne saute, alors que certains processeurs ne sélectionnent pas cette option. Il appartient aux processeurs de choisir différents algorithmes de césure qui correspondent à leurs besoins. Ces algorithmes de césure peuvent être très simples ou peut-être plus complexes. Dans certaines situations, la spécification XSL-FO sanctionne explicitement les processeurs FO, un certain degré de choix dans le contexte de la mise en page.

Cette variation entre les processeurs FO génère des résultats variables, dont les processeurs restent souvent indifférents. Parce que l'objectif général de XSL-FO est de produire des documents paginés/imprimés. Les documents XSL-FO eux-mêmes agissent généralement comme des intermédiaires, leur fonction principale est de générer soit des fichiers PDF, soit un document qui peut être imprimé comme sortie à distribuer. En HTML/CSS ou XSL-FO, la distribution du PDF comme résultat final plutôt que la saisie du langage de formatage indique que les récepteurs ne sont pas affectés par la polyvalence résultante qui est produite en raison des différences entre les interprètes du langage de formatage. D'autre part, il est évident qu'il n'y a pas de moyen simple pour qu'un document puisse répondre aux différents besoins des destinataires, par exemple une taille de page variable ou une taille de police souhaitée, ou une personnalisation pour la page ou l'impression.

## Format de fichier XSLFO ##

Les documents SL-FO sont essentiellement des documents XML, mais ils ne suivent aucun schéma. A sa place, les documents SL-FO suivent la syntaxe définie dans la spécification de leur propre langage. Deux sections sont requises dans chaque document XSL-FO :

1. Une section qui spécifie une liste de mises en page étiquetées.
1. Une section avec tous les détails des données du document, avec un balisage, qui détermine l'affichage du contenu sur différentes pages à travers différentes mises en page.

Les propriétés de la page sont mentionnées dans les mises en page, qui peuvent définir l'organisation du texte, pour se conformer aux conventions de la langue spécifique. De plus, la taille de la page, leurs marges et les séquences de pages (qui sanctionnent des propriétés différentes pour les pages paires et impaires) sont également définies par les mises en page.

La partie données du document est divisée en une série de flux, où chaque flux est connecté à une mise en page. Les flux contiennent une liste de blocs. Cette liste de blocs peut contenir des fonctionnalités de balisage en ligne ou une liste de données textuelles, ou peut-être les deux en même temps. Les marges du document peuvent également afficher les numéros de page ou les titres de chapitre. La fonctionnalité des blocs et des éléments en ligne reste la même que dans le CSS, mais certaines règles de remplissage et de marge sont différentes entre FO et CSS.

Le sens d'orientation de la page est entièrement spécifié pour l'extension des blocs et des inlines, rendant ainsi les documents FO performants dans des langues différentes de l'anglais. Le langage de la spécification FO utilise les mots début et fin plutôt que gauche et droite pour la description des directions. Le balisage de contenu de base et les règles en cascade de XSL-FO sont tirés de CSS. Le langage XSL-FO accepte les spécifications suivantes.

## Plusieurs colonnes ##

Une page peut avoir plusieurs colonnes et blocs et peut s'étendre d'une colonne à l'autre par défaut. Plusieurs pages peuvent avoir des largeurs et des nombres de colonnes différents. Toutes les caractéristiques FO suivent les limites d'une page multi-colonnes.

### Listes ###

Une liste XSL-FO est établie par deux ensembles de blocs disposés côte à côte. Conceptuellement, dans une liste, un bloc à gauche indique un nombre, une puce ou une chaîne de texte, tandis que le bloc de droite peut fonctionner comme prévu. La numérotation des listes XSL-FO est généralement effectuée par le XSLT.

### Les tables ###

Un tableau FO est similaire à un tableau HTML/CSS. L'utilisateur peut sélectionner les lignes de données, les informations de style, la couleur d'arrière-plan pour chaque cellule individuelle. À l'aide d'informations de style distinctes, l'utilisateur a le privilège de sélectionner la première ligne comme ligne d'en-tête de tableau. Le processeur FO peut être informé explicitement de la spécification d'espace de chaque colonne, ou pour ajuster automatiquement le texte dans le tableau.

### Indexation ###

XSL-FO 1.1 a des fonctionnalités qui aident à générer un index en référençant des éléments correctement balisés.

### Avantages ###

* Convient pour la publication basée sur le contenu
* Facilité d'utilisation
* Faible coût

## Références ##

* [Qu'est-ce que XSL-FO ?] (https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [Objets de formatage XSL](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

