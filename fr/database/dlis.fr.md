{
  "date" : "2023-01-16",
  "keywords" :[ "DLIS", "qu'est-ce qu'un fichier DLIS", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier DLIS et les API qui peuvent créer et ouvrir des fichiers DLIS.",
  "title" :"Format de fichier DLIS - Fichier de données de journal de puits",
  "linktitle" : "DLIS",
  "menu" : {
    "docs" : {
      "identifier":"database-dlis",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Qu'est-ce qu'un fichier DLIS ?

Le format de fichier .dlis est un format de fichier standard pour le stockage et l'échange de données de diagraphie de puits dans l'industrie pétrolière et gazière. Le format a été développé par le comité Logging Industry Data Standard (LIDS) et signifie « Digital Log Information Standard ». Le format est conçu pour stocker les données des diagraphies de puits d'une manière facile à lire, à écrire et à échanger entre différents systèmes.

Les fichiers DLIS contiennent un ensemble d'enregistrements logiques qui décrivent les données de journal de puits et leurs caractéristiques, telles que le type de données de journal (par exemple résistivité, rayons gamma), les unités de mesure et l'emplacement des données dans le puits. Les données de journal réelles sont stockées dans des fichiers binaires séparés et sont référencées par les enregistrements logiques du fichier DLIS.

## Brève information sur les données de journal de puits

Les données de diagraphie de puits sont un enregistrement des mesures prises à différentes profondeurs dans un puits, généralement pendant le processus de forage ou après le forage du puits. Ces mesures peuvent inclure diverses propriétés physiques, chimiques et/ou géophysiques de la roche et des fluides dans le puits. Voici quelques exemples de données de diagraphie de puits :

- Résistivité électrique : mesure de la capacité d'une roche à résister au passage d'un courant électrique
- Rayon gamma : une mesure de la radioactivité naturelle de la roche
- Porosité : une mesure de la quantité d'espaces ouverts ou de pores dans la roche
- Sonic : une mesure du temps qu'il faut à une onde sonore pour traverser la roche
- Densité : mesure de la masse d'une roche par unité de volume
- Lithologie : une mesure du type de roche ou de la formation

Les données des journaux de puits sont utilisées à diverses fins dans l'industrie pétrolière et gazière, telles que :

- Identifier la localisation et la qualité des formations hydrocarburées
- Evaluer le potentiel de production d'un puits
- Planification et suivi de la réalisation et de la stimulation d'un puits
- Suivi du comportement du puits dans le temps

## Relation avec PPDM

PPDM (Professional Petroleum Data Management) est une norme de gestion des données de l'industrie pétrolière et gazière qui fournit un modèle de données commun pour la gestion des données de puits et de production. Le modèle de données PPDM définit un ensemble d'objets de données standard et de relations qui peuvent être utilisés pour organiser et gérer les données de diagraphie de puits, y compris les données DLIS.

Le modèle de données PPDM comprend des objets de données pour les données de puits et de production, telles que les puits, les en-têtes de puits, les journaux de puits et les données de production. Il inclut également les relations entre ces objets de données, telles que la relation entre un puits et les journaux de puits qui lui sont associés.

Le modèle de données PPDM fournit un moyen cohérent et conforme aux normes de l'industrie d'organiser et de gérer les données des journaux de puits, y compris les données DLIS. Il permet à différentes organisations de partager et d'échanger des données à l'aide d'un modèle de données commun, améliorant ainsi l'interopérabilité des données et réduisant les coûts d'intégration des données.

L'utilisation conjointe du modèle de données PPDM et des données DLIS permet de stocker et de gérer les données des journaux de puits d'une manière conforme aux normes de l'industrie et facilement accessible à d'autres systèmes et applications.

## Références
* [Format pour les données numériques de journal de puits](http://w3.energistics.org/rp66/V1/Toc/main.html)
* [DLIS - Organisation des données](http://w3.energistics.org/rp66/V1/Toc/main.html)

