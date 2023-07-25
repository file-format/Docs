{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Format d'échange de matériel",
  "keywords" :[ "MXF", "vidéo matroska", "format mkv", "comment lire des fichiers MXF", "SMPTE", "multimédia", "vidéo" ],
  "description":"En savoir plus sur le format de fichier MXF et les API qui peuvent créer et ouvrir des fichiers MXF.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## Qu'est-ce qu'un fichier MXF ?

Un fichier avec l'extension .mxf est un format de conteneur multimédia qui contient des médias vidéo et audio numériques ainsi que des informations de métadonnées sur le fichier. Il suit la norme SMPTE (Society of Motion Picture and Television Engineers) qui est une association mondiale de professionnels de l'ingénierie, de la technologie et des cadres travaillant dans l'industrie des médias et du divertissement. Les fichiers MXF peuvent être convertis en d'autres formats de fichiers tels que [AVI](/fr/video/avi/) ou [MOV](/fr/video/mov/).

## Format de fichier MXF

Les fichiers MXF sont en fait des fichiers binaires constitués d'une séquence d'octets dans un format défini. Les applications de décodage doivent respecter ce format pour le comprendre et en extraire des informations. Le format permet d'ajouter de nouveaux éléments sans rompre la rétrocompatibilité à l'aide du codage KLV décrit ci-dessous.

* Clé - l'identifiant de l'élément, une étiquette universelle SMPTE (UL)
* Longueur - la longueur des données qui est l'encodage à longueur variable utilisé afin de réduire la quantité d'espace requis pour cet élément
* Valeur - la valeur réelle de l'élément.

### Spécifications du format SMPTE

Le format de fichier MXF a été défini par les spécifications SMPTE suivantes.

* SMPTEST 377-1:2011. Télévision — Format d'échange de matériel (MXF) — Spécification du format de fichier
* SMPTE ST 377-2 (travaux en cours depuis janvier 2012). Syntaxe d'extension codée KLV pour MXF.
* SMPTE ST 378:2004 (Archivé 2010). Télévision — Format d'échange de matériel (MXF) — Modèle opérationnel 1a (article unique, paquet unique)
* SMPTEST 379-1:2009. Format d'échange de matériel (MXF) — Conteneur générique MXF
* SMPTEST 379-2:2010. Format d'échange de matériel (MXF) -- Conteneur générique contraint MXF
* SMPTEST 380:2004. Télévision — Format d'échange de matériel (MXF) — Schéma de métadonnées descriptives-1 (standard, dynamique)
* SMPTEST 381-1:2005. Télévision - Format d'échange de matériel (MXF) - Mappage des flux MPEG dans le conteneur générique MXF (dynamique)
* SMPTEST 381-2:2011. Format d'échange de matériel (MXF) — Mappage des flux MPEG dans le conteneur générique contraint MXF
* SMPTEST 382:2007. Format d'échange de matériel (MXF) - Mappage des flux AES3 et de l'audio Broadcast Wave au conteneur générique MXF
* SMPTEST 383:2008. Télévision — Format d'échange de matériel (MXF) — Mappage des données DV-DIF au conteneur générique MXF
* SMPTEST 384:2005. Télévision — Format d'échange de matériel (MXF) — Mappage d'images non compressées dans le conteneur générique MXF
* SMPTEST 385:2004. Télévision - Format d'échange de matériel (MXF) - Mappage de l'essence et des métadonnées SDTI-CP dans le conteneur générique MXF
* SMPTE ST 386:2004 (Archivé 2010). Télévision — Format d'échange de matériel (MXF) — Mappage des données d'essence de type D-10 au conteneur générique MXF
* SMPTE ST 387:2004 (Archivé 2010). Télévision — Format d'échange de matériel (MXF) — Mappage des données d'essence de type D-11 au conteneur générique MXF
* SMPTE ST 388:2004 (Archivé 2010). Télévision - Format d'échange de matériel (MXF) - Mappage de l'audio codé A-law dans le conteneur générique MXF
* SMPTEST 389:2005. Télévision — Format d'échange de matériel (MXF) — Élément de système de lecture inversée de conteneur générique MXF
* SMPTEST 390:2011. Télévision — Format d'échange de matériel (MXF) — Modèle opérationnel spécialisé "Atom" (représentation simplifiée d'un élément unique)
* SMPTE ST 391:2004 (Archivé 2010). Télévision — Format d'échange de matériel (MXF) — Modèle opérationnel 1b (article unique, ensembles groupés)
* SMPTEST 392:2004. Télévision — Format d'échange de matériel (MXF) — Modèle opérationnel 2a (éléments de la liste de lecture, paquet unique)
* SMPTEST 393:2004. Télévision — Format d'échange de matériel (MXF) — Modèle opérationnel 2b (éléments de la liste de lecture, forfaits jumelés)
* SMPTEST 394:2006. Télévision — Format d'échange de matériel (MXF) — Schéma de système 1 pour le conteneur générique MXF
* SMPTEST 405:2006. Télévision — Format d'échange de matériel (MXF) — Éléments et éléments de données individuels pour le schéma de système de conteneur générique MXF 1
* SMPTEST 407:2006. Télévision — MXF — Modèles opérationnels 3a et 3b
* SMPTEST 408:2006. Télévision — MXF — Modèles opérationnels 1c, 2c et 3c
* SMPTE ST 410 : 2008. Format d'échange de matériel - Partition de flux générique.
* SMPTEST 422:2006. Format d'échange de matériel — Mappage des flux codés JPEG2000 dans le conteneur générique MXF
* SMPTEST 429.4:2006. Emballage D-Cinéma — Application MXF JPEG 2000
* SMPTEST 429.5:2006. Emballage D-Cinema - Fichier de piste de texte chronométré
* SMPTEST 429.6:2006. Emballage D-Cinema — Cryptage d'essence de fichier de piste MXF
* SMPTEST 434:2006. Format d'échange de matériel — Encodage XML pour les métadonnées et les informations sur la structure des fichiers
* SMPTEST 436:2006. Télévision — Mappages MXF pour les lignes VBI et les paquets de données auxiliaires
* ST SMPTE 2019-4:2009. Mappage des unités de codage VC-3 dans le conteneur générique MXF
* SMPTE ST 2037:2009. Mappage de VC-1 dans le conteneur générique MXF
* SMPTE RP 2008:2008. Format d'échange de matériel — Mappage des flux AVC dans le conteneur générique MXF
* SMPTE RP 2057:2011. Transport de métadonnées textuelles dans MXF
* SMPTE EG 41:2004. Format d'échange de matériaux (MXF) — Directive d'ingénierie. Remarque : Ce document n'était plus répertorié sur le site Web de la SMPTE lors de sa consultation en janvier 2012.
* SMPTE EG 42:2004. Format d'échange de matériel (MXF) — Métadonnées descriptives MXF
* SMPTE RDD 3:2008. Spécification d'interopérabilité e-VTR MXF
* SMPTE DDR 9-2009. Spécification d'interopérabilité MXF des produits Sony MPEG Long GOP
* Menu de la feuille de calcul du registre des métadonnées SMPTE.

### Métadonnées structurelles MXF

Les métadonnées structurelles sont fondamentales dans un fichier MXF car elles contiennent des informations utiles sur le contenu du fichier. Les métadonnées MXF contiennent des informations telles que la fréquence d'images, la taille d'image, la date de création du fichier et la date de modification personnalisée. Les métadonnées structurelles décrivent la structure et les fonctionnalités d'un fichier MXF, notamment la description technique des différents composants essentiels et la présentation de la composition de la chronologie de sortie.

## Références

* [MXF - Wikipédia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - Rapport d'avancement](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [Bibliothèque OpenSource C++ pour MXF](http://www.freemxf.org/)

