{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier de langage de balisage d'appareil portable",
  "description":"En savoir plus sur le format de fichier HDML et les API qui peuvent créer et ouvrir des fichiers HDML.",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## Qu'est-ce qu'un fichier HDML ?

Un fichier avec l'extension .hdml (Handheld Device Markup Language) est un langage de balisage permettant de créer des pages Web pour des appareils électroniques portables tels que des ordinateurs de poche, des smartphones et des appareils d'affichage d'informations. On dit que HDML est une extension du langage [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language). Le HDML est similaire au HTML, mais pour les appareils sans fil et portables dotés de petits écrans tels que les PDA, les téléphones portables, etc. Il a été remplacé par WML pour lequel il a exercé une influence importante.

## Format de fichier HDML - Plus d'informations

HDML est un langage de balisage pour appareils portables basé sur des balises de balisage similaires à HTML. HDML a été soumis au W3C pour normalisation mais il n'est jamais devenu un standard. Ses spécifications de format de fichier sont cependant disponibles sur le [site Web de W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) pour référence. La [syntaxe du langage HDML](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) est disponible à titre de référence pour les développeurs et peut être utilisée pour le développement d'exemples d'applications.

## Éléments HDML

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

