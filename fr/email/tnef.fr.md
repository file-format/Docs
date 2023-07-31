{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"En savoir plus sur le format de fichier TNEF et les API qui peuvent créer et ouvrir des fichiers TNEF.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier TNEF ?

Transport Neutral Encapsulation Format (TNEF) est une propriété exclusive de Microsoft, pour l'encapsulation des pièces jointes aux e-mails sur la base de l'interface de programmation d'application de messagerie (**MAPI**). Microsoft Outlook et Microsoft Exchange Server prennent entièrement en charge TNEF, tandis que plus tard décode TNEF en MAPI et affiche les e-mails formatés. Une pièce jointe à un e-mail avec un codage TNEF a un type MIME de MS-TNEF et est stockée sous winmail/win.dat. La pièce jointe dans winmail .dat contient les informations suivantes :


|Message|Objets OLE|Fonctionnalités d'Outlook
---|---|---|
|<ul><li> Pièces jointes aux messages d'origine</li><li> Version originale formatée</li><li> polices, tailles de texte et couleurs de texte</li></ul> |<ul><li> images intégrées</li><li> documents Office intégrés</li></ul> |<ul><li> formulaires personnalisés</li><li> boutons de vote</li><li> demandes de rendez-vous</li></ul>


D'autres services de messagerie qui ne prennent pas en charge TNEF présentent du texte brut pour les messages au format TNEF. Outlook intègre un format riche du message dans des fichiers TNEF (OLE) ou des fonctionnalités Outlook particulières (formulaires, boutons d'interrogation et demandes de conférence). Il n'est pas possible de sanctionner l'encodage TNEF explicite dans le client de messagerie Outlook, mais opter pour le format RTF pour l'envoi d'un e-mail facilite implicitement l'encodage TNEF.

## Format de fichier TNEF

L'algorithme de données TNEF établit une structure aplatie à partir de propriétés de messages hiérarchiques riches. Ces structures aplaties servent ensuite à représenter un flux de données en série composé de propriétés particulières.

Dans certaines situations, où les propriétés se produisent dans des groupes ou ont plusieurs valeurs, le flux peut inclure des décomptes et des remplissages pour appliquer des alignements de données spécifiques. Une situation particulière où l'utilisation de cet algorithme est avantageuse est dans un environnement de messagerie non compatible. Dans de tels environnements, une propriété de message riche est codée dans un flux de données série par un enregistreur TNEF. De plus, les propriétés qui n'appartiennent pas au TNEF sous-jacent peuvent être encapsulées pendant la transmission. Ces propriétés encapsulées sont ensuite rendues disponibles par décodage via un TNEF pour garantir la disponibilité de toutes les propriétés du message d'origine à l'application cliente.

Dans TNEF, tous les types de données numériques sont little-endian et leur taille est supérieure à un octet. La manipulation de ces valeurs numériques sur des plates-formes non little-endian nécessite d'effectuer les transformations appropriées pour obtenir des valeurs correctes. Les valeurs de chaîne sont représentées au format ABNF (Augmented Backus-Naur Form) conformément aux spécifications [RFC5234]. Lorsque la chaîne se termine par un caractère nul, elle est également incluse ; par exemple, "worker@specimen.com" %x00.

{{< figure src="../TNEF.png" alt="Format de fichier TNEF" >}}

## Attributs TNEF et règles de traitement ##

Le flux de données dans TNEF commence par un numéro de version hérité, une signature, une valeur de clé primitive et un attribut représentant la page de codes. Cette page de codes est générée lorsque l'encodeur enregistre les attributs et les propriétés ANSI. Après cela, le flux est devenu une série d'attributs dans lesquels les attributs de message étaient alignés en premier, puis suivis des attributs de pièce jointe. Différentes caractéristiques de message et de pièce jointe sont contenues dans des attributs spéciaux tels que attMsgProps, attAttachment et attRecipTable. Les attributs qui apparaissent dans le flux TNEF contiennent la structure, les propriétés de message et les conversions nécessaires pour les engager avec les propriétés de message. Chaque attribut se compose d'un identifiant, de la taille et des données de l'attribut, d'une somme de contrôle et d'un niveau en fonction de son application.

## Relation avec les protocoles et autres algorithmes ##

Les systèmes qui ont un mécanisme médiocre pour afficher un format de message riche ont nativement besoin de l'algorithme de données TNEF pour le transport. En utilisant le type de média ms-TNEF, la sortie de l'algorithme se compose d'un fichier joint (winmail.dat) et d'une partie de corps de MIME spécifié dans [RFC2045]. Le corps du message en texte brut est transmis à l'aide de UUENCODE conformément à la spécification [MSDN-UAF] et ce corps de message ou une méthode équivalente est décodé à l'extrémité destinataire. De plus, TNEF peut transmettre des données de message en utilisant différents protocoles Internet comme SMTP, POP3, IMAP4, et ceux qui intègrent MIME selon la norme RFC2045.

## Déclaration d'applicabilité ##

En plus de la simple transmission de messages, l'application originale de TNEF devait être créée pour utiliser des classes de messages et prendre en charge des fonctionnalités supplémentaires qui n'ont pas de prise en charge d'origine dans le protocole de transport. Cette application a été affinée pour la transmission de propriétés de message riches et de propriétés nommées que les clients de messagerie modernes utilisent de nos jours. Pour la conformité avec l'implémentation d'origine, la syntaxe d'attribut d'origine est conservée et un attribut spécial contient les nouvelles propriétés de message séparément.

## Références

* [Format d'encapsulation neutre pour le transport](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Adresses e-mail et carnets d'adresses dans Exchange Server](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# serveur d'échange-2019)
* [[MS-OXTNEF] : algorithme de données au format d'encapsulation neutre de transport (TNEF)](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

