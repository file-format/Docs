{
  "date" : "2020-03-16",
  "keywords" :[ "Fichier IGES", "Format de fichier", "CAO" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier IGES et les API qui peuvent créer et ouvrir des fichiers IGES.",
  "title" :"Format de fichier IGES",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Qu'est-ce qu'un fichier IGES ?

Un fichier avec l'extension .iges est utilisé pour échanger des informations de conception entre les applications de conception assistée par ordinateur (CAO). IGES signifie Initial Graphics Exchange Specifications. Les informations échangées à l'aide d'IGES comprennent des représentations de schémas de circuits, de structures filaires, de surfaces de forme libre ou de modèles solides. IGES trouve ses applications dans les dessins d'ingénierie traditionnels, l'analyse de modèles et les fonctions de fabrication. Le format peut échanger des informations de conception 2D ou 3D entre les programmes de CAO. Les fichiers IGES peuvent être ouverts avec plusieurs applications de CAO telles qu'Autodesk et CADSoftTools ABViewer. Il existe également plusieurs API disponibles pour ouvrir et convertir les fichiers IGES par programmation.

## Format de fichier IGES

Les fichiers IGES sont au format texte ASCII et peuvent être ouverts dans n'importe quel éditeur de texte pour afficher le contenu du fichier. Les informations textuelles d'un fichier IGES sont représentées au format "Hollerith". Un fichier IGES commun peut contenir des milliers de lignes pour représenter les informations 2D ou 3D qui peuvent être échangées selon ce format. Un fichier IGES est divisé en cinq sections, désignées par la lettre majuscule spécifique dans la 73e colonne. Ces sections sont les sections `Start` (S), `Global` (G), `Data Entry` (D), `Parameter Data` (P) et `Terminate` (T). Les sections de saisie de données et de données de paramètres sont généralement abrégées DE et PD, respectivement.

### En-tête de fichier IGES

Les sections Start et Global contiennent des informations de base sur :
* Nom du fichier et sa source
* Délimiteurs pour la section Parameter Data
* Auteur du fichier et autres informations générales.

Les sections Start et Global de l'exemple de document sur Wikipedia sont les suivantes.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Comme on peut le voir, le champ de début contient des descriptions lisibles par l'homme du fichier, et j'ai tous les caractères dans les colonnes 1-72, avec la ligne se terminant par l'en-tête de section et le numéro de ligne de section. Il doit y avoir au moins 1 ligne de la section Début. La section globale contient des données de préprocesseur. Il doit également être présent dans le fichier et se terminer par le format G000000#.

### Section de saisie de données (DE) et de données de paramètres (PD)

#### Section de saisie de données
Un fichier IGES se compose de plusieurs entités qui contiennent les informations sur les données de base du format de fichier IGES. Une entité contient des informations sur différents éléments d'un format de données IGES et est utilisée pour le dessin. Les entités les plus couramment utilisées incluent :
* Arc circulaire
* Courbe composée
* Arc conique
* Avion
* Ligne

Ce ne sont que quelques-uns et il y a environ 150 entités différentes dans IGES. Chaque entité est identifiée par un numéro de type tel que :
* ARC CIRCULAIRE (Type 100)
* LIGNE (Type 110)

##### Propriétés de l'entité

Chaque entité déclarée possède les propriétés suivantes.

|Nom du champ|Description|
---|---|
|Type d'entité |Il s'agit du type d'entité décrite. Par exemple, 116 décrit une entité Point.|
|Pointeur PD |Ceci donne l'emplacement des données de cette entité dans la section Parameter Data. Cet emplacement est simplement le numéro de ligne à l'intérieur de la section PD qui contient la première ligne de ces données d'entité.|
|Structure |Zéro ou pointeur vers l'entité de définition. Non applicable pour la plupart des entités |
|Modèle de police de ligne| Numéro ou pointeur vers l'entité de modèle de police de ligne. Le nombre signifie : * 0 Aucun motif spécifié (par défaut) * 1 Solide * 2 Tireté * 3 Fantôme * 4 Ligne centrale * 5 Pointillé |
|Niveau| Spécifie les niveaux à associer à cette entité. Permet à l'entité d'apparaître sur plusieurs niveaux |
|Voir| Spécifie les options d'affichage. Ce sont : 0 Indique une visibilité et des caractéristiques identiques dans toutes les vues. Pointeur par défaut vers l'entité Vue (Type 410) à partir de laquelle elle peut être visualisée Référencer une entité Vue Associativité visible (Type 402, Formulaire 3)
|Pointeur de matrice de transformation| Fait référence à une entité de matrice de transformation (Type 124) ou vaut zéro par défaut (pas de transformation) |
|Associativité d'affichage des étiquettes| Fait référence à une associativité d'affichage d'étiquette (type 402, formulaire 5) qui définit la façon dont l'étiquette d'entité apparaît.|
|Numéro de statut| Contient quatre sections de deux nombres. 1-2 : Statut vide. Soit 00 pour normal ou 01 pour masqué. 3-4 : Commutateur d'entité subordonnée : 00 pour indépendant, 01 pour physiquement dépendant, 02 pour logiquement dépendant et 03 pour les deux. 5-6 : Indicateur d'utilisation d'entité : est soit 00 pour la géométrie, 01 pour l'annotation, 02 pour la définition, 03 pour autre, 04 pour logique, 05 pour paramétrique 2D et 06 pour la géométrie de construction. Enfin, 7-8 est la hiérarchie, où 00 indique le haut vers le bas global (utilisez les caractéristiques de cette entité), 01 est le report global (n'utilisez pas les caractéristiques de cette entité) et 02 est l'utilisation de la propriété de hiérarchie (utilisez Hierarchy Entity (Type 406, Form 10)pour déterminer les caractéristiques du groupement hiérarchique).|
|Numéro de séquence| Spécifié par D#, où # est le numéro de ligne pour cette section (pas à partir du haut du fichier). Ceci est également utilisé pour pointer vers cette entité de saisie de données.|
|Type d'entité| il est spécifié deux fois par liste d'entités |
|Numéro d'épaisseur de ligne| Spécifie l'épaisseur lors de l'affichage de l'entité. Le plus petit est 1, 0 est la valeur par défaut |
|Numéro de couleur| Spécifie la couleur de l'entité. Les valeurs entières autorisées sont : 0 Aucune couleur (par défaut) 1 Noir 2 Rouge 3 Vert 4 Bleu 5 Jaune 6 Magenta 7 Cyan 8 Blanc |
|Numéro de comptage de ligne de paramètre| Spécifie le nombre de lignes occupées par cette entité dans la section des données de paramètres |
|Numéro du formulaire| Indique la forme, ou la représentation de cette entité. Modifie la façon dont les données de paramètre sont interprétées. La valeur par défaut est 0 |
|Champ réservé| Non utilisé |
|Champ réservé| Non utilisé |
|Libellé d'entité| Identifiant spécifié par l'application - justifié à droite |
|Numéro d'indice| Qualificatif numérique pour l'étiquette d'entité. Les deux forment ensemble un identifiant unique pour l'entité |
|Numéro de séquence Voir ci-dessus. |Ce sera D#+1, car chaque entité est spécifiée sur deux lignes.|

#### Section des données des paramètres
La section Entrées de données est suivie de la section Données de paramètre. Il répertorie les données pour chaque entrée respective et répertorie les paramètres de l'entité en fonction des délimiteurs spécifiés dans la section Global (généralement des virgules pour séparer les paramètres et un point-virgule pour terminer la liste).


## Références
* [IGES par WikiPedia](https://en.wikipedia.org/wiki/IGES)

