{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier P7S - Message électronique signé numériquement",
  "description":"En savoir plus sur le format de fichier P7S et les API qui peuvent créer et ouvrir des fichiers P7S.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## Qu'est-ce qu'un fichier P7S ?

Un fichier P7S est une signature numérique reçue avec un e-mail signé numériquement. La présence de ce fichier en pièce jointe avec l'e-mail vérifie que l'e-mail est envoyé à partir d'une source authentique. Cela garantit que l'expéditeur dispose d'un certificat de signature d'e-mail installé sur son ordinateur. Lorsqu'un tel e-mail signé est envoyé à partir de l'ordinateur de l'utilisateur, le fichier P7S y est joint et contient le nom de l'expéditeur. Les clients de messagerie prenant en charge les e-mails signés peuvent voir les informations de l'expéditeur.

## Format de fichier P7S - Plus d'informations

Les fichiers P7S S/MIME (Secure/Multipurpose Internet Mail Extensions) contiennent les informations au format texte brut lisible par l'homme. Les clients de messagerie tels que Microsoft Outlook, Apple Mail et Mozilla Thunderbird prennent en charge la lecture des informations signées numériquement à partir d'un e-mail S/MIME. La signature d'un e-mail vérifie l'identité de l'expéditeur et indique au destinataire que le message est authentique. Lorsque des e-mails sont téléchargés à partir de clients de messagerie (soit [EML](/fr/email/eml/) ou [MSG](/fr/email/msg/)), ces fichiers P7S sont joints à ces e-mails.

Un fichier P7S contient les informations suivantes :

* Source d'origine de l'e-mail
* Date et heure d'envoi,
* S'il a été modifié lors de la transmission

Ces informations sont intégrées à l'aide de la technologie Public-Key Cryptography Standard #7 (PKCS7) pour joindre numériquement les signatures cryptées à l'e-mail.

## Références ##

* [Outil de signature Microsoft](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

