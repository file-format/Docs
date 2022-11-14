{
  "date" : "2021-02-10",
  "keywords" :[ "fichier jpf", "format de fichier jpf", "qu'est-ce qu'un fichier jpf", "fichier", "exemple jpf", "extension de fichier jpf","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPF - Format de fichier image",
  "description":"En savoir plus sur le format de fichier JPF et les API qui peuvent créer et ouvrir des fichiers JPF.",
  "linktitle" : "JPF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Qu'est-ce qu'un fichier JPF ? ##

Un fichier avec l'extension .jpf est une extension du système de codage d'image JPEG 2000 ISO/IEC 15444 et est appelé sa partie 2 ISO/IEC 15444-2. Elle définit et spécifie un ensemble de méthodes de compression sans perte (préservant les bits) et avec perte pour le codage d'images fixes numériques à tons continus, à deux niveaux, à niveaux de gris, en couleur ou à plusieurs composants. La première partie de l'ISO/CEI 15444-1 fait référence au [JP2](/fr/image/jp2/) qui utilise la technologie des ondelettes pour coder le contenu sans perte et constitue la base des formats de fichier d'image JPEG 2000. Le format de fichier JPF n'a pas reçu un accueil chaleureux en raison de l'utilisation intensive du format JPEG. Les fichiers JPF peuvent être ouverts avec des applications d'imagerie populaires telles qu'Adobe Photoshop 2020, Adobe Illustrator 2020 et CorelDraw Graphics Suite 2020.

## Bref historique

En 2000, le comité du Joint Photographic Experts Group a conçu JP2 dans le but d'améliorer leur propre norme JPEG basée sur la transformée en cosinus discrète avec cette nouvelle méthode basée sur les ondelettes. Le comité JPEG visait à fournir leurs méthodes de base sans frais de licence. Dans la licence JP2 gagnant la concurrence entre 20 entreprises, ils ont gagné d'un cheveu. JPEG 2000 a été déclaré norme ISO, bien que la plupart des navigateurs Web ne soient pas prêts à donner un coup de main à JPEG 2000 depuis 2017. En 2004, le format ISO/IEC 15444-2 a été publiquement accepté comme extension du format de fichier JP2.

## Format de fichier JPF

Le format de fichier JPF définit des processus de décodage étendus pour la conversion de données d'image compressées pour la reconstruction. Il s'agit d'un format de fichier étendu qui spécifie une syntaxe de flux codé étendu contenant des informations pour interpréter les données d'image compressées. Cette norme étendue spécifie un conteneur pour stocker les métadonnées d'image et fournit des conseils sur les processus d'encodage étendus pour convertir les données d'image source en données d'image compressées.

### Organisation des fichiers

JPF est le format de fichier de stockage formel lorsque les fichiers JPX sont stockés dans des systèmes de fichiers informatiques. De plus, d'autres recommandations/normes internationales peuvent définir d'autres cases à utiliser dans les fichiers JPX. Cependant, toutes les informations contenues dans un fichier JPX doivent être au format boîte ; les flux d'octets qui ne sont pas au format de boîte ne doivent pas être trouvés dans le fichier. La structure binaire d'une boîte dans un fichier JPX est identique à celle définie dans le format de fichier [JP2](/fr/image/jp2/).

## Références ##

* [Aperçu de JPEG 2000](https://jpeg.org/jpeg2000)
* [ISO/CEI 15444-2:2004](https://www.iso.org/standard/33160.html)

