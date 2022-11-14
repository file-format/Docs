{
  "date" : "2021-02-10",
  "keywords" :[ "fichier jpx", "format de fichier jpx", "qu'est-ce qu'un fichier jpx", "fichier", "exemple jpx", "extension de fichier jpx","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX - Format de fichier image",
  "description":"En savoir plus sur le format de fichier JPX et les API qui peuvent créer et ouvrir des fichiers JPX.",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Qu'est-ce qu'un fichier JPX ? ##

Un fichier avec l'extension .jpx est une extension du format de fichier JPEG 2000. Il utilise principalement la compression JPEG 2000 et fournit également des fonctionnalités avancées telles que plusieurs couches pour une image, divers espaces colorimétriques, l'opacité et des flux de code fragmentés. JPX permet également d'autres compressions telles que JBIG, CCITT Group3, CCITT Group4, etc. en plus de la compression JPEG 2000. Le format de fichier JPX a été approuvé en tant que norme [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html), mais n'a pas pu recevoir un accueil chaleureux en raison de l'utilisation intensive de [JPEG ](/fr/image/jpeg/). Les applications pouvant ouvrir les fichiers JPX incluent Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 et CorelDraw Graphics Suite 2020.

## Bref historique

En 2000, le comité du Joint Photographic Experts Group a conçu JP2 dans le but d'améliorer leur propre norme JPEG basée sur la transformée en cosinus discrète avec cette nouvelle méthode basée sur les ondelettes. Le comité JPEG visait à fournir leurs méthodes de base sans frais de licence. Dans la licence JP2 gagnant la concurrence entre 20 entreprises, ils ont gagné d'un cheveu. JPEG 2000 a été déclaré norme ISO, bien que la plupart des navigateurs Web ne soient pas prêts à donner un coup de main à JPEG 2000 depuis 2017. En 2004, le format ISO/IEC 15444-2 a été publiquement accepté comme extension du format de fichier JP2.

## Format de fichier JPX

Le format de fichier JPX a été formulé pour répondre aux exigences des applications qui avaient besoin de structures de données au-delà de la fonctionnalité définie par le format de fichier [JP2](/fr/image/jp2/). Un fichier JP2 avec des extensions non compatibles pourrait prêter à confusion sur le marché où certains lecteurs peuvent interpréter certains fichiers JP2 mais pas d'autres. JPX est la solution pour éviter de tels problèmes dans les applications.

### Identification du fichier

Les fichiers JPX sont stockés en tant que [JPF](/fr/image/jpf/) lorsqu'ils sont stockés dans un système de fichiers informatique traditionnel. C'est pourquoi le terme JPX est le moins utilisé par rapport au JPF. Un fichier JPX commence par les octets suivants :

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Organisation des fichiers

Semblable à JP2, un fichier JPX est une collection de boîtes ayant une structure binaire avec les boîtes disposées dans un ordre contigu. La première case donne le début du fichier avec son premier octet et le dernier octet de la dernière case représente le dernier octet du fichier.
La structure binaire d'une boîte dans un fichier JPX est identique à celle définie dans le format de fichier [JP2](/fr/image/jp2/).

### Stockage de CodeStream dans JPX

Le format de fichier JPX permet de diviser le flux codé de l'image en fragments. Cela permet de modifier une seule tuile de l'image et d'écrire la tuile modifiée à la fin du fichier sans réécrire le fichier entier. Le format de fichier original [JP2](/fr/image/jp2/) limite le stockage de l'intégralité du flux codé dans une partie contiguë du fichier, ce qui peut être problématique pour les applications d'édition d'images qui souhaitent modifier une seule mosaïque de l'image et obtenir la prise en charge ci-dessus par le format de fichier JPX. La fragmentation du flux codé d'image rend le format de fichier JPX supérieur au format de fichier JP2. De plus, le format de fichier JPX permet de combiner plusieurs flux codés et de produire un résultat rendu. Les flux codés peuvent être combinés en tant que composition et animation.

## Références ##

* [Aperçu de JPEG 2000](https://jpeg.org/jpeg2000)

