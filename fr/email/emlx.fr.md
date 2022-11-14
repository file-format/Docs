{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Format de fichier Apple Mail",
  "description":"En savoir plus sur le format de fichier EMLX et les API qui peuvent créer et ouvrir des fichiers EMLX.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier EMLX ?

Le format de fichier EMLX est implémenté et développé par Apple. L'application Apple Mail utilise le format de fichier EMLX pour exporter les e-mails. Il existe également d'autres applications qui peuvent ouvrir les fichiers EMLX et les convertir en d'autres formats de fichiers.

## Bref historique du format de fichier EMLX

Le système d'exploitation Mac OS X a adopté le programme de messagerie existant, NeXTMail, créé par NeXT dans le cadre du système d'exploitation NeXTSTEP. Après avoir acquis NeXT, Apple a amélioré ses fonctionnalités et est devenue l'application de messagerie Apple Mail à utiliser comme client de messagerie par défaut. Les e-mails exportés via Apple Mail sont directement enregistrés en tant que fichiers EMLX. De plus, il s'agit du client de messagerie par défaut pour les fichiers EMLX lorsque quelqu'un les ouvre en double-cliquant sur Mac OS.

## Format de fichier EMLX

Les fichiers EMLx sont de simples fichiers texte qui peuvent être ouverts dans n'importe quel éditeur de texte comme le Bloc-notes. La structure du fichier EMLX se compose de trois parties :

* Un nombre d'octets pour le message - Longueur du message lui-même, écrit en ASCII en décimal, terminé par 0x0a
* Le message lui-même
* Métadonnées de message sous forme de plist XML

Celles-ci peuvent être mieux expliquées à l'aide de l'exemple d'e-mail suivant extrait d'Apple Mail en tant qu'EMLX et ouvert dans un éditeur de texte.

### Exemple EMLX

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1] (******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

Dans cet exemple, le 875 affiche la longueur totale du message. Les métadonnées du message sont incluses dans le<plist> les balises et les drapeaux sont décrits comme suit :

|Champ|Description|Valeur
---|---|---|
|0|lire|1 << 0
|1|supprimé|1 << 1
|2|répondu|1 << 2
|3|crypté|1 << 3
|4|marqué|1 << 4
|5|récent|1 << 5
|6|brouillon|1 << 6
|7|initial (n'est plus utilisé)|1 << 7
|8|transféré|1 << 8
|9|redirigé|1 << 9
|10-15|nombre de pièces jointes|3F << 10 (6 bits)
|16-22|niveau de priorité|7F << 16 (7 bits)
|23|signé|1 << 23
|24|est indésirable|1 << 24
|25|n'est pas indésirable|1 << 25
|26-28|taille de police delta|7 << 26 (3 bits)
|29|niveau de courrier indésirable enregistré|1 << 29
|30|texte en surbrillance dans toc|1 << 30
|31|(inutilisé)|

## Voir également ##

* [EML](/fr/email/eml/)
* [MSG](/fr/email/msg/)

