{
  "date" : "2021-02-01",
  "keywords" :["usdz", "fichier usdz", "format de fichier usdz", "format de fichier", "3d","téléchargement de fichier usdz"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - Format ZIP de description de scène universelle",
  "description":"En savoir plus sur le format de fichier USDZ et les API qui peuvent ouvrir et créer des fichiers USDZ.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Qu'est-ce qu'un fichier USDZ ?

Un fichier avec .usdz est une archive ZIP non compressée et non cryptée pour le format de fichier [USD](/fr/3d/usd/) (Universal Scene Description) qui contient et proxies pour des fichiers d'autres formats (tels que des textures et des animations) intégrés dans l'archive et les exécute directement avec l'environnement d'exécution USD sans avoir besoin de déballer. Les fichiers USDZ sont des packages dont la conception est basée sur la nouvelle abstraction de niveau Ar d'un package. Usdz a été enregistré auprès de l'IANA et a un nom de type de support de modèle et un nom de sous-type de vnd.usd+zip et ses détails peuvent être trouvés sur [page d'enregistrement IANA] (https://www.iana.org/assignments/media- types/modèle/vnd.usdz+zip).

## Format de fichier USDZ

Les fichiers USDZ sont basés sur le format de fichier ZIP qui archive les fichiers individuels dans son conteneur. Cela permet au destinataire de simplement décompresser le contenu et d'utiliser les fichiers de description de scène USD normaux pour travailler et inspecter. Presque tous les systèmes d'exploitation offrent une prise en charge intégrée des formats de fichiers ZIP et le choix de ce format d'archivage plutôt que n'importe quelle méthode personnalisée permet aux fichiers USDZ d'être facilement utiles en tant que protocole de transport simple.

### Contraintes ZIP

Le format de fichier USDZ utilise le format de fichier ZIP sans aucune "compression" ni "cryptage". Cela visait par conception à répondre à deux exigences :

* Pour un package déjà chargé en mémoire ou en tant que fichier unique sur disque, les API sont disponibles en USD pour accéder aux données contenues dans l'image
* Il ne devrait pas être nécessaire d'extraire des fichiers sur un disque ou d'allouer plus de stockage de tas

Avec USDZ, ces deux exigences sont remplies car la plupart des formats d'image eux-mêmes autorisent des schémas de compression internes, ce qui se traduit par une taille de fichier compacte.

### Exigences de mise en page

Les packages USDZ nécessitent la disposition des fichiers dans le package, c'est-à-dire que les données de chaque fichier doivent commencer à un multiple de 64 octets à partir du début du package. Cependant, le package doit commencer par un fichier natif [USD](/fr/3d/usd/) en cas de ciblage du package avec une simple référence. Dans un tel cas, ce premier fichier USD est appelé la couche par défaut. Les clients souhaitant fournir un "contenu diffusable" peuvent également envisager d'autres contraintes de mise en page.

## Téléchargement du fichier USDZ
Étant donné que les fichiers usdz contiennent d'autres images et fichiers usd de haute qualité, ils peuvent occuper une plus grande capacité de stockage sur le disque. Vous trouverez ici un fichier d'exemple USDZ simple et plus petit à télécharger :

- [Échantillon.usdz](../échantillon.usdz)

## Références

* [Spécifications du format de fichier USDZ] (https://graphics.pixar.com/usd/docs/Usdz-File-Format-Specification.html)

