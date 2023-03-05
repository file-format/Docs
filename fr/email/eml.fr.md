{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - Message électronique",
  "description":"En savoir plus sur le format de fichier EML et les API qui peuvent créer et ouvrir des fichiers EML.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## Qu'est-ce qu'un fichier EML ?

Le format de fichier EML représente les messages électroniques enregistrés à l'aide d'Outlook et d'autres applications pertinentes. Presque tous les clients de messagerie prennent en charge ce format de fichier pour sa conformité avec la norme de format de message Internet RFC-822. Microsoft Outlook est le logiciel par défaut pour l'ouverture des types de messages EML. Les fichiers EML peuvent être utilisés pour l'enregistrement sur disque ainsi que pour l'envoi aux destinataires à l'aide de protocoles de communication.

## Bref historique de l'EML

Les spécifications de format de fichier EML sont disponibles conformément au format standard [RFC 822](http://www.ietf.org/rfc/rfc0822.txt). Avant la RFC-822, la RFC-733 régissait les règles d'échange de messages réseau jusqu'en 1982, la première a été créée comme une amélioration du latéral en établissant des normes ARPA. Parallèlement, Microsoft a créé ses propres modules COM pour le développement de son propre client de messagerie, à savoir Outlook Express. La RFC-822 a pris la voie pour s'établir en tant que format propriétaire lorsque Microsoft s'est écarté de la norme ouverte et a créé le format de fichier [PST](/fr/email/pst/) dans lequel les e-mails sont enregistrés dans un format de base de données hautement structuré. Cela entraînait des problèmes pour les utilisateurs de clients de messagerie autres que Microsoft lorsque des e-mails étaient transférés à partir de Microsoft Outlook.

C'était en 2001 lorsque la norme 822 a été améliorée en 2822 - Internet Message Format qui est actuellement utilisé pour créer, lire et envoyer des messages EML au format MIME RFC-822.

## Spécifications du format de fichier EML

Les fichiers EML comprennent deux sections distinctes :

* En-têtes - Contient des informations sur l'en-tête du message
* Corps du message - Contient une série d'informations pouvant inclure le contenu du message, des images intégrées et des pièces jointes

### Informations sur les en-têtes ###

Un fichier EML se compose d'informations d'en-tête et éventuellement du corps du message. Chaque ligne d'en-tête dans l'EML comporte deux parties séparées par deux points " : ". Le premier s'appelle le nom de l'en-tête et celui qui suit les deux-points est le corps de l'en-tête. Par exemple, ces en-têtes incluent :

* Adresse e-mail de l'expéditeur
* Adresse courriel du destinataire
* Objet de l'e-mail
* Horodatage du message

**Exemple d'en-tête**

De:<John@bmw.eml.light.com>

À:<Andy@fileformat.com>

Date : jeu. 8 mars 2018 10:43:37 +0100

Objet : éclairage eml bmw

### Corps du message ###

Le corps du message EML contient les informations principales de l'e-mail sous forme de texte, d'hyperliens et de pièces jointes. Le corps de l'e-mail peut contenir du texte lisible en clair, mais ce n'est pas nécessaire. Dans ce cas, le corps du message peut être vide ou contenir des données de pièces jointes encodées.

Le contenu du corps du message est décrit par son Content-Type qui permet aux applications de lecture de lire les informations dans les formats respectifs. Il représente en fait la nature et le format d'un document. La structure d'un type MIME ou d'un type de contenu est très simple ; il se compose d'un type et d'un sous-type, deux chaînes, séparées par un '/'. Aucun espace n'est autorisé. Le "type" représente la catégorie et peut être un type discret ou multipartie. Le `sous-type` est spécifique à chaque type. La liste des types, qui entrent dans la catégorie Content-Type, est longue mais certains types de contenu importants sont les suivants :


|**Type**|**Description**|**Exemple de sous-types**
---|---|---|
|text|Représente un format lisible par l'homme|text/plain, text/html, text/css, text/javascript
|image|Représente une image de tout type à l'exception des vidéos|image/bmp, image/png, image/jpg, image/gif
|audio|Représente n'importe quel format de fichier audio|audio/mdi, audio/wav
|application|Représente tout type de données binaires|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Représentation de l'attachement dans le corps EML ###

Le corps EML contient des limites pour chaque type de contenu qu'il contient. La pièce jointe dans le corps du message est identifiée par son Content-Type et Content-Disposition, comme illustré dans l'exemple suivant :

Type de contenu : texte/plain ; jeu de caractères#"windows-1252" ; nom#"apple app store.txt"
Contenu-Disposition : pièce jointe ; nom de fichier#"apple app store.txt"
Encodage de transfert de contenu : base64
ID de pièce jointe X : f_jkhztmd02

Comme on peut le voir, le Content-Disposition réglé sur pièce jointe permet aux applications de lecture d'obtenir des informations sur la pièce jointe telles que le nom du fichier joint et le codage de transfert. Les informations d'en-tête de pièce jointe sont suivies du contenu codé de la pièce jointe qui doit être lu.

#### Exemple de feuille de calcul en pièce jointe ####

Type de contenu : application/vnd.openxmlformats-officedocument.spreadsheetml.sheet ; nom#"francais_spodr.xlsx"
Contenu-Disposition : pièce jointe ; filename#"english_spodr.xlsx"
Encodage de transfert de contenu : base64
ID de pièce jointe X : f_jkhztmd43

## Références

* [RFC 822](http://www.ietf.org/rfc/rfc0822.txt)

