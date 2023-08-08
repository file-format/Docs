{
  "date" : "2019-10-11",
  "keywords" :[ "fichier djvu", "format de fichier djvu", "qu'est-ce qu'un fichier djvu", "fichier", "exemple djvu", "extension de fichier djvu","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier DJVU",
  "description":"En savoir plus sur le format de fichier DJVU et les API qui peuvent créer et ouvrir des fichiers DJVU.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier DJVU ?

DjVu, prononcé comme "déjà vu", est un format de fichier graphique destiné aux documents numérisés et aux livres, en particulier ceux qui contiennent la combinaison de texte, dessins, images et photographies. Il a été développé par AT&T Labs. Il utilise plusieurs techniques telles que la séparation des couches d'image du texte et des images d'arrière-plan, le chargement progressif, le codage arithmétique et la compression avec perte pour les images bitonales. Étant donné que le fichier DJVU peut contenir des images, des photographies, du texte et des dessins en couleur compressés mais de haute qualité et peut donc être enregistré dans moins d'espace, il est utilisé sur le Web sous forme de livres électroniques, de manuels, de journaux, de documents anciens, etc.

DjVu peut être considéré comme une alternative supérieure à [PDF](/fr/pdf/). Les extensions de fichiers associées à DjVu sont .DJVU ou .DJV. DjVu peut atteindre des taux de compression environ 5 à 10 meilleurs que les méthodes existantes telles que [JPEG](/fr/image/jpeg/) & [GIF](/fr/image/gif/) pour les documents couleur et 3 à 8 fois mieux que [TIFF]( /image/tiff/) dans les documents en noir et blanc. Les documents numérisés à 300 DPI avec des couleurs jusqu'à 25 Mo peuvent être compressés jusqu'à 30 à 100 Ko. De même, les documents en noir et blanc peuvent être compressés jusqu'à 5 à 30 Ko. La page HTML moyenne peut atteindre 50 Ko, par conséquent, ces documents peuvent être téléchargés sur le net sans aucun problème.

## Bref historique ##

La technologie DjVu a été développée dans les laboratoires AT&T par [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner et Paul G de 1996 à 2001. Le format de fichier DjVu a subi diverses révisions, la plus récente datant de 2005.


|Version|Date de sortie|Remarques
---|---|---|
|1–19|1996–1999|Ce sont les versions de développement.
|20|Avril 1999|La page unique est passée au format multipage.
|23|Juillet 2002|Bloc CID
|24|Février 2003|LTAnno chunk
|21|Septembre 1999|Format de stockage indirect remplacé. La couche de recherche de texte a été ajoutée.
|22|Avril 2001|Orientation de la page, couleur JB2
|25|Mai 2003|Bloc NAVM. La prise en charge des signets DjVu a été ajoutée.
|26|Avril 2005|Annotations texte/ligne

## Format de fichier DjVu ##

Les documents DjVu sont des fichiers IFF85. La structure fournit une hiérarchie de conteneurs contenant des informations dans un fichier DjVu. Ces conteneurs sont également appelés "Chunks". Le type de bloc et l'ID de bloc décrivent comment le bloc est utilisé. Il y a un en-tête de 4 octets suivi d'une structure IFF. Les quatre premiers octets d'un fichier DjVu sont 0x41 0x54 0x26 0x54. Cette section traite des différents types de documents DjVu et des morceaux correspondants qui les composent.


|ID de bloc|Utilisation
---|---|
|FORM|Le bloc composite ayant les quatre premiers octets de données du bloc FORM qui sont l'identifiant secondaire.
|FORM:DJVM|Un document DjVu multipage. Bloc composite contenant le bloc DIRM.
|FORM:DJVU|Document DjVu d'une seule page. Morceau composite qui contient les morceaux qui composent une page dans un document djvu.
|FORM:DJVI|Un fichier DjVu "partagé" qui est inclus via le bloc INCL. Annotations partagées et dictionnaire de formes.
|FORM:THUM|Bloc composite contenant les blocs TH44 qui sont les vignettes intégrées.
|DIRM|Informations sur le nom de la page pour les documents multipages.
|NAVM|Informations sur les signets
|ANTa, ANTz|Annotations comprenant à la fois les paramètres d'affichage initiaux et les hyperliens superposés, les zones de texte, etc.
|TXTa, TXTz|Unicode Informations sur le texte et la mise en page.
|Djbz|Table de forme partagée.
|Sjbz|BZZ a compressé les données bitonales JB2 utilisées pour stocker le masque.
|FG44|Données IW44 utilisées pour stocker le premier plan
|BG44|Données IW44 utilisées pour stocker l'arrière-plan
|TH44|Données IW44 utilisées pour stocker les images miniatures intégrées
|WMRM|Données JB2 requises pour supprimer un filigrane
|FGbz|Données JB2 de couleur. Fournit une couleur pour chacun (blit ou shape ?) dans le bloc Sjbz correspondant.
|INFO|Informations sur une page DjVu
|INCL|L'ID d'un bloc FORM:DJVI inclus.
|BGjp|Arrière-plan encodé en JPEG
|FGjp|Premier plan encodé en JPEG
|Smmr|Masque encodé G4

### Compression DJVU

Une image unique est divisée en plusieurs images différentes, puis chaque image est compressée séparément. Pour la création d'un fichier DjVu l'image est d'abord séparée en trois images, une image de fond, de premier plan et une image de masque. Généralement, les images d'arrière-plan et de premier plan sont des images couleur de résolution inférieure; mais l'image de masque est une image de plus haute résolution et généralement le texte y est stocké. Après la séparation, les images de premier plan et d'arrière-plan sont compressées via un algorithme de compression basé sur les ondelettes IW44, tandis que l'image de masque est compressée à l'aide d'une autre méthode appelée JB2.

La méthode de codage JB2 élimine une grande partie de la redondance dans l'image du texte en identifiant des formes identiques sur la page, telles que des occurrences multiples d'un caractère dans une police particulière. JB2 code d'abord le bitmap de chaque forme unique en tirant parti de la redondance entre les formes similaires. Il code ensuite les emplacements auxquels chaque forme apparaît sur la page. JB2 et IW44 reposent tous deux sur un nouveau type de codeur arithmétique binaire adaptatif appelé le codeur ZP qui élimine toute redondance restante à quelques pour cent de la limite de Shannon. Le codeur ZP est adaptatif et plus rapide que les autres codeurs arithmétiques binaires approximatifs.

## Références ##

* [DjVu - Wikipédia](https://en.wikipedia.org/wiki/DjVu)
* [Format de fichier DjVu](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

