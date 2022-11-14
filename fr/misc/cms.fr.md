{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier CMS - Fichier de profil de service Connection Manager",
  "description":"En savoir plus sur le fichier CMS et les API qui peuvent créer et ouvrir des fichiers CMS.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Qu'est-ce qu'un fichier CMS ?

Un fichier CMS est un fichier de données qui contient des informations de profil utilisées par Microsoft Windows Connection Manager. Il permet aux utilisateurs distants de se connecter à un réseau à l'aide de ces informations de profil. Les informations stockées dans un fichier CMS incluent des données sur le système d'exploitation de l'utilisateur et les autorisations utilisées pour établir une connexion entre un utilisateur distant et le réseau. Les administrateurs CMS utilisent le kit d'administration de Connection Manager (CMAK) pour générer des fichiers CMS.

## Format de fichier CMS - Plus d'informations

Les fichiers CMS ne se trouvent généralement pas sur les machines des utilisateurs. Étant donné qu'ils sont utilisés spécifiquement pour permettre aux utilisateurs distants d'accéder à un réseau, vous les trouverez sur des ordinateurs utilisés pour se connecter à un réseau d'entreprise ou à un bureau spécialement conçu à cet effet. Dans la plupart des cas, il est utilisé pour se connecter à un réseau organisationnel tel qu'un réseau privé virtuel (VPN) dédié à une entreprise uniquement. En tant qu'administrateur réseau, vous configurerez l'accès à un tel réseau avec Connection Manager pour lui permettre d'accéder au réseau de l'entreprise à partir d'un emplacement distant.

### Qu'est-ce qu'un CMS indépendant ?

Un fichier de profil CMS est créé à l'aide de Connection Manager et est fourni avec d'autres fichiers de configuration avant d'être fourni à l'utilisateur distant. Ces fichiers supplémentaires peuvent inclure un fichier CMP et un fichier INF qui sont regroupés dans un fichier [EXE](/fr/executable/exe/). Ce package complet est fourni à l'utilisateur distant pour se connecter au réseau.

## Références

* [Comprendre et configurer le gestionnaire de connexion Windows] (https://docs.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

