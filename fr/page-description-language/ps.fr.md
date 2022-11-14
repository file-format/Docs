{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier PS",
  "description":"En savoir plus sur le format de fichier PS et les API qui peuvent créer et ouvrir des fichiers PS.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier .PS ? ##

PostScript (PS) est un langage de description de page à usage général utilisé dans le secteur de la publication assistée par ordinateur et électronique. L'objectif principal de PostScript (PS) est de faciliter la conception graphique en deux dimensions. La plupart des langages nécessitent une étape de compilation distincte avant l'exécution du code, tandis que le format Post Script (PS) prend en charge une interprétation simple à l'exécution. Sa première version définit les formes graphiques, les différentes apparences de texte et les images modélisées sur les pages imprimées ou les pages affichées, en suivant les règles du modèle d'imagerie Adobe. Un programme de PS est capable d'intercommuniquer une description de document entre un système de composition et d'impression en gardant le dispositif indépendant et de haut niveau. De plus, ce programme est également capable de gérer l'apparence du texte et des graphiques sur un écran.

La description de la page PostScript est disponible pour être rendue, affichée sur l'imprimante et sur un autre périphérique de sortie à l'aide de l'interpréteur PostScript du périphérique. Lorsque les commandes d'impression de caractères, de formes graphiques et d'images sont exécutées par l'interpréteur, pour ce périphérique spécifique, la description PostScript de haut niveau est convertie au format de données raster de bas niveau. Généralement, différentes applications telles que les illustrateurs, les systèmes de composition de documents et la conception assistée par ordinateur (CAO) sont automatisées pour générer des descriptions de page PostScript. Généralement, les programmeurs doivent écrire des programmes PostScript au moment de la création de nouvelles applications. Cependant, un programmeur peut tirer parti des capacités du langage PostScript qui ne sont accessibles dans aucune application en écrivant un programme PS pour cette situation particulière.

## Bref historique ##

Le concept de langage PostScript a été introduit pour la première fois par John Warnock. En 1966, il travaillait sur un projet du port de New York. Il essayait de développer un interpréteur pour un grand graphique en trois dimensions pour la base de données de ce projet. Pour traiter ces graphiques, John Warnock a conçu le langage Design System. Pendant ce temps, Xerox PARC cherchait un moyen standard de définir des images de page pour sa première imprimante laser. Bien que Bob Sproull et William Newman aient développé en 1975-76 le format Press (format de données) pour piloter les imprimantes laser, un langage était nécessaire pour plus de flexibilité. En 1978, Warnock a rejoint Martin Newell au Xerox PARC et a réécrit le langage d'interprétation, JaM, qui a ensuite été développé et étendu au langage Interpress. Warnock a fondé Adobe Systems en décembre 1982 avec Chuck Geschke, Doug Brotz, Ed Taft et Bill Paxton. Ils ont commencé à travailler sur un langage plus simple appelé PostScript similaire à Interpress, qui a été commercialisé en 1984. Steve Jobs d'Apple leur a rendu visite et leur a conseillé d'adapter PostScript pour piloter des imprimantes laser.

En mars 1985, la première imprimante dotée d'un interpréteur PostScript intégré était la LaserWriter d'Apple, qui a révolutionné la publication assistée par ordinateur (DTP). La solidité technique et la disponibilité généralisée ont fait de PostScript un langage de choix pour la publication assistée par ordinateur et électronique. En 1990, un interpréteur pour le langage PostScript était une partie essentielle des imprimantes laser.

## Caractéristiques principales ##

Les capacités du langage PostScript à gérer les graphiques interactifs et la description de page possèdent les caractéristiques suivantes :

**Formes :** De nature arbitraire, elles peuvent comprendre des lignes droites, des courbes, des carrés et des courbes cubiques qui peuvent être à la fois auto-traversantes et déconnectées (dans les sections et les trous).

**Opérateurs de peinture :** permettent le contour de la forme de n'importe quelle épaisseur, couleur, remplissage ou permettent à la forme d'être dessinée comme un découpage pour permettre le recadrage de tout autre graphique.

**Couleurs :** ont la diversité comme les niveaux de gris, RVB, CMJN et CIE. Des types spéciaux de couleurs sont modélisés comme des caractéristiques différentes : couleurs d'accompagnement, mappage des couleurs, même ombrage et motifs répétitifs.

**Texte :** entièrement intégré aux graphiques. De plus, le modèle d'imagerie Adobe permet d'afficher des caractères de texte sous forme de formes graphiques pouvant être exploitées par n'importe quel opérateur graphique normal.

**Images échantillonnées** : extraites de sources originales (photographies numérisées) ou pouvant être produites de manière synthétique. Le langage PostScript offre divers moyens de régénérer des images à n'importe quelle résolution et selon différents modèles de couleurs sur un périphérique de sortie.

Un langage de programmation à usage général peut tirer parti des capacités graphiques du langage PostScript en intégrant Ps dans son cadre. Les types de données primitifs, tels que les nombres, les caractères, les tableaux et les chaînes ; les primitives de contrôle, telles que les boucles, les procédures et les conditions ; et certaines fonctionnalités non conventionnelles, telles que les dictionnaires, sont spécifiées dans la langue. Ces fonctionnalités permettent aux programmeurs d'écrire des commandes pour invoquer des opérations de niveau supérieur. Ces opérations de haut niveau répondent aux besoins d'applications complexes. Une telle pratique est plus compacte et efficace plutôt que d'utiliser un ensemble fixe d'opérations de base.

Les programmes écrits en PostScript peuvent être produits, communiqués et interprétés sous la forme d'un texte source ASCII. L'ensemble du langage peut être défini sous la forme de caractères imprimables et d'espaces blancs. Cette représentation aide les programmeurs à créer, manipuler et comprendre facilement le langage. De plus, le stockage et la transmission de fichiers entre divers ordinateurs et systèmes d'exploitation restent pratiques grâce à l'indépendance de la machine.

Les formes codées binaires du langage sont possibles, lorsque le programme est garanti à un chemin de communication entièrement transparent vers l'interpréteur PostScript. Une cohérence stricte avec la représentation ASCII des programmes PS est conseillée par Adobe pour l'échange de documents ou le stockage d'archives.

## Versions ##

PS(.ps) est l'extension de fichier d'un document PostScript. Les Archives nationales du Royaume-Uni classent cinq versions chronologiques du fichier PostScript, définies dans la version DSC : versions 1.0, 2.0, 2.1, 3.0, 3.1. Chaque version définit des commentaires structurants importants. Le fichier PostScript encapsulé (EPS) est un sous-type spécial de fichier PostScript qui utilise le langage pour spécifier un graphique rectangulaire. Le manuel de référence du langage PostScript décrit un EPS comme suit : "Un fichier PostScript encapsulé (EPS) est un programme PostScript décrivant au plus une seule page dans un formulaire qui peut être importé par d'autres applications pour être intégré dans un document contenant." Un fichier de document PostScript peut contenir un fichier EPS. Une utilisation supplémentaire de PostScript est mentionnée sous le nom de Display PostScript (DPS). DPS génère des graphiques à l'écran via un moteur graphique qui utilise le modèle et le langage d'imagerie PostScript.

## Références ##

* [Famille de formats PostScript](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

