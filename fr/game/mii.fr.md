{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier Age of Empires 2 Expansion Replay MGX et les API qui peuvent créer et ouvrir des fichiers MGX.",
  "title" :"Fichier MII - Format de fichier d'avatar virtuel Wii",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## Qu'est-ce qu'un fichier MII ?

Un fichier MII est un format de fichier d'avatar virtuel utilisé pour stocker des avatars virtuels sur la console de jeu Nintendo Wii. Ces fichiers contiennent des informations telles que l'apparence, les mouvements et les animations de l'avatar. Ils peuvent être utilisés dans des jeux, des applications de réseaux sociaux et d'autres logiciels sur la Wii. Un fichier MII contient également d'autres caractéristiques sur l'avatar telles que le sexe, la couleur des cheveux, la couleur de la peau, les traits du visage et le type d'yeux.

Vous pouvez ouvrir un fichier MII à l'aide de [My Avatar Editor](https://rc24.xyz/goodies/mii/).

## Format de fichier MII

Le format de fichier MII est défini en détail sur [Wii Brew](https://wiibrew.org/wiki/Mii_data). Les chaînes d'un fichier MII sont stockées au format Unicode (UTF-16), big-endian.

### Bloc MI

Les données du fichier MII sont stockées sur la Wiimote en deux blocs. Chaque bloc a une longueur de 750 octets, avec un CRC de 2 octets, soit un total de 752 octets. Chaque bloc commence par une valeur de 4 octets ('RNCD') qui semble être le nombre magique pour le format de fichier MII.

## Comment créer des fichiers MII ?

Il existe plusieurs façons de créer des avatars pour la Nintendo Wii :

1. "Utilisation de la chaîne Mii intégrée sur la Wii :" Cette chaîne vous permet de créer des avatars personnalisés à l'aide de divers outils, notamment les traits du visage, la forme du corps et les vêtements. Une fois que vous avez créé votre avatar, vous pouvez l'enregistrer en tant que fichier Mii et l'utiliser dans des jeux et d'autres logiciels sur la Wii.

1. "Utilisation de l'application Mii Maker sur la Nintendo 3DS :" L'application Mii Maker vous permet de créer des avatars personnalisés à l'aide de l'écran tactile et de l'appareil photo de votre Nintendo 3DS. Une fois que vous avez créé votre avatar, vous pouvez l'enregistrer en tant que fichier Mii et le transférer sur votre Wii via une connexion sans fil.

1. "Utilisation d'un logiciel tiers :" Certains développeurs ont créé un logiciel qui vous permet de créer des avatars personnalisés pour la Wii. Ce logiciel est généralement conçu pour être utilisé sur un ordinateur et peut nécessiter des étapes supplémentaires pour transférer l'avatar sur votre Wii.

1. "Utilisation d'avatars prédéfinis :" Certains jeux et autres logiciels sur Wii peuvent être livrés avec des avatars prédéfinis que vous pouvez utiliser.

Dans tous les cas, vous devez avoir un compte Nintendo pour créer et enregistrer votre avatar sur la Wii.

## Références

* [Mon éditeur d'avatar] (https://rc24.xyz/goodies/mii/)
* [Wii Brew] (https://wiibrew.org/wiki/Mii_data)

