{
  "date" : "2021-06-11",
  "keywords" :[ "mp2", "fichier mp2", "extension", "format", "qu'est-ce qu'un fichier mp2", "musique", "format de fichier mp2"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier MP2 et les API qui peuvent créer, convertir et ouvrir des fichiers MP2.",
  "title" :"MP2 - Format de fichier audio MPEG Layer 2",
  "linktitle" : "MP2",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Qu'est-ce qu'un fichier MP2 ?

Un fichier MP2, également appelé fichier MPA, est un fichier audio compressé avec la couche II de MPEG-1 ou MPEG-2 ; un format de compression audio avec perte défini par ISO/IEC 11172-3 avec MPEG-1 Audio Layer I et MPEG-1 Audio Layer III ([MP3](/fr/audio/mp3/)), pour réduire la taille du fichier audio. Alors que MP3 est plus populaire que MP2 en raison de sa taille plus petite et de sa disponibilité sur Internet. Par conséquent, le MP2 reste une norme vitale pour la diffusion audio.

## Format de fichier MP2

MPEG Audio Layer II (MP2) est l'algorithme de base des normes MP3. Le codage MPEG-1 Audio Layer 2 a été obtenu à partir du codec audio MUSICAM. Tout a commencé par le projet Digital Audio Broadcast (DAB) en Allemagne dans le cadre du programme de recherche EUREKA. L'Eureka 147 contenait trois éléments principaux : le codage et le multiplexage de transmission, la modulation COFDM et le codage audio MUSICAM (modèle de masquage Universal Sub-band Integrated Coding And Multiplexing). Le MUSICAM était l'un des rares encodages capables d'atteindre une qualité audio élevée à des débits binaires de l'ordre de 64 à 192 kbit/s par canal monophonique. L'objectif était de fournir un faible retard, une faible complexité, une robustesse aux erreurs, des unités d'accès courtes et de répondre aux exigences techniques de la radiodiffusion, des télécommunications et de l'enregistrement sur des supports de stockage numériques.

MP2 est un encodeur audio de sous-bande, qui peut être compressé dans le domaine temporel avec une banque de filtres à faible retard générant 32 composants de domaine de fréquence. Par comparaison, MP3 est un encodeur audio à transformation avec banque de filtres hybrides, ce qui signifie que la compression est appliquée dans le domaine fréquentiel après une transformation hybride à partir du domaine temporel. L'encodeur MP2 peut exploiter les redondances entre canaux en utilisant un codage d'intensité "stéréo conjoint" facultatif.

### Spécifications du format de fichier MP2

Le format de fichier MP2 est basé sur des trames numériques successives de 1152 intervalles d'échantillonnage avec quatre formats possibles :

- format mono
- format stéréo
- format stéréo commun codé en intensité (stéréo non pertinent)
- format double canal (non corrélé)
Certaines spécifications techniques importantes de MP2 sont données dans le tableau ci-dessous :

|Spécification| Descriptif|
---|---|
|**Taux d'échantillonnage**| 32, 44,1 et 48 kHz |
|**Débits binaires**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 et 384 kbit/s|
|**Fréquences d'échantillonnage supplémentaires**|16, 22,05 et 24 kHz|
|**Débits supplémentaires**|8, 16, 24, 40 et 144 kbit/s|
|**Prise en charge multicanal**|Jusqu'à 5 canaux audio pleine gamme et un canal LFE (Low Frequency Enhancement channel)|

## Références ##

* [MPEG-1 Audio Layer II - Par Wikipédia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

