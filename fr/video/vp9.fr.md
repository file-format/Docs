{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "Fichier", "Extension", "Format de fichier", "Format vidéo", "Vidéo TrueMotion", "VPX", "On2 Technologies"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 - Fichier vidéo TrueMotion",
  "description":"En savoir plus sur le format de fichier VP9 et les API qui peuvent créer et ouvrir des fichiers VP9.",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## Qu'est-ce qu'un fichier VP9 ?

Google a développé le codec VP9 en tant que norme de codage vidéo open source libre de droits en tant que successeur de VP8. Il a été conçu à l'origine pour compresser le contenu ultra HD sur YouTube, car il étend et améliore l'efficacité de codage de son prédécesseur. Si on parle des codecs VPX d'origine, ils sont issus d'On2 Technologies, qui a été assimilé par Google en 2010. Google a ensuite open-source le codec. Les deux formats VP8 et VP9 sont disponibles sous une licence BSD gratuite qui permet aux opérateurs d'organiser les compétences d'encodage ou de décodage dans les logiciels exclusifs et les logiciels open source sans révéler leur code source.

## Caractéristiques techniques du VP9

* VP9 fournit une résolution maximale de 8192x4352 jusqu'à 120 ips et plusieurs espaces colorimétriques, avec Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 et sRGB
* La gamme complète de cas d'utilisation Web et mobile, de la compression à faible débit binaire à l'ultra-HD de haute qualité, avec une prise en charge supplémentaire de l'encodage 10/12 bits et du HDR, est entièrement prise en charge par ce format
* Il peut réduire les débits binaires vidéo jusqu'à 50 % par rapport aux autres
* Il est préparé pour le streaming adaptatif et est utilisé par YouTube et d'autres fournisseurs de vidéos Web bien connus
* Les appareils Chrome, Opera, Edge, Firefox et Android, ainsi que des millions de téléviseurs intelligents, prennent en charge le décodage de ce codec
* Les résolutions vidéo supérieures à 1080p sont modifiées via VP9 et permettent une compression sans perte
* Différents espaces colorimétriques comme Rec. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240 et sRGB sont pris en charge par VP9
* La vidéo HDR utilisant Hybrid Log-Gamma et Perceptual Quantizer peut également être prise en charge par VP9


## Bref historique

* Le développement du codec vidéo VP9 a commencé en 2011 et son décodeur a été ajouté au navigateur Web Chromium en décembre 2012
* Sa première version du navigateur Web Google Chrome est sortie en février 2013 et a publié le décodage à ce moment-là
* Google a publié Chrome 29.0.1547 avec la prise en charge finale de VP9 en août 2013
* En octobre 2013, un décodeur VP9 instinctif a été ajouté à FFmpeg
* Mozilla a ajouté la maintenance VP9 à Firefox en décembre 2013 dans la version 2 qui a ensuite été publiée le 18 mars 2014
 

## Fonctionnement du VP9

Habituellement, la vidéo 4K augmente la qualité de l'image en réduisant des pixels spécifiques, le codec VP9 et HEVC les agrandissent pour réduire le débit binaire et la taille du fichier. Bien que cela puisse sembler contradictoire, le moteur d'encodage prend les pixels les plus grands et les transforme en une meilleure productivité de résolution. La vidéo source, comprenant des images vidéo, est codée ou compressée pour créer un flux binaire vidéo compressé. Chaque image séparée est d'abord divisée en blocs de pixels. Les blocs sont ensuite examinés à la recherche de rejets tridimensionnels et les connexions séquentielles entre les cadres sont évaluées pour tirer parti des zones qui ne peuvent pas être modifiées. Ceux-ci sont codés via des vecteurs de mouvement qui garantissent les qualités du bloc donné sur la trame suivante. Les informations résiduelles sont codées à l'aide d'une compression binaire efficace.

## Références

* [VP9 Wikipédia](https://en.wikipedia.org/wiki/VP9)
* [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [Noix de coco](https://www.coconut.co/)

