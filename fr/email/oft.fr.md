{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - Fichier de modèle d'e-mail Microsoft Outlook",
  "description":"En savoir plus sur le format de fichier OFT et les API qui peuvent créer et ouvrir des fichiers OFT.",
  "linktitle" : "OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier OFT ?

Les fichiers avec l'extension .oft sont des fichiers modèles créés à l'aide de Microsoft Outlook. L'ensemble de mise en page pré-formaté pour les modèles de message est ensuite utilisé pour envoyer des e-mails avec des informations communes afin de gagner du temps. Ces fichiers peuvent être générés en créant un nouvel e-mail, en ajoutant les informations nécessaires, puis en utilisant la liste déroulante Enregistrer en tant que modèle Office (.oft) de Microsoft Outlook. Les utilisateurs peuvent ouvrir les fichiers OFT en double-cliquant dessus et il s'ouvrira dans l'application associée sur ce système particulier.

## Structure du fichier OFT ##

Le format de fichier .OFT utilise le format de fichier [MSG](/fr/email/msg/) à sa base. La seule différence est que les fichiers OFT ont CLSID_TemplateMessage ({0006F046-0000-0000-C000-000000000046}) comme classe de stockage (WriteClassStg), tandis que les fichiers MSG utilisent CLSID_MailMessage ({00020D0B-0000-0000-C000-000000000046}).

Le format CFB_3 est la base du fichier MSG. Le paradigme est basé sur les concepts de stockages et de flux, assez proches des répertoires et des fichiers. Par conséquent, une différence majeure dans le premier est la hiérarchie entière, regroupée dans un fichier distinct, appelé fichier composé. Les objets constituent les fichiers de messages et se composent d'une seule propriété ou de ses collections. Cette capacité permet aux applications de stocker des données complexes et structurées dans un seul fichier. Ce format spécifie également plusieurs stockages, chaque stockage représentant l'objet Message en tant que composant principal. Ces stockages contiennent un certain nombre de flux représentant une propriété de ce composant. L'imbrication des rangements est également possible.

### Propriétés OFT

Au niveau supérieur du fichier .msg, les stockages contiennent des flux qui y stockent des propriétés. Les propriétés peuvent être classées comme suit :

* Propriétés de longueur fixe
* Propriétés de longueur variable
* Propriétés à valeurs multiples

Indépendamment de la catégorie, une propriété est soit étiquetée, soit nommée. Cependant, des informations de mappage appropriées sont requises pour les propriétés nommées, comme spécifié par leur stockage de mappage.

### Stockages OFT

Les stockages constituent les composants clés de l'objet Message. Le format de fichier MSG indique les stockages suivants :

### Structure de niveau supérieur

L'objet Message représente tout le niveau supérieur du format de fichier Msg. Selon le type, les propriétés, le nombre d'objets destinataire et pièce jointe, un objet message peut avoir différents stockages de flux dans son fichier .MSG correspondant.

#### Relation avec d'autres structures

Le format de fichier MSG/OFT a les relations suivantes avec d'autres structures :

* La base de .msg est le format de fichier binaire composé.
* Les propriétés utilisées par Message and Attachment Object Protocol sont utilisées par ce format.

## Références

* [[MS-OXMSG] : format de fichier Outlook MSG](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

