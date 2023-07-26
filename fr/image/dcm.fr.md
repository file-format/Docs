{
  "date" : "2019-10-11",
  "keywords" :[ "fichier dcm", "format de fichier dcm", "qu'est-ce qu'un fichier dcm", "fichier", "exemple dcm", "extension de fichier dcm","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier DCM - Fichier d'informations médicales numériques",
  "description":"En savoir plus sur le format de fichier DCM et les API permettant de créer et d'ouvrir des fichiers DCM.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## Qu'est-ce qu'un fichier DCM ?

Les fichiers avec l'extension .dcm représentent une image numérique qui stocke les informations médicales des patients telles que les IRM, les tomodensitogrammes et les images échographiques. Les fichiers DCM utilisent le format de fichier image [DICOM](/fr/image/dicom/) (Digital Imaging and Communications in Medicine) et peuvent inclure des informations sur le patient à titre de référence. Il a été développé par la [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) et visait à normaliser le format de fichier d'imagerie pour la distribution et la visualisation des images médicales.

## Format de fichier MCD

Les fichiers DCM stockent les informations au format d'image DICOM. Ces fichiers stockent l'ensemble de données, qui sont des informations du monde réel, qui représentent une instance SOP liée à un IOD DICOM. Les métadonnées du fichier DICOM sont stockées dans le fichier suivi du flux d'octets de l'ensemble de données réel.

### Méta-informations du fichier DICOM ##

Chaque fichier DICOM comprend un en-tête d'informations d'identification pour l'ensemble de données encapsulé qui se compose de :
* Un préambule de fichier de 128 octets
* Préfixe DICOM de 4 octets
* Fichier Meta Elements

Cet en-tête est indispensable pour chaque fichier DICOM.

### Éléments de méta de fichier ###
|Nom d'attribut|Balise|Type| Attribut Description
---|---|---|---|
|Préambule de fichier|Aucun champ d'étiquette ou de longueur|1|Un champ fixe de 128 octets disponible pour le profil d'application ou l'utilisation spécifiée par l'implémentation. S'ils ne sont pas utilisés par un profil d'application ou une implémentation spécifique, tous les octets doivent être mis à 00H. Les lecteurs ou les mises à jour d'ensembles de fichiers ne doivent pas se fier au contenu de ce préambule pour déterminer si ce fichier est ou n'est pas un fichier DICOM.
|Préfixe DICOM|Aucun champ de balise ou de longueur|1|Quatre octets contenant la chaîne de caractères "DICM". Ce préfixe est destiné à être utilisé pour reconnaître que ce fichier est ou non un fichier DICOM.
|Longueur du groupe de méta-informations de fichier|(0002,0000)|1|Nombre d'octets suivant cet élément de méta-fichier (fin du champ Valeur) jusqu'au dernier élément de méta-fichier du groupe 2 inclus
|Version de méta-informations de fichier|(0002,0001)|1|Il s'agit d'un champ de deux octets où chaque bit identifie une version de cet en-tête de méta-informations de fichier. Dans la version 1, la première valeur d'octet est 00H et la deuxième valeur d'octet est 01H. version de PS3.10. Tous les autres bits ne doivent pas être vérifiés.
|UID de classe SOP de stockage multimédia|(0002,0002)|1|Identifie de manière unique la classe SOP associée à l'ensemble de données. Les UID de classe SOP autorisés pour le stockage multimédia sont spécifiés dans PS3.4 - Profils d'application de stockage multimédia.
|UID de l'instance SOP de stockage multimédia|(0002,0003)|1|Identifie de manière unique l'instance SOP associée à l'ensemble de données placé dans le fichier et suivant les métadonnées du fichier.
|Transfer Syntax UID|(0002,0010)|1|Identifie de manière unique la syntaxe de transfert utilisée pour coder l'ensemble de données suivant. Cette syntaxe de transfert ne s'applique pas aux métadonnées de fichier.
|UID de classe d'implémentation|(0002,0012)|1|Identifie de manière unique l'implémentation qui a écrit ce fichier et son contenu. Il permet d'identifier sans ambiguïté le type d'implémentation qui a écrit le fichier en dernier en cas de problème d'échange.
|Nom de la version d'implémentation|(0002,0013)|3|Identifie une version pour un UID de classe d'implémentation (0002,0012) en utilisant jusqu'à 16 caractères du répertoire.
|Titre de l'entité d'application source|(0002,0016)|3|Titre de l'entité d'application DICOM (AE) de l'AE qui a écrit le contenu de ce fichier (ou qui l'a mis à jour pour la dernière fois). S'il est utilisé, il permet de remonter à la source des erreurs en cas de problème d'échange de média.
|UID du créateur des informations privées|(0002,0100)|3|L'UID du créateur des informations privées (0002,0102).
|Informations privées|(0002,0102)|1C|Contient des informations privées placées dans les métadonnées du fichier. Le créateur doit être identifié en (0002,0100). Obligatoire si l'UID du créateur d'informations privées (0002,0100) est présent.

### Encapsulation de l'ensemble de données ###

Un fichier DICOM contient un seul ensemble de données qui représente une seule instance SOP liée à une seule classe SOP. L'UID de syntaxe de transfert des métadonnées de fichier DICOM doit définir la syntaxe de transfert utilisée pour coder l'ensemble de données.

### Prise en charge des informations de gestion de fichiers ###

La couche de format de support fournit les informations de gestion de fichiers suivantes si nécessaire pour un profil d'application DICOM donné.

* Identification du propriétaire du contenu du fichier

* Statistiques d'accès aux fichiers (par exemple, date et heure de création)

* Contrôle d'accès aux fichiers d'application

* Contrôle d'accès aux supports physiques (par exemple, protection en écriture)

## Références ##
* [Norme DICOM](https://www.dicomstandard.org/current/)
* [Format de fichier DICOM](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

