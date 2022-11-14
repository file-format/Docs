{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier WMV",
  "description":"En savoir plus sur le format de fichier WMV et les API qui peuvent créer et ouvrir des fichiers WMV.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## Qu'est-ce qu'un fichier WMV ?

L'Advanced Systems Format (ASF) est un conteneur multimédia numérique conçu principalement pour stocker et transmettre des flux multimédias. Microsoft Windows Media Video (WMV) est le format vidéo compressé et Microsoft Windows Media Audio (WMA) est le format audio compressé avec des métadonnées supplémentaires dans le conteneur ASF développé par Microsoft. Une fois que les fichiers WMV ou WMA sont encodés avec les codecs Windows Media Video et Windows Media Audio, ils sont représentés avec l'extension .asf. WMV compresse les fichiers volumineux pour un meilleur taux de transmission sur un réseau tout en maintenant la qualité de la vidéo. WMV est spécialement conçu pour fonctionner sur tous les appareils Windows. Après la normalisation par la Society of Motion Picture and Television Engineers (SMPTE), WMV est désormais considéré comme un format standard ouvert.

## Histoire ##

Avec l'aide des codecs propriétaires de Microsoft, un nouveau format vidéo compressé a été développé en 1999, connu sous le nom de WMV7, basé sur MPEG-4 Partie 2. Des améliorations ont été ajoutées dans deux autres versions, à savoir WMV8 et 9. Microsoft a soumis une 9 ^^ ème version ^^ de WMV à SMPTE pour la normalisation en 2003, qui a finalement été normalisée en 2006 sous le nom de SMPTE 421M également connu sous le nom de VC-1. L'idée derrière le WMV était de développer un format multimédia qui pourrait être pris en charge par tous les matériels et logiciels pris en charge par Microsoft. De plus, un autre objectif majeur était de transmettre des flux vidéo sur Internet dans un scénario optimal. Après la normalisation de SMPTE, WMV est également devenu un format vidéo pour les disques Blu-ray.

## Spécifications du format de fichier

### Récipient

En règle générale, WMV est emballé dans un conteneur ASF, mais en plus, le conteneur Matroska ou AVI peut également le prendre en charge avec les extensions .mkv et .avi respectivement.

### Windows Media Vidéo 9

Bien qu'il existe divers codecs audio et vidéo disponibles dans la série Windows Media Video 9 pour la création et la lecture de médias numériques, le codec WMV-9 est le dernier et le meilleur codec vidéo car il peut atteindre une compression optimale à partir de débits binaires très faibles, c'est-à-dire 160 x 120 à 10 Kbps à 1920 x 1080 à 4-8 Mbps pour une variété de vidéos HD.

### Structure du codec

WMV-9 a un format de couleur interne 8 bits 4:2:0. Comme toutes les autres normes de compression vidéo populaires MPEG-1 et H.261, WMV-9 utilise une compensation de mouvement basée sur les blocs et un schéma de transformation spatiale. En général, on peut dire que ces normes effectuent une compensation de mouvement bloc par bloc à partir de l'image reconstruite précédente à l'aide d'une quantité 2D appelée vecteur de mouvement (MV) pour signaler le déplacement spatial. Le bloc actuel est formé à l'aide de la prédiction des valeurs à partir de la trame reconstruite précédente de même taille qui est déplacée de la position actuelle par le vecteur de mouvement. Finalement, l'erreur résiduelle est calculée comme la différence entre le bloc prédit compensé en mouvement et le bloc réel. Cette erreur résiduelle est transformée à l'aide d'une transformée linéaire de compactage en énergie puis quantifiée et codée entropiquement.

Les coefficients de transformation quantifiés sont décodés entropiquement, déquantifiés et transformés en inverse pour produire une approximation de l'erreur résiduelle côté décodeur, qui est ensuite ajoutée à la prédiction compensée en mouvement pour générer la reconstruction. La description de haut niveau du codec est illustrée dans l'image suivante.

Le reste de la section discutera des nouvelles améliorations de WMV-9 qui le différencient du reste des solutions de codage vidéo comme les normes MPEG. WMV-9 a des trames intra (I), prédites (P) et bidirectionnelles prédites (B). Les trames intra sont celles qui sont codées indépendamment et ne dépendent pas d'autres trames. Les trames prédites sont des trames qui dépendent d'une trame dans le passé. Le décodage d'une trame prédite ne peut avoir lieu qu'après que toutes les trames de référence antérieures à la trame courante à partir de la trame (I) la plus récente ont été décodées. Les trames B sont des trames qui ont deux références : une dans le passé temporel et une dans le futur temporel. Les trames B sont transmises à la suite de leurs références, ce qui signifie que les trames B sont émises dans le désordre pour s'assurer que leurs références sont disponibles au moment du décodage. Les trames B dans WMV-9 ne sont pas utilisées comme référence pour les trames suivantes. Cela place les images B en dehors de la boucle de décodage, ce qui permet de prendre des raccourcis lors du décodage des images B sans dérive ni artefacts visuels à long terme. La définition ci-dessus des images I, P et B est valable pour les séquences progressives et entrelacées.

Les performances des codecs vidéo sont comparées à leur tracé débit-distorsion (RD). C'est une courbe 2D qui montre la distorsion produite par la compression à un certain débit.

WMV-9 a résolu ce problème avec l'introduction d'une variété de techniques énumérées ci-dessous :

1. Transformation de taille de bloc adaptative

2. Ensemble de transformation de précision limité

3. Compensation de mouvement

4. Quantification et déquantification

5. Codage entropique avancé

6. Filtrage de boucle

7. Codage de trame B avancé

8. Codage entrelacé

9. Lissage de chevauchement

10. Outils à faible taux

11. Compensation de la décoloration

## Références ##

* [https://bytescout.com/blog/2014/10/windows-media-video-format.html](https://bytescout.com/blog/2014/10/windows-media-video-format.html )
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)
* [http://citeseerx.ist.psu.edu/viewdoc/download?doi#10.1.1.101.488&rep#rep1&type#pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi#10.1 .1.101.488&rep#rep1&type#pdf)

