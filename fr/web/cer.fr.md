{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "extension", "fichier", "format", "web", "certificat", "langue" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - Format de fichier de certificat",
  "description":"En savoir plus sur le format de fichier CER et les API qui peuvent créer et ouvrir des fichiers CER.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Qu'est-ce qu'un fichier CER ? ##

Un fichier avec une extension .cer est responsable du stockage de certaines informations sur le certificat du propriétaire et la clé publique spécifique. Ce format de fichiers ne peut pas stocker les clés privées et a la capacité de stocker un seul certificat qui est x509. Les autorités de certification spécifiquement sécurisées sont celles qui appartiennent à HTTPS, un protocole de confiance et sécurisé pour la navigation
Le CER est un certificat de votre serveur. Il est généralement reçu par l'autorité de certification du domaine. CER est généralement considéré comme identique à [CRT](/fr/web/crt/), bien que les deux aient le même format de certificat SSL mais soient des extensions de nom de fichier différentes.
Ceux-ci peuvent être utilisés sur les systèmes d'exploitation en ouvrant simplement un navigateur et en vérifiant la sécurité du navigateur ou du site Web utilisé.

## Bref historique ##

En 1995, Thawte est devenue la première autorité de certification à résoudre le problème des certificats SSL publics (lien de socket sécurisé) hors des États-Unis. Après cela, il y a une série d'autorités de ce type qui ont été fondées de 1995 à 2020.

## Format de fichier CER ##

Ces fichiers peuvent être simplement
* Le PKC S#7 comprend l'encodage Base64 ASCII
* Ses extensions de fichier sont p7b ou p7cZ
* Pour le contenu binaire, le certificat serait DER ou pkcs12/pfx.
Il existe de nombreux types de fichiers de certificat avec des spécifications uniques :
* .pem, lorsqu'une organisation usThawteificate chaînage ce format est bien connu pour créer des certificats
* .arm, lorsque la méthode d'extraction d'une certification assistée auto-signée est requise, le format spécifié à cet effet est .arm. Il est représenté en codage ASCII base 64.
* .der, Il se compose de données binaires. Cela signifie qu'il ne peut être utilisé que pour un seul certificat
* .pfx (PKC512), Il s'agit d'une clé privée correspondant à un certificat délivré par l'AC ou un certificat auto-signé. Ce format est bien connu pour la conversion d'une implémentation SSL à l'autre.


