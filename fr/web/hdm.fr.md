{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier HDM - Fichier de langage de balisage d'appareil portable",
  "description":"En savoir plus sur le format de fichier HDM et les API qui peuvent créer et ouvrir des fichiers HDM.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## Qu'est-ce qu'un fichier HDM ?

Un fichier HDM est un fichier de page Web en langage de balisage créé dans le langage HDML (Handheld Device Markup Language). Il contient des balises de balisage similaires au langage [HTML](/fr/web/html/), mais est conçu pour les appareils électroniques portables tels que les smartphones et les PDA. Les [spécifications du format de fichier HDML](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) ont été soumises au W3C pour normalisation, mais n'ont pas pu devenir une norme. HDM est basé sur les spécifications de format de fichier [HDML](/fr/web/hdml/) disponibles sur le site Web de W3.

## Format de fichier HDM - Plus d'informations

Le fichier HDM se compose de balises de balisage qui sont rendues sur un site Web conçu visuellement sur des appareils portables. Les fichiers HDM sont copiés sur les appareils à l'aide du protocole HDTP (Handheld Device Transport Protocol) au lieu du protocole HTTP utilisé pour les pages HTML.

## Éléments de fichier HDML

Vous trouverez ci-dessous une liste d'éléments qui fournissent un environnement d'exécution pour HDML et sont appelés agents utilisateur.

|Élément|Description|
---|---|
|Cartes|Il s'agit du bloc de construction fondamental de HDML. Il affiche et permet à l'utilisateur d'interagir avec des cartes d'informations. |
|Decks|Les cartes HDML sont regroupées en decks. Un deck HDML est similaire à une page HTML en ce qu'il est identifié par l'URL [RFC1738] et est l'unité de contenu demandée à un serveur et mise en cache par l'agent utilisateur.|
|Actions|Les actions peuvent être de type PREV, SOFT1-SOFT8 et HELP. Ceux-ci sont abstraits et sont pris en charge dans l'interface utilisateur d'une manière spécifique à l'agent utilisateur.|
|Activités|Une activité est comme un groupe de cartes liées qui exécutent une fonction logique. Ceux-ci peuvent s'étendre sur un ou plusieurs ponts. Le modèle de navigation et d'état HDML est structuré autour d'activités.|
|Navigation basée sur l'historique|L'agent utilisateur conserve un historique des cartes affichées à l'utilisateur. Chaque carte consultée est ajoutée à l'historique des cartes. L'agent utilisateur permet à l'utilisateur de revenir facilement à la carte précédente dans l'historique.|

## Références

* [HDML - Wikipédia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [Spécifications HDML - Écoles W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

