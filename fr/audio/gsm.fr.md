{
  "date" : "2021-08-05",
  "keywords" :[ "gsm", "fichier", "extension", "format", "Audio", "Global System for Mobile Audio", "extension gsm", "fichiers gsm"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier GSM et les API qui peuvent créer et ouvrir des fichiers GSM.",
  "title" :"GSM - Système mondial de format de fichier audio mobile",
  "linktitle" : "GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-05"
}

## Qu'est-ce qu'un fichier GSM ?

GSM est une extension de fichier associée à Global System for Mobile Audio Format Files. Les fichiers contenant des extensions GSM peuvent être ouverts sur les plates-formes Linux, Windows et Mac OS. Le format de fichier GSM appartient à la catégorie des fichiers audio.

Un fichier GSM est encodé avec un codec de compression sonore CBR (Constant Bitrate) avec perte. Le taux d'échantillonnage dans un fichier audio GSM est de 8000 échantillons/seconde alors que le débit de données est d'environ 13 kbps. Le débit binaire dans les fichiers GSM garantit la qualité lors de l'enregistrement vocal. De plus, le format de fichier GSM est également connu comme le format standard mondial à utiliser dans les téléphones mobiles et les fichiers WAV peuvent également être facilement encodés à l'aide d'un format de fichier GSM. Tout problème avec un fichier GSM peut être facilement résolu par l'utilisateur lui-même sans passer par un expert.

Les utilisateurs peuvent également convertir des fichiers GSM aux formats [MP3](/fr/audio/mp3/) et [MP4](/fr/audio/mp4/).

## Bref historique du format de fichier GSM

GSM est un format de fichier audio qui a été créé pour la téléphonie Internet en Europe. Il a été développé par l'Institut européen des normes de télécommunications (ETSI) pour être utilisé comme un cellulaire numérique 2G utilisé dans les téléphones mobiles et les tablettes. Aujourd'hui, il est utilisé pour stocker des enregistrements de conversations téléphoniques et de messages vocaux.

## Spécifications du format de fichier GSM ##

GSM fonctionne sur un réseau structuré qui se compose des sections suivantes :

- **Modulation** : Il s'agit d'un processus de transformation des données d'entrée dans un format facilement transmissible. Les données transmises sont démodulées à la réception
- **Débit de transmission** : GSM est un système numérique qui a un débit binaire supérieur à 270 kbps
- **Plage de fréquence de liaison montante** : 933-960 MHz
- **Plage de fréquence de liaison descendante** : 890 – 915 MHz
- **Channel Spacing** : Cela signifie l'espacement entre les barrières adjacentes qui doit être d'environ 200 kHz
- **Distance duplex** : C'est l'espace entre les fréquences montantes et descendantes qui doit être de 80 MHz
- **Codage vocal** : le GSM utilise le codage prédictif linéaire (LPC). LPC comprime le débit binaire. Lorsque le signal audio passe à travers un filtre et imite le conduit vocal. GSM encode la parole à 13kbps

| Format de compression audio | Algorithme | Taux d'échantillonnage | Transformer le débit binaire | Latence | RBC | VBR | Stéréo | Multicanal |
| ------------------------ | --------- | ----------- | ------------------ | -------- | --- | --- | ------ | ------------ |
| |
| GSM-RH | VSELP | 8kHz | 5,6 kbit/s | 25 ms | Oui | Non | Non | Non |
| GSM-FR | RPE-LTP | 8kHz | 13 kbit/s | 20–30 ms | Oui | Non | Non | Non |
| GSM-EFR | ACELP | 8kHz | 12,2 kbit/s | 20–30 ms | Oui | Non | Non | Non |

## Références ##

* [GSM - Par Wikipédia](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)

