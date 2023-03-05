{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier CRL - Liste de révocation de certificats",
  "description":"En savoir plus sur le format de fichier CRL et les API qui peuvent créer et ouvrir des fichiers CRL.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## Qu'est-ce qu'un fichier CRL ?

Un fichier CRL (Certificate Revocation List) est une liste noire de certificats numériques X.509 qu'une autorité de certification (CA) révoque avant la date de révocation qui leur a été attribuée. Il contient des informations sur le problème et la date de révocation qui permettent aux administrateurs de sécurité de bloquer les certificats numériques concernés. CRL n'inclut pas les certificats expirés car son objectif principal est de notifier les certificats non approuvés et non valides.

Les applications qui peuvent **ouvrir les fichiers CRL** incluent OpenSSL, Microsoft IIS Server et Citrix NetScaler.

## Format de fichier CRL - Plus d'informations

Les fichiers CRL contiennent des informations dans la norme X.509 qui définit également sa sémantique pour le partage des informations de clé publique. D'autres informations contenues dans un fichier CRL peuvent inclure le délai pour lequel les certificats ont été révoqués, la raison de la révocation, le numéro de série du certificat révoqué et l'horodatage.


### Principales raisons pour lesquelles les certificats sont ajoutés à la CRL

Il peut y avoir plusieurs raisons pour lesquelles le certificat de votre site Web est révoqué et ajouté à la CRL. Certains d'entre eux pourraient l'être;

1. La clé privée de votre certificat a été compromise
1. Votre certificat n'est pas valide ou a été mal émis par l'AC
1. Les détails organisationnels associés au certificat sont modifiés et l'AC émet un nouveau certificat
1. Toute autre raison inévitable pour laquelle le certificat a été révoqué

## Références

* [Institut national des normes et de la technologie (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [RFC 5280 de l'IETF (Internet Engineering Task Force)](https://tools.ietf.org/html/rfc5280)
* [Liste de révocation de certification](https://en.wikipedia.org/wiki/Certificate_revocation_list)

