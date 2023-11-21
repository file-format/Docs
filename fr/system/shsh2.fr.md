{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier SHSH2 - Format de fichier iOS SHSH Blob",
  "description":"Découvrez ce qu'est un fichier SHSH2.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Qu'est-ce qu'un fichier SHSH2 ?

Un fichier SHSH2, également connu sous le nom de blob SHSH ou ECID SHSH, est une signature numérique utilisée par Apple pour authentifier et vérifier les mises à jour du micrologiciel des appareils iOS tels que les iPhones, iPads et iPods. Il contient un identifiant unique pour l'appareil appelé ECID (Exclusive Chip ID). Il contient également des informations sur la version du micrologiciel installé sur l'appareil.

## Format de fichier SHSH2 - Plus d'informations

Les fichiers SHSH2 sont enregistrés sur disque au format de fichier binaire et les détails de la structure de fichier interne de ce format de fichier ne sont pas accessibles au public.

Lorsqu'une nouvelle version d'iOS est installée sur un appareil Apple tel qu'un iPhone, iPad ou Mac, un fichier SHSH2 est généré. Ce fichier SHSH2 est envoyé aux serveurs Apple qui lisent et vérifient ce fichier de signature numérique. En fonction de ces informations, le serveur autorise ou empêche l'installation.

La même chose se produit lorsqu'une mise à jour est demandée. Lorsqu'un utilisateur demande une mise à jour ou une restauration de son appareil via iTunes ou un autre logiciel, les serveurs d'Apple vérifient que le fichier SHSH2 correspond à l'ECID et à la version du micrologiciel de l'appareil avant d'autoriser la mise à jour.

## Les références

* [SHSH Blob - Par Wikipédia](https://en.wikipedia.org/wiki/SHSH_blob)
* [Épargnant TSS](https://tsssaver.1conan.com/v2/)

