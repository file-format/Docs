{
  "date" : "2019-12-13",
  "keywords" :[ "fichier ppt", "format de fichier ppt", "qu'est-ce qu'un fichier ppt", "fichier", "exemple ppt", "extension de fichier ppt","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier PPT et les API qui peuvent créer et ouvrir des fichiers PPT.",
  "title" :"PPT - Format de fichier PowerPoint",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier PPT ?

Un fichier avec l'extension PPT représente un fichier PowerPoint composé d'une collection de diapositives à afficher sous forme de diaporama. Il spécifie le format de fichier binaire utilisé par Microsoft PowerPoint 97-2003. Un fichier PPT peut contenir plusieurs types d'informations différents tels que du texte, des puces, des images, du multimédia et d'autres objets OLE intégrés. Microsoft a proposé un nouveau format de fichier pour PowerPoint, connu sous le nom de [PPTX](/fr/presentation/pptx/), à partir de 2007, basé sur Office OpenXML et différent de ce format de fichier binaire. Plusieurs autres programmes d'application tels que OpenOffice Impress et Apple Keynote peuvent également créer des fichiers PPT.

## Bref historique ##

Microsoft a introduit le format de fichier PPT avec la sortie de PowerPoint en 1987. Le format binaire stable était partagé par défaut dans PowerPoint 97-2003 pour Windows. Le format de fichier binaire est pris en charge pour la lecture et l'écriture par les versions les plus récentes de PowerPoint, y compris PowerPoint 2016.

## Spécifications du format de fichier ##

Depuis son introduction, le format de fichier PPT a subi plusieurs révisions pour l'ajout de nouvelles fonctionnalités et améliorations. Les dernières spécifications de version disponibles sont celles de la révision 6.0 qui ont été publiées en août 2018 et qui ne doivent pas être mélangées avec le numéro de produit réel du format de fichier PPT car Microsoft ne fournit plus de modifications pour ce format.

### Présentation du format de fichier ###

Certains des composants clés d'un format de fichier PPT sont les suivants :

#### Diapositives ####

Les données utilisateur telles que les formes, le texte, les animations et les médias sont ajoutées à une présentation dans une diapositive. Une présentation peut contenir une ou plusieurs diapositives qui s'affichent sous forme de diaporama lors de l'exécution d'une présentation. Une présentation contient des diapositives principales et des diapositives principales de titre qui servent de modèle pour les propriétés visuelles communes des diapositives de présentation. Il existe également une diapositive principale de notes et une diapositive principale de document qui ont un objectif similaire et fournissent des propriétés visuelles communes pour toutes les diapositives de notes et tous les documents imprimés.

#### Formes ####

Les formes sont des objets qui permettent aux utilisateurs d'ajouter une variété de contenus à une diapositive sous la forme de formes d'espace réservé, d'images et de graphiques. Les formes d'une diapositive principale définissent des données communes pour des groupes de formes.

#### Formes d'espaces réservés ####

Ce sont des espaces réservés spéciaux qui servent de conteneurs pour une variété d'objets. Différentes formes d'espace réservé peuvent être utilisées pour fournir des indices pour insérer des types spécifiques de formes telles que des tableaux ou des graphiques. À l'intérieur d'une diapositive, une forme d'espace réservé adopte les propriétés visuelles d'une diapositive principale principale, d'une diapositive principale de titre ou d'une diapositive principale de notes.

#### Objets externes ####

Les objets externes tels que l'audio incorporé et lié, la vidéo liée, les objets OLE incorporés et liés et les hyperliens peuvent être incorporés dans une diapositive. Ces objets peuvent être utilisés pour activer des objets liés pour accéder à des ressources externes pendant un diaporama.

### Structures des formats de fichiers ###

Les formats de fichiers binaires PowerPoint consistent à suivre les flux pour représenter la structure et les données globales du document.

* Flux d'utilisateurs actuel
* Flux de documents PowerPoint
* Flux d'images
* Informations récapitulatives et informations récapitulatives sur le document (facultatif)

Les spécifications complètes du format de fichier DOC sont fournies par [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) et doivent être consultées en référence aux sections mentionnées dans les détails suivants.

#### Flux d'utilisateurs actuel ####

Il conserve l'enregistrement du dernier utilisateur qui a ouvert le document et son nom doit être « Utilisateur actuel ».

#### Flux de documents PowerPoint ####

Enregistre toutes les informations sur une présentation PowerPoint et explique sa mise en page et son contenu. Il s'agit d'un flux obligatoire dont le nom DOIT être "Document PowerPoint". Le contenu de ce flux est spécifié par une séquence d'enregistrements de niveau supérieur. Les restrictions de classement partiel sur la séquence d'enregistrements sont spécifiées dans les enregistrements PersistDirectoryAtom et UserEditAtom.

En tant qu'enregistrements de conteneur, les enregistrements DocumentContainer, MainMasterContainer (section 2.5.3), HandoutContainer (section 2.5.8), SlideContainer (section 2.5.1) et NotesContainer (section 2.5.6) sont chacun la racine d'une arborescence d'enregistrements de conteneur. et enregistrements atomiques. À l'intérieur de tout enregistrement de conteneur, d'autres enregistrements peuvent exister qui ne sont pas explicitement répertoriés en tant qu'enregistrements enfants. Les enregistrements inconnus sont identifiés lorsque le champ recType de la structure RecordHeader (section 2.3.1) contient une valeur non spécifiée par l'énumération RecordType (section 2.13.24). Ces enregistrements inconnus, s'ils sont rencontrés, DOIVENT être ignorés et PEUVENT<1> être préservés. Les enregistrements inconnus peuvent être ignorés en recherchant les octets recLen vers l'avant à partir de la fin de la structure RecordHeader.

Chaque fois que ce flux est écrit, de nouveaux enregistrements de niveau supérieur, une modification de l'utilisateur, peuvent être ajoutés au flux existant, ou tout le contenu du flux peut être remplacé par une séquence mise à jour d'enregistrements de niveau supérieur. Si le flux entier n'est pas remplacé, tout enregistrement de niveau supérieur existant précédemment qui comprenait une modification utilisateur précédente peut être rendu obsolète par les enregistrements de niveau supérieur ajoutés ultérieurement qui comprennent la modification utilisateur actuelle.

#### Flux d'images ####

Il s'agit d'un flux facultatif qui contient des données sur les images contenues dans une présentation PowerPoint. Son nom DOIT être "Images". Le contenu de ce flux est spécifié par l'enregistrement OfficeArtBStoreDelay comme spécifié dans [MS-ODRAW] section 2.2.21.

#### Flux d'informations récapitulatives ####

Il conserve des statistiques sur le document conformément à la norme Microsoft Office. Le nom du flux d'informations récapitulatives doit être "\005SummaryInformation", où \005 est le caractère avec la valeur 0x0005, et non la chaîne littérale "\005". Ce flux DEVRAIT être omis pour les documents chiffrés. Le contenu de ce flux est spécifié dans [MS-OSHARED] section 2.3.3.2.1.

#### Flux d'informations sur le résumé du document ####

Un flux facultatif dont le nom DOIT être "\005DocumentSummaryInformation", où \005 est le caractère avec la valeur 0x0005, et non la chaîne littérale "\005". Ce flux PEUT<2> être omis pour les documents chiffrés. Le contenu de ce flux est spécifié dans la section 2.3.3.2.2 de [MS-OSHARED].

#### Flux d'informations récapitulatives cryptées ####

Un flux facultatif dont le nom DOIT être "EncryptedSummary". Ce flux n'existe que dans un document chiffré. Le contenu de ce flux est spécifié dans [MS-OFFCRYPTO] section 2.3.5.4.

#### Stockage de signature numérique ####

Un stockage facultatif dont le nom DOIT être "_xmlsignatures". Il PEUT être omis et PEUT être ignoré. Le contenu de ce stockage est spécifié dans [MS-OFFCRYPTO] section 2.5.2.

#### Stockage de données XML personnalisé ####

Un stockage optionnel dont le nom DOIT être "MsoDataStore". Le contenu du stockage est spécifié dans [MS-OSHARED] section 2.3.6.

#### Flux de signatures ####

Un flux optionnel dont le nom DOIT être "_signatures". Il DEVRAIT être omis et PEUT être ignoré. Le contenu de ce flux est spécifié dans [MS-OFFCRYPTO] section 2.5.1.

## Références ##

* [Spécifications du format de fichier PPT](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED] : Types de données et structures d'objets communs Office](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Structure de chiffrement des documents Office](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [Formats de fichier PowerPoint] (https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

