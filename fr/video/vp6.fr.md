{
  "date" : "2021-02-15",
  "keywords" :[ "fichier vp6", "format de fichier vp6", "qu'est-ce qu'un fichier vp6", "fichier", "exemple vp6", "extension de fichier vp6","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - Fichier vidéo TrueMotion",
  "description":"En savoir plus sur le format de fichier VP6 et les API qui peuvent créer et ouvrir des fichiers VP6.",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Qu'est-ce qu'un fichier VP6 ?

VP6 est un format vidéo de compression avec perte introduit par les technologies On2 en mai 2003. Il fait partie d'une série de codecs vidéo développés par TrueMotion, notamment V3, V4 et V5. Le format a été utilisé peu de temps dans le domaine de la radiodiffusion, comme avec les rapports de la BBC et le logiciel QuickLink. VP6 a été remplacé par VP7 Codec en janvier 2005 avec une meilleure compatibilité de compression.

## Format de fichier VP6

Les spécifications complètes des fichiers V6 ne sont pas disponibles publiquement. On2 a initialement rendu les spécifications publiques, mais elles ont rapidement été rendues non disponibles pour les utilisateurs généraux. Une documentation non officielle du format de fichier VP6 est disponible sur [wiki multimédia](https://wiki.multimedia.cx/index.php?title=On2_VP6) qui peut être consultée pour référence par le développeur.

### Macroblocs (Mo)

Semblable à MPEG-2, MPEG-4 parties 2 et 10, chaque image vidéo d'un fichier VP6 est composée d'un tableau de 16x16 macroblocs (Mo). Chaque Mo peut être dans l'un des modes suivants :

* Intra Mo
* Inter MB, null MV, référence de trame précédente
* Inter MB, différentiel MV, référence trame précédente
* Inter MB, quatre MV, référence de trame précédente
* Inter MB, MV 1, référence de trame précédente
* Inter MB, MV 2, référence de trame précédente
* Inter MB, null MV, référence de trame mise en signet
* Inter MB, différentiel MV, référence de trame en signet
* Inter MB, MV 1, référence de trame avec signet
* Inter MB, MV 2, référence de trame avec signet

### En-tête de trame

L'en-tête de trame d'un VP6 est comme indiqué ci-dessous qui suit le paquet de bits gros boutien.

|Syntaxe|Nombre de bits|Type|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 signifie une trame intra|
|qp |6 |Non signé |Paramètre de quantification plage valide 0..63|
|marqueur| 1| Constante | 0=VP61/62, 1=VP60|
|if (frame_mode == 0) { | 0 | |égal à INTRA_FRAME|
|version |5| Constante | 6=VP60/61, 7=VP60(Arts électroniques), 8=VP62|
|version2 |2| Constante |0=VP60, 3=VP61/62|
|entrelacé |1| Booléen |true (1) signifie que l'entrelacement sera utilisé|
|if (marqueur==1 ou version2==0) {||||
|décalage |16 |Sans signe| décalage du tampon secondaire (octets relatifs au début du tampon) |
|}||||
|dim_y |8| Non signé | Hauteur du macrobloc de la vidéo |
|dim_x |8| Non signé | Largeur du macrobloc de la vidéo |
|render_y |8 |Non signé |Hauteur d'affichage de la vidéo|
|render_x |8 |Non signé |Largeur d'affichage de la vidéo|
|}autrement{||||
|if (marqueur==1 ou version2==0) {||||
|offset |16 |Unsigned |Décalage du tampon secondaire (octets relatifs au début du tampon)|
|}||||
|}||||

## Références

* [VP6 Wikipédia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

