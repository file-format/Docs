{
  "date" : "2019-12-16",
  "keywords" :[ "XLS", "fichier", "extension", "format de fichier", "Excel", "Feuille de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Votre guide de format de fichier pour savoir ce qu'est un fichier XLS et les API qui peuvent les créer et les ouvrir.",
  "title" :"Qu'est-ce que le format de fichier XLS ? Apprenez des experts en format de fichier !",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## Qu'est-ce qu'un fichier XLS ?

Les fichiers avec l'extension XLS représentent le format de fichier binaire Excel. Ces fichiers peuvent être créés par Microsoft Excel ainsi que par d'autres tableurs similaires tels que OpenOffice Calc ou Apple Numbers. Le fichier enregistré par Excel est connu sous le nom de classeur où chaque classeur peut avoir une ou plusieurs feuilles de calcul. Les données sont stockées et affichées aux utilisateurs sous forme de tableau dans une feuille de calcul et peuvent couvrir des valeurs numériques, des données textuelles, des formules, des connexions de données externes, des images et des graphiques. Des applications telles que Microsoft Excel vous permettent d'exporter des données de classeur dans plusieurs formats différents, notamment [PDF](/fr/pdf/), [CSV](/fr/spreadsheet/csv/), [XLSX](/fr/spreadsheet/xlsx/), [TXT](/fr/ word-processing/txt/), [HTML](/fr/web/html/), [XPS](/fr/page-description-language/xps/), et plusieurs autres. Le format de fichier XLS a été remplacé par un format plus ouvert et structuré, XLSX, avec la sortie de Microsoft Excel 2007. Les dernières versions prennent toujours en charge la création et la lecture de fichiers XLS, bien que XLSX soit désormais le premier choix d'utilisation.

## Bref historique

XLS a été créé par Microsoft pour être utilisé avec Microsoft Excel et est également connu sous le nom de format de fichier d'échange binaire (BIFF). Ce type de fichier a été introduit pour la première fois en l'intégrant à Excel pour Windows en 1987. Les spécifications du format de fichier XLS ont été rendues publiques pour la première fois en juin 2008 en tant que révision 1. Après cela, les spécifications ont été continuellement mises à jour et la dernière révision disponible. date d'août 2018 et porte la mention révision 8.0. Voici un bref historique des différentes versions du format de fichier XLS :

* Version 7.0 (publiée avec office 95) : cette version d'Excel était la plus robuste et la plus rapide de toutes les versions et les réécritures de flux internes ont été mises à jour en 32 bits.
* Version 8 (publiée avec Office 97) : VBA a été introduit en tant que langage standard et les étiquettes de langage naturel supprimées ont été incorporées dans cette version pour la première fois. Il a également introduit un assistant de bureau trombone pour la première fois.
* Version 9 (publiée avec Office 2000) : Il n'y a eu que des modifications mineures dans la version 9 où l'assistant de bureau trombone pouvait simultanément contenir plusieurs objets qui n'étaient pas possibles auparavant.
* Version 10 (Sortie avec Office XP) : Cette version ne contient aucune amélioration notable.
* Version 11 (Sortie avec office 2003) : mise à jour majeure de la version 11, excel 2003 a été l'introduction de nouvelles tables.

## Spécifications du format de fichier XLS ##

Les données sont organisées dans un fichier XLS sous forme de flux binaires sous la forme d'un fichier composé comme décrit dans [MS-CFB]. Les données sont stockées dans le fichier composé à l'aide de stockages, de flux et de sous-flux qui contiennent des informations sur le contenu et la structure d'un classeur, y compris des données de classeur telles que des définitions de feuille de calcul. Chaque flux ou sous-flux contient une série d'enregistrements binaires. Chaque enregistrement binaire contient zéro ou plusieurs champs structurés contenant les données du classeur. Cette section donne un bref aperçu de la structure de fichier XLS, mais pour les spécifications détaillées du format de fichier, il faut consulter les [spécifications de formation de fichier XLS](https://msdn.microsoft.com/en-us/library/cc313154(v#office .12).aspx) document de Microsoft.

#### Flux et sous-flux ####

Un classeur est représenté par le flux de classeur. Chaque feuille de calcul d'un classeur est représentée par des sous-flux. En outre, il possède un sous-flux de feuille de graphique, un sous-flux de feuille de macro ou un sous-flux de feuille de dialogue qui suit le sous-flux global. Chaque flux ou sous-flux binaire contenant des données de classeur DOIT être écrit sous la forme d'une série d'enregistrements binaires.

#### Enregistrement ####

Les informations sur les fonctionnalités d'un classeur sont stockées sous la forme d'un enregistrement qui est une séquence d'octets de longueur variable. Un enregistrement binaire se compose des trois composants suivants :

**Type d'enregistrement :** Le type d'enregistrement est un entier non signé de deux octets qui spécifie le type d'informations spécifié par l'enregistrement et la façon dont la structure des données d'enregistrement spécifiques à cet enregistrement est ordonnée et structurée. Les valeurs de type d'enregistrement DOIVENT être une valeur de l'énumération d'enregistrement (section 2.3) ou l'enregistrement DOIT utiliser la future architecture d'enregistrement (section 2.1.6).

**Taille de l'enregistrement** : la taille de l'enregistrement est un entier non signé de deux octets qui spécifie le nombre d'octets qui spécifie la taille totale des données d'enregistrement. La taille de l'enregistrement DOIT être supérieure ou égale à 0 et DOIT être inférieure ou égale à 8224.

**Données d'enregistrement :** Le composant de données d'enregistrement contient des champs qui correspondent à un type d'enregistrement particulier et comprennent le reste de l'enregistrement. L'ordre et la structure des champs pour un type d'enregistrement donné sont spécifiés dans la section correspondante pour ce type d'enregistrement. La taille du composant de données d'enregistrement DOIT être égale à la taille de l'enregistrement. Les champs du composant de données d'enregistrement peuvent contenir des valeurs simples, des tableaux de valeurs, des structures de plusieurs champs, des tableaux de champs et des tableaux de structures.

#### Table de cellules ####

Les cellules sont les blocs fondamentaux d'un classeur qui stockent le contenu du classeur comme du texte, des formules et des données numériques. Les cellules conservent l'enregistrement des données stockées via une structure de données appelée table de cellules. La table de cellules elle-même est stockée dans la séquence d'enregistrements conformes aux règles CELLTABLE définies dans le document de spécifications. Il se compose d'une série de blocs de rangées où les rangées sont disposées en blocs de rangées. Chaque bloc de lignes contient des lignes allant de la première ligne contenant des données à la dernière ligne contenant des données.

La mise en forme des données ou des lignes est enregistrée dans un enregistrement de ligne pour chaque bloc de lignes. Chaque cellule contenant des données ou une mise en forme de cellule individuelle est représentée par un enregistrement. La mise en forme associée à une cellule peut être dérivée de la mise en forme de cellule individuelle, de la mise en forme des lignes, de la mise en forme des colonnes ou du format de cellule par défaut. L'ordre de priorité pour le formatage est le formatage des cellules individuelles avec la priorité la plus élevée, suivi du formatage des lignes, puis du formatage des colonnes, puis du format de cellule par défaut. Les cellules qui ne contiennent pas de données et qui ne contiennent pas de mise en forme individuelle ne sont pas enregistrées.

#### Formules ####

Une formule est une séquence de valeurs, de références de cellule, de noms, de fonctions ou d'opérateurs dans une cellule qui produisent ensemble une nouvelle valeur. Les formules sont stockées dans une représentation tokenisée appelée "expressions analysées". Une expression analysée est convertie en une formule textuelle au moment de l'exécution pour l'affichage et l'édition par l'utilisateur. Les formules de cellule sont spécifiées par l'enregistrement Formule. Les formules matricielles sont spécifiées par l'enregistrement Array. Les formules partagées sont spécifiées par l'enregistrement ShrFmla.

#### Graphiques ####

La feuille de graphique spécifie un graphique, un graphique qui affiche des données ou les relations entre des ensembles de données sous une forme visuelle, et un cache de données de graphique, une copie locale des données utilisées dans les données du graphique est manquante ou si des liens vers des les sources de données sont cassées. Le graphique spécifie un ou deux groupes d'axes, un ensemble d'axes par rapport auxquels les données du graphique sont tracées et l'ensemble de séries, de courbes de tendance et de barres d'erreur spécifiés dans le graphique. Chaque groupe d'axes spécifie un à quatre groupes de graphiques qui spécifient le type de visualisation utilisé pour afficher les données. Chaque série, courbe de tendance et barre d'erreur spécifie un groupe de graphiques auquel elle est associée.

#### Métadonnées ####

Les métadonnées sont des données supplémentaires associées à une cellule particulière ou à son contenu. Les métadonnées sont enregistrées dans BIFF8 uniquement à des fins d'extensibilité future.

#### Tableaux croisés dynamiques ####

Un tableau croisé dynamique est un mécanisme permettant de résumer les données sources pour obtenir une vue d'ensemble de la distribution de ces données. Dans un tableau croisé dynamique, les colonnes applicables des données source deviennent des champs qui peuvent être utilisés pour résumer les données. Lorsque les données source du tableau croisé dynamique sont des données source OLAP, les hiérarchies OLAP et certaines autres entités OLAP deviennent des champs dans le tableau croisé dynamique.
Un tableau croisé dynamique comporte deux parties principales, un PivotCache et une vue de tableau croisé dynamique. Il peut y avoir plusieurs vues de tableau croisé dynamique basées sur un seul PivotCache non OLAP.

#### Modes ####

Cette présentation décrit comment les informations de formatage et de protection des cellules d'une feuille (1) sont spécifiées. La mise en forme des cellules est composée de plusieurs ensembles de propriétés :

* Propriétés de la police (gras, italique, couleur de police, taille de police, etc…)
* Propriétés de remplissage (couleur de premier plan, couleur d'arrière-plan, motif, dégradé, etc…)
* Propriétés d'alignement (alignement à gauche, au centre, à droite, etc...)
* Propriétés de la bordure (gauche, droite, haut, bas, épais ou fin, couleur, etc…)
* Propriétés de formatage des nombres (date, heure, nombre de décimales, etc…)
* Propriétés de protection (verrouillé, caché, etc…)

Ces propriétés, dans leur ensemble, décrivent comment une cellule particulière est affichée et imprimée.

## Références ##

* [[MS-XLS] - Structure du format de fichier binaire Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] - Format de fichier binaire de fichier composé](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

