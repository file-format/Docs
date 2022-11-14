{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "fondamentaux" ],
  "description":"Portable Document Format (PDF) est une représentation standard de documents indépendante du logiciel, du matériel et du système d'exploitation. Les normes PDF incluent PDF/A, PDF/E, PDF/UA, PDF/VT et PDF/X.",
  "title" :"Format de fichier PDF - Qu'est-ce qu'un fichier PDF ?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) est un type de document créé par Adobe dans les années 1990. Le but de ce format de fichier était d'introduire une norme pour la représentation des documents et autres documents de référence dans un format indépendant du logiciel d'application, du matériel ainsi que du système d'exploitation. Le format de fichier PDF a la pleine capacité de contenir des informations telles que du texte, des images, des hyperliens, des champs de formulaire, des médias enrichis, des signatures numériques, des pièces jointes, des métadonnées, des fonctionnalités géospatiales et des objets 3D qui peuvent faire partie du document source.

Dans la plupart des cas, les documents existants sont convertis en PDF plutôt que de créer un nouveau PDF à partir de rien. Mais cela ne signifie pas qu'il n'y a pas de logiciel pour créer ou manipuler des fichiers PDF.

**(Vous devez partager quelque chose sur le format de fichier PDF ? Vous pouvez publier vos découvertes dans la section [PDF File Format News](https://news.fileformat.com/t/PDF).)**

## Format de fichier PDF - Bref historique

Voici un aperçu rapide de la chronologie de la formation du fichier PDF en termes de chronologie :

**1993** - Adobe Systems a rendu les spécifications PDF disponibles gratuitement

**2008** - PDF a été publié en tant que norme ouverte le 1er juillet 2008 et a été publié par l'Organisation internationale de normalisation en tant que **ISO 32000-1:2008**.

**2008** - Adobe a publié une licence de brevet public au format ISO 32000-1 pour tous les brevets détenus par Adobe nécessaires à la fabrication, l'utilisation, la vente et la distribution d'implémentations conformes au format PDF.

La première version de PDF désignée comme PDF 1.0 qui a ensuite subi des révisions jusqu'à PDF 1.7. PDF 1.7, qui est devenu la norme ISO 32000-1, inclut certaines technologies propriétaires non normalisées ainsi que l'architecture Adobe XML Forms (XFA) et l'extension JavaScript pour Acrobat. C'était le 28 juillet 2017 lorsque le PDF 2.0, connu sous le nom d'ISO 32000-2:2017, a été publié et n'inclut aucune technologie non normalisée.

## Spécifications du format de fichier PDF

Un fichier PDF est un ensemble d'octets qui peuvent être regroupés en jetons selon des règles de syntaxe définies par les spécifications PDF. Une ou plusieurs jetons sont combinés pour former des entités syntaxiques de niveau supérieur, principalement des objets, qui sont les valeurs de données de base à partir desquelles un document PDF est construit.

### Structure des fichiers des fichiers PDF

Le contenu du fichier PDF est organisé dans l'ordre suivant à l'intérieur du fichier.

|En-tête
|Corps
|Table de concordance
|Bande-annonce

#### En-tête du fichier PDF ####

Quelle que soit la version PDF, un fichier PDF commence par un en-tête contenant un identifiant unique pour le PDF et la version du format tel que %PDF-1.x où x varie de 1 à 7.

#### Corps du fichier ####

Le corps d'un fichier PDF consiste en une séquence d'objets indirects représentant le contenu d'un document. Les objets, comme décrit ci-dessus, représentent des composants du document tels que des polices, des pages et des images échantillonnées. À partir de PDF 1.5, le corps peut également contenir des flux d'objets, chacun contenant une séquence d'objets indirects.

#### Tableau de correspondance ####

La table de références croisées contient des informations qui permettent un accès aléatoire à des objets indirects dans le fichier afin que le fichier entier n'ait pas besoin d'être lu pour localiser un objet particulier. Le tableau doit contenir une entrée d'une ligne pour chaque objet indirect, spécifiant le décalage d'octet de cet objet dans le corps du fichier. (À partir de PDF 1.5, certaines ou toutes les informations de référence croisée peuvent également être contenues dans des flux de référence croisée.

#### Bande annonce du fichier ####

La bande-annonce d'un fichier PDF permet à un lecteur averti de retrouver rapidement la table de correspondance et certains objets particuliers. Les lecteurs conformes doivent lire un fichier PDF à partir de sa fin. La dernière ligne du fichier ne doit contenir que le marqueur de fin de fichier, %%EOF. Les deux lignes précédentes doivent contenir, une par ligne et dans l'ordre, le mot clé startxref et le décalage d'octet dans le flux décodé du début du fichier au début du mot clé xref dans la dernière section de renvoi.

### Objets PDF ###

Un fichier PDF comprend plusieurs types d'objets différents qui sont des types suivants

* Valeurs booléennes - représentant conditionnel vrai ou faux
* Nombres - Valeurs entières et réelles
* Chaînes - contient des caractères entre parenthèses
* Noms - commencent par un caractère avant /, par exemple /ASomewhatLongerName donne ASomewhatLongerName
* Tableaux - PDF prend en charge les tableaux unidimensionnels. Des tableaux de dimensions supérieures peuvent être construits en utilisant des tableaux comme éléments imbriqués
* Dictionnaires - collection d'objets sous forme de paires clé-valeur. Il peut avoir zéro entrée.
* Streams - représente une séquence d'octets qui peut également être de longueur illimitée
* Objet nul - représente une valeur nulle

Il peut y avoir d'autres objets comme des commentaires qui sont introduits avec le signe % et peuvent contenir des caractères 8 bits.

### Objets indirects ###

Tout objet dans un fichier PDF peut être étiqueté comme un objet indirect. Les objets indirects reçoivent un identifiant d'objet unique par lequel d'autres objets peuvent s'y référer. Les références croisées à ceux-ci sont conservées dans une table d'index et marquées avec le mot-clé xref qui suit le corps principal et donne le décalage d'octet de chaque objet indirect depuis le début du fichier.

### Mises en page PDF linéaires et non linéaires ###

Les mises en page PDF sont classées comme linéaires et non linéaires en fonction des applications cibles et d'autres facteurs.

Non linéaire - Les fichiers PDF non linéaires utilisent moins d'espace disque que les fichiers PDF linéaires. Les pages PDF du document résident sous forme dispersée dans le fichier PDF et c'est pourquoi les fichiers non linéaires sont plus lents que les fichiers linéaires.

PDF linéaire - Ciblant les lecteurs PDF en ligne, les fichiers PDF linéaires sont construits de telle manière qu'ils sont écrits sur le disque de manière linéaire. Cela ne nécessite pas de plugins de navigateur pour que le document entier soit chargé avant l'affichage.

### Présentation des objets ###

Comme mentionné, le corps du PDF est une collection d'objets mentionnés ci-dessus. PDF est largement basé sur PostScript sans les fonctionnalités de contrôle des langages de programmation comme les commandes if et loop. Les commandes émises par le code Postscript pour générer des contenus graphiques sont collectées et tokenisées en plus de tous les fichiers, graphiques ou polices référencés par le document. Tous ces contenus sont accumulés dans un seul fichier, ce qui donne une sortie PostScript composée.

#### Texte ####

Le texte en PDF est représenté par des éléments de texte qui sont en fait affichés avec des glyphes de polices. Un glyphe est une forme graphique et est sujet à toutes les manipulations graphiques, telles que la transformation des coordonnées. En raison de l'importance du texte dans la plupart des descriptions de page, PDF fournit des fonctionnalités de niveau supérieur pour décrire, sélectionner et afficher les glyphes de manière pratique et efficace.

#### Graphiques ####

Les opérateurs graphiques utilisés dans les flux de contenu PDF décrivent l'apparence des pages qui doivent être reproduites sur un périphérique de sortie raster. Les installations sont destinées à la fois aux applications d'impression et d'affichage. Les opérateurs graphiques forment six groupes principaux :

* Les opérateurs d'état graphique manipulent la structure de données appelée l'état graphique, le cadre global dans lequel les autres opérateurs graphiques s'exécutent. L'état graphique comprend la matrice de transformation actuelle (CTM), qui mappe les coordonnées de l'espace utilisateur utilisées dans un flux de contenu PDF en coordonnées du périphérique de sortie. Il inclut également la couleur actuelle, le chemin de détourage actuel et de nombreux autres paramètres qui sont des opérandes implicites des opérateurs de peinture.
* Les opérateurs de construction de chemin spécifient des chemins, qui définissent des formes, des trajectoires de ligne et des régions de différentes sortes. Ils incluent des opérateurs pour commencer un nouveau chemin, y ajouter des segments de ligne et des courbes et le fermer.
* Les opérateurs de peinture de chemin remplissent un chemin avec une couleur, peignent un trait le long de celui-ci ou l'utilisent comme limite de délimitation.
* D'autres opérateurs de peinture peignent certains objets graphiques auto-descriptifs. Ceux-ci incluent des images échantillonnées, des ombrages géométriquement définis et des flux de contenu entiers qui contiennent à leur tour des séquences d'opérateurs graphiques.
* Les opérateurs de texte sélectionnent et affichent les glyphes de caractères à partir des polices (descriptions des polices de caractères pour représenter les caractères de texte). Étant donné que PDF traite les glyphes comme des formes graphiques générales, de nombreux opérateurs de texte peuvent être regroupés avec les opérateurs d'état graphique ou de peinture. Cependant, les structures de données et les mécanismes de traitement des descriptions de glyphes et de polices sont suffisamment spécialisés.
* Les opérateurs de contenu marqué associent des informations logiques de niveau supérieur à des objets dans le flux de contenu. Ces informations n'affectent pas l'apparence rendue du contenu ; il est utile pour les applications qui utilisent PDF pour l'échange de documents.

## Références ##

* [Format de fichier PDF : structure de base] (https://resources.infosecinstitute.com/pdf-file-format-basic-structure/)
* [PDF - Wikipédia](https://en.wikipedia.org/wiki/PDF)
* [Référence PDF - Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

