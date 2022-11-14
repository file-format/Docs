{
  "date" : "2019-10-11",
  "keywords" :[ "fichier jp2", "format de fichier jp2", "qu'est-ce qu'un fichier jp2", "fichier", "exemple jp2", "extension de fichier jp2","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Format de fichier image",
  "description":"En savoir plus sur le format de fichier JP2 et les API qui peuvent créer et ouvrir des fichiers JP2.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## Qu'est-ce qu'un fichier JP2 ? ##

JPEG 2000 (**JP2**) est un système de codage d'image et une norme de compression d'image de pointe. Il utilise la technologie des ondelettes pour coder du contenu sans perte dans n'importe quelle qualité à la fois. De plus, sans aucune pénalité substantielle dans l'efficacité du codage, JPEG 2000 a la capacité d'accéder et de décoder efficacement le même contenu dans une variété d'autres résolutions et qualités. Les flux de code dans JPEG 2000 sont considérablement évolutifs, ayant des régions d'intérêt qui fournissent la possibilité d'un accès spatial aléatoire.

JPEG 2000 se distingue comme l'un des standards les plus évolutifs. Différentes parties d'une image peuvent être stockées en utilisant diverses qualités. Une augmentation notable des performances peut être obtenue en ordonnant le flux de code de différentes manières. Néanmoins, JP2 nécessite des encodeurs/décodeurs complexes et exigeants en termes de calcul, en raison de cette flexibilité. En comparaison avec JPEG, JPEG 2000 ne produit que des artefacts de sonnerie qui créent des anneaux près du bord de l'image et peuvent être flous, tandis que JPEG utilise des blocs d'artefacts visuels 8 × 8 qui peuvent être à la fois des artefacts de sonnerie et de blocage. Possédant jusqu'à 16384 composants divers avec des dimensions en térapixels, et une précision pouvant atteindre 38 bits/échantillon.

## Histoire ##

En 2000, le comité du Joint Photographic Experts Group a conçu JP2 dans le but d'améliorer leur propre norme JPEG basée sur la transformée en cosinus discrète avec cette nouvelle méthode basée sur les ondelettes. Le comité JPEG visait à fournir leurs méthodes de base sans frais de licence. Dans la licence JP2 gagnant la concurrence entre 20 entreprises, ils ont gagné d'un cheveu. JPEG 2000 a été déclaré norme ISO, bien que la plupart des navigateurs Web ne soient pas prêts à donner un coup de main à JPEG 2000 depuis 2017.

## Parties du système de codage d'image JPEG 2000 ##

Voici les principales parties qui constituent la suite complète de normes pour JPEG 2000.


|Partie|Titre|Description|Numéro
---|---|---|---|
|Partie 1|Système de codage de base| Définit la syntaxe du flux de code. Différentes étapes du décodage des images JPEG 2000. Explique le format de fichier de base JP2, les métadonnées et les droits IP à fournir.|ISO/IEC 15444-1
|Partie 2|Extensions|Définit les extensions pour le flux de code de format de fichier et permet des démonstrations d'échantillons HDR, la spécification de l'espace colorimétrique, le recadrage, les transformations géométriques ; diverses animations, métadonnées et plusieurs flux de code.|ISO/IEC 15444-2
|Partie 3|Motion JPEG 2000 (MJ2 ou MJP2)|Introduire un format de fichier pour les séquences de mouvement, encodant les images dans un flux de code indépendant.|ISO/IEC 15444-3
|Partie 4|Conformité|Déclare les techniques de test pour le codage et le décodage et vérifie les fichiers pour les flux de code à barres et les fichiers JP2.|ISO/IEC 15444-4
|Partie 5|Logiciel de référence|Comprend deux packages de code source (Java, C) qui implémentent le système de codage Core et sont disponibles sous des licences open-source.|ISO/IEC 15444-5
|Partie 6|Format de fichier image composé|Définit le format de fichier JPM et permet l'imagerie de documents multipages pour les applications de type fax. Prend en charge l'utilisation de JBIG2 et JPEG.|ISO/IEC 15444-6
|Partie 8|JPEG 2000 Secured (JPSEC)|Garantit la sécurité des transactions, des contenus et des technologies, et autorise les flux JPEG 2000 bits sécurisés.|ISO/IEC 15444-8
|Partie 9|JPIP|Définit les outils dans un environnement en réseau pour accéder aux métadonnées et aux images, et énonce des protocoles interactifs et efficaces|ISO/IEC 15444-9
|Partie 10|JP3D|Extension volumétrique de la partie 1 et introduction de la dimension Z. Étend le concept de tuiles, de blocs de code, d'enceintes et de fonctionnalités d'accessibilité de région d'intérêt 3D.|ISO/IEC 15444-10
|Partie 11|JPWL|Traite d'une transmission bien organisée sur un réseau sans fil sujet aux erreurs. Cette extension est compatible avec les décodeurs|ISO/IEC 15444-11
|Partie 13|Entry-level Encoder|Définit une implémentation d'encodeur d'entrée de gamme du système de codage Core.|ISO/IEC 15444-13
|Partie 14|JPXML|Une représentation en XML et explique les segments marqueurs et les méthodes d'accès aux données internes de l'imagerie.|ISO/IEC 15444-14
|Partie 15|HTJ2K (En cours de développement)|Spécifie un autre algorithme de codage par blocs. L'algorithme offre un débit multiplié par dix et un codage/décodage sans perte.|

## Format de fichier JP2 ##

JPEG 2000 définit le format de fichier ainsi que le flux de code de la même manière que JPEG-1. Bien que les échantillons d'image soient exclusivement décrits par JPEG 2000, JPEG-1 inclut d'autres informations supplémentaires sur l'espace colorimétrique et la résolution essentielles pour encoder l'image. Si une image est stockée en tant que fichier JPEG 2000, le **.jp2** est utilisé comme extension. Ce format de fichier est encore amélioré par l'extension JPEG 2000 part-2, qui définit les mécanismes d'animation et la configuration de nombreux flux de code en une seule image. L'extension **.jpx** est utilisée lorsque les images sont enregistrées à l'aide de ce format de fichier étendu. Comme les données de flux codé ne sont pas considérées comme étant principalement enregistrées dans des fichiers, aucune extension standard n'est définie à cette fin. Bien qu'à des fins de test, il obtienne fréquemment l'extension **.jpc** ou **.j2k**. Contrairement à JPEG-1, JPEG 2000 choisit une manière différente d'encoder les métadonnées au format XML. La norme 12234-1.4 (du comité ISO TC42) sert de référence entre les balises Exif et les composants XML. JPEG 2000 peut contenir une norme ISO, XMP à l'intérieur.

### Morceaux ###
Les fichiers JPEG 2000 sont constitués de morceaux consécutifs. Chaque bloc a un en-tête de 8 octets : une taille de bloc de 4 octets (gros boutien, octet de poids fort en premier) et un type de bloc de 4 octets - l'une des signatures prédéfinies : "jP" ou "jP2".

Le deuxième bloc doit être de type "ftyp" et avoir un sous-type à l'offset 8. JPEG 2000 défini par un sous-type qui doit être l'une des valeurs : "jp2" (type de fichier \*.JP2), "jp20" (fichier type \*.JPA), "jpm " (type de fichier \*.JPM), "jpx " (type de fichier \*.JPX).

En itérant des morceaux, jusqu'à ce qu'un type inconnu soit détecté, nous composons un fichier image/vidéo JPEG 2000.

### Transformation des couleurs ###

Initialement, la transformation des images de l'espace colorimétrique RVB vers un autre espace colorimétrique est nécessaire. À cette fin, il existe deux méthodes : la transformation de couleur irréversible (ICT) et la transformation de couleur réversible (RCT). Le premier utilise l'espace colorimétrique YC,,B,,C,,R,, et doit être implémenté en point fixe/flottant, tandis que plus tard, un espace colorimétrique YUV modifié et de nature réversible. // // Non limité au modèle RVB, JPEG Le langage 2000 utilise la transformation de composants multiples.

### Carrelage ###

Lorsque la transformation de couleur est terminée, l'image est convertie en régions rectangulaires appelées tuiles qui peuvent être transformées et encodées séparément. La taille de toutes les tuiles sera identique ou l'image entière peut être considérée comme une seule tuile. Le décodeur tire parti de la mosaïque et consomme moins de mémoire ou peut encoder partiellement certaines mosaïques. Bien que cette technique présente un inconvénient de dégradation de la qualité de l'image.

### Transformée en ondelettes ###

L'image après le pavage est transformée en ondelettes qui peut être irréversible ou réversible et mise en œuvre en utilisant le schéma de convolution ou de levage.

### Ratio de compression ###

Selon les caractéristiques physiques d'une image, un gain de compression de 20% est obtenu. La prédiction de redondance spatiale de JPEG 2000 joue un rôle vital dans le processus de compression et les images haute résolution ont tendance à tirer le meilleur parti.

## Applications desservies par la norme ##

* Enregistrement, édition et stockage de vidéos HD basées sur des images
* Imagerie médicale & biométrie
* images satellites, télédétection et détection de mouvement
* Communication client/serveur, distribution réseau et stockage.
* Cinéma numérique, contribution au flux HDTV en direct, matériel audiovisuel numérisé

## Références ##

* [Aperçu de JPEG 2000](https://jpeg.org/jpeg2000)
* [Système de codage d'image JPEG 2000] (https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

