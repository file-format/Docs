{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Format de messagerie Microsoft Outlook",
  "description":"En savoir plus sur le format de fichier MSG et les API qui peuvent créer et ouvrir des fichiers MSG.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier MSG ?

MSG est un format de fichier utilisé par [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) et Exchange pour stocker les messages électroniques , contact, rendez-vous ou autres tâches. Ces messages peuvent contenir un ou plusieurs champs d'e-mail, avec l'expéditeur, le destinataire, l'objet, la date et le corps du message, ou les informations de contact, les détails du rendez-vous et une ou plusieurs spécifications de tâche. Les propriétés qui constituent l'objet Message, y compris font également partie du fichier MSG. Le fichier MSG contient des en-têtes, le corps du message principal et des hyperliens sous forme de texte ASCII brut. Les fichiers MSG conviennent également aux programmes qui nécessitent l'interface de programmation d'applications de messagerie (MAPI) de Microsoft.

## Structure du fichier MSG

Le format CFB_3 est la base du fichier MSG. Le paradigme est basé sur les concepts de stockages et de flux, assez proches des répertoires et des fichiers. Par conséquent, une différence majeure dans le premier est la hiérarchie entière, regroupée dans un fichier distinct, appelé fichier composé. Les objets constituent les fichiers de messages et se composent d'une seule propriété ou de ses collections. Cette capacité permet aux applications de stocker des données complexes et structurées dans un seul fichier. Ce format spécifie également plusieurs stockages, chaque stockage représentant l'objet Message en tant que composant principal. Ces stockages contiennent un certain nombre de flux représentant une propriété de ce composant. L'imbrication des rangements est également possible.

## Propriétés Mapi

Au niveau supérieur du fichier .msg, les stockages contiennent des flux qui y stockent des propriétés. Les propriétés peuvent être classées comme suit :

* Propriétés de longueur fixe
* Propriétés de longueur variable
* Propriétés à valeurs multiples

Indépendamment de la catégorie, une propriété est soit étiquetée, soit nommée. Cependant, des informations de mappage appropriées sont requises pour les propriétés nommées, comme spécifié par leur stockage de mappage.

## Stockages

Les stockages constituent les composants clés de l'objet Message. Le format de fichier MSG indique les stockages suivants :

## Structure de niveau supérieur

L'objet Message représente l'intégralité du niveau supérieur du format de fichier MSG. Selon le type, les propriétés, le nombre d'objets destinataire et pièce jointe, un objet message peut avoir différents stockages de flux dans son fichier .MSG correspondant.

### Relation avec d'autres structures

Le format de fichier Msg a les relations suivantes avec d'autres structures :

* La base de .msg est le format de fichier binaire composé.
* Les propriétés utilisées par Message and Attachment Object Protocol sont utilisées par ce format.

## Scénarios pour éviter les formats MSG

L'objet message peut être partagé entre les clients ou les magasins de messages qui utilisent le système de fichiers .msg. Il existe peu de circonstances dans lesquelles le stockage d'un objet Message au format de fichier .msg ne serait pas approprié. Par exemple:

* En cas de maintien d'une grande archive autonome, il est préférable d'utiliser un format complet dans lequel les vues peuvent être rendues plus précisément.
* Si le destinataire est inconnu, il est possible que le format ne soit pas pris en charge par le destinataire et que des informations privées ou non pertinentes soient transmises.

## Exemple de fichier MSG

Pour avoir une idée de l'apparence d'un fichier MSG, vous pouvez télécharger un [exemple de fichier MSG](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) et l'ouvrir sur votre ordinateur pour voir son contenu.

## Références

* [[MS-OXMSG] : format de fichier Outlook MSG](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

