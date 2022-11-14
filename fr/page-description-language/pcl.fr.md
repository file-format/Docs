{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"En savoir plus sur le format de fichier PCL et les API qui peuvent créer et ouvrir des fichiers PCL.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier PCL ? ##

PCL signifie Printer Command Language qui est un langage de description de page introduit par Hewlett Packard (HP). HP a créé PCL pour fournir un moyen efficace de contrôler les fonctionnalités de l'imprimante sur de nombreux périphériques d'impression différents. Le format a été développé à l'origine pour les imprimantes matricielles et à jet d'encre de HP, mais a fait partie de diverses imprimantes thermiques, matricielles et par page au fil du temps. Le format a subi plusieurs révisions différentes, aboutissant à différentes versions où chaque version a été améliorée pour répondre aux exigences de temps en ce qui concerne les fonctionnalités de contrôle de l'imprimante. Aujourd'hui, PCL est le langage d'impression le plus répandu sur le marché des imprimantes laser.

## Versions PCL ##

Les versions PCL diffèrent par leurs fonctionnalités (par exemple, prise en charge des types de polices : polices bitmap, polices évolutives (Intellifonts, polices TrueType), méthodes de compression graphique raster, prise en charge graphique HP-GL/2).

**PCL 1 :** vers 1980 - La fonctionnalité d'impression et d'espace est l'ensemble de fonctions de base fourni pour une sortie de poste de travail simple et pratique pour un seul utilisateur.

**PCL 2 :** vers 1980 - La fonctionnalité EDP (traitement électronique des données)/transaction est un sur-ensemble de PCL 1. Des fonctions ont été ajoutées pour l'impression système multi-utilisateurs à usage général.

**PCL 3** : 1984 - La fonctionnalité de traitement de texte Office est un sur-ensemble de PCL 2. Des fonctions ont été ajoutées pour la production de documents bureautiques de haute qualité et l'augmentation des ppp jusqu'à 300 ppp. Il permettait l'utilisation d'un nombre limité de polices et de graphiques bitmap et prenait en charge HP-GL. PCL 3 a été largement imité par d'autres fabricants d'imprimantes et a été appelé par ces sociétés « LaserJet Plus Emulation ».
(Imprimantes : famille HP DeskJet, imprimante série HP LaserJet, imprimante série HP LaserJet Plus)

**PCL3+ :** Utilisé par les gammes d'imprimantes DeskJet et DesignJet.

**PCL3c :** Utilisé par les gammes d'imprimantes DeskJet et DesignJet.

**PCL3e** : utilisé par les gammes d'imprimantes DeskJet et DesignJet. Désormais également utilisé dans PhotoSmart.

**PCL3GUI** : Utilise RTL et est utilisé par la famille d'imprimantes DeskJet et DesignJet.

**PCLSLEEK** : Utilise RTL et est utilisé par la famille d'imprimantes DeskJet et DesignJet.

**PCL 4** : 1985 - La fonctionnalité de formatage de page est un sur-ensemble de PCL 3. Macros prises en charge, polices bitmap plus grandes et graphiques. (Imprimantes : HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5 :** 1990 - La fonctionnalité Office Publishing est un sur-ensemble de PCL 4. Les nouvelles fonctionnalités de publication incluent la mise à l'échelle des polices et les graphiques HP-GL/2 (vecteur). (Imprimantes : HP LaserJet III)

**PCL 5e :** 1994 - Il s'agit d'une révision majeure, qui inclut de nouvelles fonctionnalités telles que le système de compression adaptatif, l'encodage de caractères à 2 octets, la prise en charge des polices vectorielles et des commandes de configuration bidirectionnelles. Inclut les opérations logiques (correspondant aux ROP GDI) pour améliorer la prise en charge de Windows avant de couper les chemins. (Imprimantes : HP LaserJet 4)

**PCL 5j :** Nouvelles fonctionnalités telles que la prise en charge des caractères 2 octets pour les polices évolutives résidentes japonaises, l'écriture verticale, les formats de papier japonais et les chaînes de caractères. (Imprimantes : HP LaserJet 4PJ)

**PCL 5c :** 1995 - La prise en charge des couleurs et les opérations logiques ont été ajoutées à PCL5. PCL5c est antérieur à PCL5e. Certains modèles prennent également en charge les chemins de détourage. (Imprimantes : HP Color LaserJet, HP PaintJet 300 XL (première imprimante avec PCL5c), HP DeskJet 1200C/1600C (ces numéros de modèle ont été réutilisés et les nouveaux modèles ne sont pas PCL 5c)

**PCL 5ce :** prend en charge les polices de caractères évolutives Agfa Microtype. (Imprimantes : imprimante HP 2500c Pro)

**PCL 6 / XL :** 1996 - PCL 6 ou PCL XL est un nouveau format introduit en 1995, qui n'est compatible avec aucune des versions précédentes de PCL. (Imprimantes : HP LaserJet 5, 5M et 5N)

## Présentation de PCL 6 ##

HP a introduit PCL 6 en 1996 qui était la prochaine évolution du langage PCL et des technologies associées. Il a les composants suivants :

**PCL 6 Enhanced :** fournit une version optimisée pour l'impression à partir d'interfaces utilisateur graphiques (GUI) telles que MS Windows et OS/2

**Norme PCL 6 :** offre une rétrocompatibilité complète avec les anciennes imprimantes HP LaserJet

** Synthèse de polices PCL : ** fournit des polices évolutives, la gestion des polices et le stockage des formulaires et des polices.

La version étendue PCL XL est plus proche de GDI que de nombreuses applications utilisent. Il garantit que moins de traductions ont lieu, ce qui se traduit par des capacités WYSIWYG accrues et de meilleures performances avec les applications qui prennent en charge les échappements implémentés par le pilote amélioré. La sortie du pilote amélioré (PCL XL) peut ne pas être la même que la sortie du pilote standard. Si la sortie n'est pas celle attendue, choisissez plutôt le pilote Standard (PCL5e).

Les commandes PCL 6 Enhanced sont conçues pour répondre de manière optimale aux exigences d'impression graphique des applications basées sur l'interface graphique. Dans la plupart des cas, pour chaque commande d'impression graphique qu'une interface graphique souhaite exécuter, il existe une commande PCL 6 Enhanced correspondante. Cela réduit le nombre de commandes nécessaires pour décrire une page graphique. Chaque commande de PCL 6 Enhanced est conçue pour nécessiter un transfert de données minimal du PC hôte vers l'imprimante. Cela réduit la quantité de données nécessaires pour décrire une page.

Le système d'impression Windows pour la plupart des imprimantes HP LaserJet fournit deux pilotes distincts : standard et amélioré. Le pilote Standard offre une rétrocompatibilité en utilisant les commandes PCL 6 Standard (PCL5e) pour imprimer du texte simple ou des pages mixtes de texte et de graphiques. Le pilote Enhanced utilise les commandes PCL 6 Enhanced qui ont été optimisées pour l'impression de pages graphiques complexes.

## Révisions de classe PCL 6 ##

#### Classe 1.1 ####

**Outils de dessin :** Prend en charge les lignes de dessin, les arcs/ellipses/cordes, les rectangles (arrondis), les polygones, les chemins de Bézier, les chemins coupés, les images raster, les lignes de balayage, les opérations raster.
**Gestion des couleurs :** Prise en charge des palettes 1/4/8 bits, espace colorimétrique RVB/gris. Prend en charge les motifs de demi-teintes personnalisés (max 256 motifs).
**Compression :** prend en charge RLE.
**Unités de mesure :** Pouce, millimètre, dixième de millimètre.
**Gestion du papier :** Prend en charge des ensembles de types de papier personnalisés ou prédéfinis, y compris les formats Lettre, Légal, A4, etc. Possibilité de choisir le papier à partir de l'alimentation manuelle, des bacs, des cassettes. Le papier peut être recto-verso horizontal ou vertical. Le papier peut être orienté en mode portrait, paysage ou rotation à 180 degrés des deux premiers.
**Police :** Prend en charge les polices bitmap ou TrueType, les points de code 8 ou 16 bits. Le choix du jeu de caractères utilise un code de jeu de symboles différent de PCL 5. Lorsque la police bitmap est utilisée, de nombreuses commandes de mise à l'échelle ne sont pas disponibles. Lorsque la police TrueType est utilisée, les descripteurs de longueur variable et les blocs de continuation ne sont pas pris en charge. La police de contour peut être pivotée, mise à l'échelle ou cisaillée.

#### Classe 2.0 ####

**Compression :** Ajout d'une compression JPEG propriétaire appelée JetReady.
**Gestion du papier :** Les supports peuvent être redirigés vers différents bacs de sortie (jusqu'à 256). Ajout des formats de support prédéfinis A6 et japonais B6. Ajout d'un troisième préréglage de cassette, 248 sources de support de plateau externe.
**Police :** Le texte peut être écrit verticalement.

#### Classe 2.1 ####

**Gestion des couleurs :** Ajout de la fonction de correspondance des couleurs.
**Compression :** Ajout de Delta Row.
**Gestion du papier :** L'orientation, la taille du support sont facultatives lors de la déclaration d'une nouvelle page. Ajout des types de papier B5, JIS 8K, JIS 16K, JIS Exec.

#### Classe 3.0 ####

**Gestion des couleurs :** permet d'utiliser différents paramètres de demi-teintes pour les graphiques vectoriels ou matriciels, le texte. Prend en charge les demi-teintes adaptatives.
**Protocole :** prend en charge le relais PCL, permettant aux fonctionnalités PCL 5 d'être utilisées par les flux PCL 6. Cependant, certains états PCL 6 ne sont pas conservés lors de l'utilisation de cette fonction.
**Police :** Prend en charge les polices PCL.
**Visionneuse/Convertisseur :** PCLReader (logiciel gratuit) peut afficher, convertir ou imprimer n'importe quel niveau de PCL 6 (y compris JetReady) sur n'importe quelle imprimante.

## Références ##

* [PCL - Par Wikipédia](https://en.wikipedia.org/wiki/Printer_Command_Language)

