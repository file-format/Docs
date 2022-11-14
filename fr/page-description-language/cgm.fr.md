{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Computer Graphics Metafile", "File", "Extension", "File Format", "Vector Graphics", "Metafile Descriptor"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier CGM",
  "description":"En savoir plus sur le format de fichier CGM et les API qui peuvent créer et ouvrir des fichiers CGM.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Qu'est-ce qu'un fichier CGM ? ##

Computer Graphics Metafile (CGM) est un format de métafichier standard international gratuit et indépendant de la plate-forme pour le stockage et l'échange de graphiques vectoriels (2D), de graphiques raster et de texte. CGM utilise une approche orientée objet et de nombreuses fonctionnalités pour la production d'images. CGM utilise ces caractéristiques orientées objet pour remodeler des éléments graphiques afin de restituer une image. Un métafichier contient les informations nécessaires qui définissent d'autres fichiers. Dans CGM, un fichier source textuel contient tous les éléments graphiques qui peuvent ensuite être compilés dans un fichier binaire. Fondamentalement, CGM est un moyen de faciliter l'échange de données graphiques 2D, indépendamment de toute plate-forme ou appareil particulier.

Le format CGM fournit différents éléments pour exécuter des fonctions et signifier des objets pour ajuster les primitives géométriques et les informations graphiques. Bien que CGM ait été remplacé par d'autres formats pour afficher les arts graphiques sur les pages Web car il n'est pas bien pris en charge par les pages Web, il reste très populaire parmi les applications industrielles, aéronautiques et autres applications techniques. Bien que le World Wide Web Consortium ait développé WebCGM, une approche alternative pour l'utilisation de CGM sur le Web. L'implémentation principale de CGM était une illustration de la séquence d'opérations de base du Graphical Kernel System (GKS). Il n'a pas été beaucoup adopté dans les conceptions professionnelles mais a été largement supplanté par d'autres formats tels que DXF et SVG.

## Histoire ##

CGM s'est avéré être une norme internationale en 1987 (ISO 8632-1987) et a également été adopté comme norme nationale au Royaume-Uni par BSI et aux États-Unis par ANSI. Après un certain nombre d'amendements en 1991, une norme révisée de CGM a été publiée en 1992 (ISO 8632: 1992). En 2001, le World Wide Web Consortium a développé WebCGM avec une capacité améliorée à utiliser avec les pages Web. En 2007, la deuxième version de WebCGM est sortie et la troisième version est sortie en 2010 avec des fonctionnalités améliorées.

## Format de fichier CGM ##

Les métafichiers d'infographie sont essentiellement une base de données d'informations graphiques et fournissent les moyens de capturer, de stocker et de transmettre des données graphiques. Par conséquent, il doit y avoir un composant système graphique pour créer la base de données simultanément avec l'exécution d'une application dans un format de métafichier. Dans la plupart des cas, ce composant est le générateur de métafichiers. Parallèlement, il existe un besoin pour un autre composant capable de récupérer, d'interpréter et de restituer des données graphiques dans un métafichier. Ce besoin est satisfait par la présence d'un interpréteur de métafichiers. La figure suivante représente l'environnement de travail du métafichier graphique.

La relation de CGM avec d'autres composants d'un système graphique typique est illustrée dans la figure ci-dessus. Il ressort également de la figure que la fonctionnalité du métafichier ne dépend pas de la sortie finale du périphérique.

Généralement, il existe deux catégories de métafichiers : **capture de section** et **capture d'image**. La principale fonctionnalité du métafichier de capture d'image est la capture de plusieurs définitions d'images indépendantes du périphérique. Alors que les métafichiers de capture de session utilisent l'interface système pour capturer le dialogue de sortie dans un système graphique. CGM appartient à la catégorie des métafichiers de capture d'images statiques. CGM fournit un arrangement bien organisé de composants avec une structure à deux niveaux.

1. Descripteur de métafichier
1. Un pool d'images logiquement indépendantes

Chaque image est une collection de descripteurs d'image et un corps d'image comprenant une définition d'image. Le descripteur de métafichier définit les informations descriptives qui s'appliquent également à toutes les images de ce métafichier. Ces informations aident l'interpréteur à analyser correctement un métafichier et à reconnaître les ressources nécessaires au rendu correct d'une image. Bien que le descripteur d'image contienne également les informations descriptives, il ne peut reconnaître que l'image dans laquelle réside le descripteur. Dans ce format de fichier, chaque définition d'image est autonome et logiquement souveraine. Ils sont indépendants de toutes les autres définitions d'image dans un fichier. Juste après l'interprétation du méta-descripteur, les images peuvent être consultées et interprétées de manière aléatoire. Le changement d'état des images précédentes n'a aucun effet sur leurs successeurs. Cette indépendance d'image est une autre caractéristique importante de CGM.CGM consiste en un espace de coordonnées qui sont des coordonnées cartésiennes 2D appelées coordonnées de périphérique virtuel et peuvent être représentées par un nombre ou une précision représentant la plage et la granularité. CGM spécifie à la fois la sélection directe des couleurs et la sélection basée sur l'indice. Dans le premier cas, le spécificateur de couleur consiste en un triplet RVB tandis que plus tard, le spécificateur de couleur indique un index dans une table de couleurs.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
