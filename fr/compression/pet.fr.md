{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier PET - Fichier de package d'installation Puppy Linux",
  "description":"En savoir plus sur le format de fichier PET et les API qui peuvent créer et ouvrir des fichiers PET.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Qu'est-ce qu'un fichier PET Linux ?

Un fichier PET est un fichier de package d'installation d'application créé et utilisé avec la variante PuppyLinux du système d'exploitation Linux. Il est créé en tant que fichier compressé [TGZ](/fr/compression/tgz/) qui réduit la taille de fichier de l'archive compressée. L'intégrité du format de fichier PET est assurée par la somme de contrôle md5sum qui est ajoutée à la fin du fichier pour vérification à l'extrémité distante. Les fichiers PET peuvent être extraits à l'aide de l'extracteur de fichiers TGZ standard et de WinRAR. Les fichiers PET ont remplacé les anciens fichiers d'installation du package [PUP](/fr/compression/pup/).

## Format de fichier PET

Les fichiers PET sont enregistrés sur disque sous forme d'archives compressées au format de fichier binaire. Cependant, les détails du format de fichier interne du format de fichier PET ne sont pas connus. Semblables aux fichiers d'installation de package [.exe](/fr/executable/exe/) et [.msi](/fr/executable/msi/), les fichiers PET démarrent une installation lorsqu'ils sont exécutés.

## Références

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [Index des packages PET PuppyLinux](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

