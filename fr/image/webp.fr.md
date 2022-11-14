{
  "date" : "2019-10-11",
  "keywords" :[ "fichier webp", "format de fichier webp", "qu'est-ce qu'un fichier webp", "fichier", "exemple webp", "extension de fichier webp","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP - Format de fichier d'image raster Google",
  "description":"En savoir plus sur le format de fichier WEBP et les API qui peuvent créer et ouvrir des fichiers WEBP.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier WEBP ?

WebP, introduit par Google, est un format de fichier d'image Web raster moderne basé sur une compression sans perte et avec perte. Il offre la même qualité d'image tout en réduisant considérablement la taille de l'image. Étant donné que la plupart des pages Web utilisent des images comme représentation efficace des données, l'utilisation d'images WebP dans les pages Web entraîne un chargement plus rapide des pages Web. Selon Google, les images WebP sans perte sont 26 % plus petites que les [PNG](/fr/image/png/), tandis que les images WebP avec perte sont 25 à 34 % plus petites que les images [JPEG](/fr/image/jpeg/) comparables. Les images sont comparées sur la base de l'indice de similarité structurelle (SSIM) entre WebP et d'autres formats de fichiers image. WebP est un projet apparenté au format de conteneur multimédia [WebM](https://en.wikipedia.org/wiki/WebM).

## Présentation des fonctionnalités WebP ##

Les images WebP utilisent le processus de compression basé sur la prédiction des pixels de leurs blocs environnants, ce qui entraîne l'utilisation de pixels plusieurs fois dans un seul fichier. Il prend en charge les images animées et devrait prendre en charge davantage de fonctionnalités à l'avenir. Google a mis à disposition le code source [en ligne](https://developers.google.com/speed/webp/download) pour son encodeur et son décodeur afin qu'il puisse être utilisé si nécessaire. L'image WebP prend en charge :

* **Compression avec perte :** la compression avec perte est basée sur le codage d'image clé [VP8](http://en.wikipedia.org/wiki/VP8). VP8 est un format de compression vidéo créé par On2 Technologies pour succéder aux formats VP6 et VP7.
* **Compression sans perte :** Le format de compression sans perte est développé par l'équipe WebP.
* **Transparence :** Le canal alpha 8 bits est utile pour les images graphiques. Le canal Alpha peut être utilisé avec RVB avec perte, une fonctionnalité qui n'est actuellement disponible avec aucun autre format.
* **Animation :** Il prend en charge les images animées aux couleurs vraies.
* **Métadonnées :** Il peut contenir des métadonnées EXIF et XMP (utilisées par les appareils photo, par exemple).
* **Profil couleur :** Il peut avoir un profil ICC intégré.

La compression WebP avec perte utilise le codage prédictif pour coder une image, la même méthode utilisée par le codec vidéo VP8 pour compresser les images clés dans les vidéos. Le codage prédictif utilise les valeurs dans des blocs de pixels voisins pour prédire les valeurs dans un bloc, puis code uniquement la différence.

La compression WebP sans perte utilise des fragments d'image déjà vus afin de reconstruire exactement de nouveaux pixels. Il peut également utiliser une palette locale si aucune correspondance intéressante n'est trouvée.

## Format de fichier ##

Le format de fichier WebP est basé sur le format de document RIFF (format de fichier d'échange de ressources). Le conteneur WebP prend en charge des fonctionnalités allant au-delà du fait de ne contenir qu'une seule image encodée en tant qu'image clé VP8. L'élément de base d'un fichier RIFF est un bloc composé de :


|Champ|Description
---|---|
|Chunk FourCC : 32 bits|Code ASCII à quatre caractères utilisé pour l'identification des blocs
|Taille du bloc : 32 bits (uint32)|La taille du bloc n'incluant pas ce champ, l'identifiant du bloc ou le rembourrage
|Chunk Payload : Chunk Size bytes|La charge utile des données. Si la taille de bloc est impaire, un seul octet de remplissage ~-~- qui devrait être 0 ~-~- est ajouté
|ChunkHeader ('ABCD')|Utilisé pour décrire l'en-tête FourCC et Chunk Size des morceaux individuels, où 'ABCD' est le FourCC pour le morceau. La taille de cet élément est de 8 octets.

### En-tête WebP ###

Un en-tête de fichier WebP est le suivant :

* En-tête RIFF - 32 bits représentant les caractères ASCII 'R' 'I' 'F' 'F'
* Taille du fichier - 32 bits (uint32) représentant la taille du fichier en octets à partir du décalage 8. La valeur maximale de ce champ est de 2 ^ 32 moins 10 octets et donc la taille de l'ensemble du fichier est au plus de 4 Go moins 2 octets .
* 'WEBP' - 32 bits représentant les caractères ASCII 'W' 'E' 'B' 'P'

### Format de fichier avec perte ###

Les images WebP utilisent le format de fichier avec perte si l'image est basée sur un encodage avec perte et ne nécessite aucune fonctionnalité avancée/étendue telle que la transparence, l'animation, l'alpha, etc. Les images avec perte sont plus petites et sont également prises en charge par les anciennes applications.

Le fichier WebP, dans ce cas, se compose de :

* En-tête de fichier WebP de 12 octets
* Morceau VP8

Le [Guide de format et de décodage des données VP8](https://tools.ietf.org/html/rfc6386) illustre les spécifications du format de flux binaire VP8.

### Format de fichier sans perte ###

Cette disposition est utilisée lorsque l'image est basée sur un codage sans perte et qu'il n'y a pas besoin des fonctionnalités avancées fournies par le format externe. Cependant, les applications plus anciennes peuvent ne pas être en mesure de lire ces fichiers.

Le fichier WebP, dans ce cas, se compose de :

* En-tête de fichier WebP de 12 octets
* Morceau VP8L

## Références ##

* [Référence du développeur WebP - Par Google](https://developers.google.com/speed/webp/)
* [Format de fichier WebP - Par Wikipédia](https://en.wikipedia.org/wiki/WebP)

