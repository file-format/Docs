{
  "date" : "2019-11-25",
  "keywords" :[ "fichier jpeg", "format de fichier jpeg", "qu'est-ce qu'un fichier jpeg", "fichier", "exemple jpeg", "extension de fichier jpeg","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - Format de fichier image",
  "description":"En savoir plus sur le format de fichier JPEG et les API qui peuvent créer et ouvrir des fichiers JPEG.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## Qu'est-ce qu'un fichier JPEG ? ##

Un JPEG est un type de format d'image enregistré à l'aide de la méthode de compression avec perte. L'image de sortie, résultant de la compression, est un compromis entre la taille de stockage et la qualité de l'image. Les utilisateurs peuvent ajuster le niveau de compression pour atteindre le niveau de qualité souhaité tout en réduisant la taille de stockage. La qualité de l'image est négligeable si une compression 10:1 est appliquée à l'image. Plus la valeur de compression est élevée, plus la dégradation de la qualité de l'image est importante.

## Spécifications du format de fichier ##

Le format de fichier d'image JPEG a été normalisé par le Joint Photographic Experts Group et, par conséquent, le nom JPEG. Le format a été le choix de stockage et de transmission d'images photographiques sur le web. Presque tous les systèmes d'exploitation ont maintenant des visionneuses qui prennent en charge la visualisation des images JPEG, qui sont souvent stockées avec l'extension JPG également. Même les navigateurs Web prennent en charge la visualisation des images JPEG. Avant d'entrer dans les spécifications du format de fichier JPEG, le processus global des étapes impliquées dans la création JPEG doit être mentionné.

### Étapes de compression JPEG ###

**Transformation :** Les images couleur sont transformées de RVB en une image de luminance/chrominance (l'œil est sensible à la luminance, pas à la chrominance, de sorte que la partie chrominance peut perdre beaucoup de données et peut donc être fortement compressée.

**Sous-échantillonnage :** Le sous-échantillonnage est effectué pour la composante colorée et non pour la composante de luminance. Le sous-échantillonnage est effectué soit à un rapport de 2:1 horizontalement et 1:1 verticalement (2h 1 V). Ainsi, la taille de l'image se réduit puisque la composante 'y' n'est pas touchée, il n'y a pas de perte notable de qualité d'image.

**Organisation en groupes :** Les pixels de chaque composant de couleur sont organisés en groupes de 8 × 2 pixels appelés « unités de données » si le nombre de lignes ou de colonnes n'est pas un multiple de 8, la ligne du bas et les colonnes les plus à droite sont dupliquées.

**Transformation en cosinus discrète :** La transformation en cosinus discrète (DCT) est ensuite appliquée à chaque unité de données pour créer une carte 8 × 8 des composants transformés. La DCT implique une certaine perte d'informations en raison de la précision limitée de l'arithmétique informatique. Cela signifie que même sans la carte, il y aura une certaine perte de qualité d'image, mais elle est normalement faible.

**Quantification :** Chacun des 64 composants transformés de l'unité de données est divisé par un nombre distinct appelé son "coefficient de quantification (QC)", puis arrondi à un nombre entier. C'est là que les informations sont perdues irrémédiablement, les grands QC causent plus de pertes. En général, la plupart des outils JPEG permettent d'utiliser les tables QC recommandées par la norme JPEG.

**Codage :** Les 64 coefficients transformés quantifiés (qui sont maintenant des nombres entiers) de chaque unité de données sont codés à l'aide d'une combinaison de codage RLE et Huffman.

**Ajout d'en-tête :** La dernière étape ajoute l'en-tête et tous les paramètres JPEG utilisés et génère le résultat.

Le décodeur JPEG utilise les étapes en sens inverse pour générer l'image originale à partir de l'image compressée.

### Structure du fichier ###

Une image JPEG est représentée comme une séquence de segments où chaque segment commence par un marqueur. Chaque marqueur commence par l'octet 0xFF suivi d'un indicateur de marqueur pour représenter le type de marqueur. La charge utile suivie du marqueur est différente selon le type de marqueur. Les types de marqueurs JPEG courants sont répertoriés ci-dessous :

|Nom court|Octets|Charge utile|Nom|Commentaires
---|---|---|---|---|
|SOI|0xFF, 0xD8|aucun|Début de l'image|
|S0F0|0xFF, 0xC0|taille variable|Début de trame|
|S0F2|0xFF, 0xC2|taille variable|Début de l'image|
|DHT|0xFF, 0xC4|taille variable|Définir les tables de Huffman|
|DQT|0xFF, 0xDB|taille variable|Définir table(s) de quantification|
|DRI|0xFF, 0xDD|4 octets|Définir l'intervalle de redémarrage|
|SOS|0xFF, 0xDA|taille variable|Début de l'analyse|
|RSTn|0xFF, 0xD//n//(/fr//n//#0..7)|aucun|Redémarrer|
|APPn|0xFF, 0xE//n//|taille variable|spécifique à l'application|
|COM|0xFF, 0xFE|taille variable|Commentaire|
|EOI|0xFF, 0xD9|aucun|Fin de l'image|

Dans les données codées entropie, après tout octet 0xFF, un octet 0x00 est inséré par l'encodeur avant l'octet suivant, de sorte qu'il ne semble pas y avoir de marqueur là où aucun n'est prévu, empêchant les erreurs de cadrage. Les décodeurs doivent sauter cet octet 0x00. Cette technique, appelée [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (voir la section F.1.2.3 de la spécification JPEG), n'est appliquée qu'aux données codées entropie, pas aux données de charge utile du marqueur . Notez cependant que les données codées par entropie ont leurs propres marqueurs ; spécifiquement les marqueurs de réinitialisation (0xD0 à 0xD7), qui sont utilisés pour isoler des blocs indépendants de données codées entropie pour permettre un décodage parallèle, et les encodeurs sont libres d'insérer ces marqueurs de réinitialisation à intervalles réguliers (bien que tous les encodeurs ne le fassent pas).

