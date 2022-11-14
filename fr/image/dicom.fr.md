{
  "date" : "2019-10-11",
  "keywords" :[ "fichier dicom", "format de fichier dicom", "qu'est-ce qu'un fichier dicom", "fichier", "exemple dicom", "extension de fichier dicom","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - Format de fichier d'imagerie numérique et de communication",
  "description":"En savoir plus sur le format de fichier DICOM et les API qui peuvent créer et ouvrir des fichiers DICOM.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier DICOM ?

DICOM est l'acronyme de Digital Imaging and Communications in Medicine et appartient au domaine de l'informatique médicale. DICOM est utilisé pour l'intégration d'appareils d'imagerie médicale tels que des imprimantes, des serveurs, des scanners, etc. de divers fournisseurs et contient également des données d'identification de chaque patient pour l'unicité. Les fichiers DICOM peuvent être partagés entre deux parties si elles sont capables de recevoir des données d'image au format DICOM. La partie communication de DICOM est le protocole de la couche application et utilise TCP/IP pour communiquer entre les entités. Les versions prises en charge par les services Web sont 1.0, 1.1, 2 ou ultérieures.

## Histoire ##

DICOM a été développé conjointement par l'American College of Radiology (ACR) et la National Electrical Manufacturers Association (NEMA) pour l'échange et la visualisation d'images médicales telles que les IRM, les tomodensitogrammes et les images échographiques. Au départ, il était difficile de décoder les images produites par les machines. Par conséquent, ACR et NEMA ont formé ensemble une équipe en 1983 qui a publié sa première norme, ACR/NEMA 300 en 1985. La deuxième version a été publiée en 1988, qui était plus populaire parmi les fournisseurs, mais on s'est vite rendu compte que la deuxième version devait également être améliorée. La 3ème version de la norme a été publiée en 1993 sous le nom de "DICOM". 3.0 est toujours la dernière version mais elle a été continuellement mise à jour depuis 1993.

## Format de fichier DICOM ##

DICOM est la combinaison d'une définition de format de fichier et d'un protocole de communication réseau. DICOM utilise l'extension .DCM. .DCM existe en deux formats différents, à savoir le format 1.x et le format 2.x. DCM Format 1.x est en outre disponible en deux versions normale et étendue. Les protocoles HTTP et HTTPS sont utilisés pour les services Web de DICOM.

### En-tête de fichier ###

L'en-tête du fichier contient un préambule de fichier de 128 octets et un préfixe DICOM de 4 octets.

**Préambule # 128 Octets**|**Préfixe # 4 Octets “D, I, C, M**

**Préambule** est utilisé pour accéder aux images et autres données dans le fichier DICOM assurant la compatibilité avec les formats de fichiers image couramment utilisés.

**Prefix** contient la chaîne "DICM" en majuscules.

### Base de données ###

Chaque fichier doit contenir un seul ensemble de données représentant l'instance SOP et la classe SOP avec l'IOD associé. L'ensemble de données est la représentation des informations du monde réel. L'ensemble de données contient des éléments de données et les éléments de données contiennent les valeurs des attributs de cet objet. La structure des attributs est spécifiée dans les IOD. Un objet de données DICOM se compose d'un certain nombre d'attributs, y compris des éléments tels que le nom, l'ID, etc., ainsi qu'un attribut spécial contenant les données de pixels de l'image.

### Éléments de données ###

L'élément de données se compose de l'étiquette de l'élément de données, de la longueur de la valeur et de la valeur de l'élément de données. Il existe 5 types d'éléments de données, à savoir les éléments de données obligatoires de type 1, les éléments de données conditionnels de type 1C, les éléments de données obligatoires de type 2, les éléments de données conditionnels de type 2C et les éléments de données facultatifs de type 3. Les trois types de structures d'éléments de données sont les suivants.

**Élément de données avec un VR explicite**

|Numéro de groupe|Numéro d'élément|Représentation de la valeur|Réservé|Longueur de la valeur|Champ de valeur
---|---|---|---|---|---|
|2 octets|2 octets|2 octets|2 octets # 0x00, 0x00|4 octets|"Octets de longueur de valeur"

**Élément de données avec un VR explicite**

|Numéro de groupe|Numéro d'élément|Représentation de la valeur|Longueur de la valeur|Champ de valeur
---|---|---|---|---|
|2 octets|2 octets|2 octets|2 octets|"Octets de longueur de valeur"

**Élément de données avec un VR implicite**


|Numéro de groupe|Numéro d'élément|Longueur de valeur|Champ de valeur
---|---|---|---|
|2 octets|2 octets|4 octets|"Octets de longueur de valeur"

1. **Étiquette d'élément de données** : un entier ordonné qui représente le numéro de groupe et le numéro d'élément
1. **Value Representation VR** : VR est une chaîne de caractères qui représente le VR de l'élément de données.
1. **Longueur de la valeur** : est-ce que l'entier non signé représente la longueur explicite du champ de valeur.
1. **Champ de valeur** : Décrit les valeurs des éléments de données.

## Syntaxe de transfert ##

La syntaxe de transfert est un ensemble de règles de codage pour représenter sans ambiguïté des syntaxes plus abstraites. A l'aide de la syntaxe de transfert, les entités communicantes négocient sur les techniques de codage communes qu'elles supportent.

## SOP ##

L'union de l'IOD et du DIMSE définit une classe SOP. La définition de classe SOP contient les règles et la sémantique qui peuvent restreindre l'utilisation des services dans le groupe de services DIMSE ou les attributs de l'IOD. Des exemples d'éléments de service sont Store, Get, Find, Move, etc. Des exemples d'objets sont des images CT, des images MR, mais incluent également des listes de planification, des files d'attente d'impression, etc.

## Prestations de service ##

DICOM fournit divers services, principalement liés à la communication de données. Chacun est brièvement décrit ci-dessous :


**Store :** Le service DICOM Store envoie des images ou d'autres objets à un système d'archivage et de communication d'images (PACS) ou à un serveur.


**Engagement de stockage :** Le service d'engagement de stockage est utilisé pour confirmer qu'une image a été stockée de manière permanente sur un appareil sur tout type de support.


**Query/retrieve :** Ce service permet à un poste de travail de trouver les listes d'images ou d'autres objets, puis de les récupérer à partir du PACS.


**Liste de travail de modalité :** Le service de liste de travail de modalité donne une liste des procédures d'imagerie qui ont été programmées pour être exécutées par un appareil d'acquisition d'images.


**Imprimer :** Ce service envoie des images à l'imprimante.

## Numéros de port sur IP ##

DICOM utilise les ports TCP et UDP suivants :

1. 104
1. 2761
1. 2762
1. 11112

## Références ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

