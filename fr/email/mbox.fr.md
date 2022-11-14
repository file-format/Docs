{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - Fichier de boîte aux lettres électronique",
  "description":"En savoir plus sur le format de fichier MBOX et les API qui peuvent créer et ouvrir des fichiers MBOX.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier MBOX ?

Le format de fichier MBox est un terme générique qui représente un conteneur pour la collecte de messages électroniques. Les messages sont stockés à l'intérieur du conteneur avec leurs pièces jointes. Les messages d'un dossier entier sont enregistrés dans un seul fichier de base de données et les nouveaux messages sont ajoutés à la fin du fichier. De nombreuses applications et API prennent en charge le format de fichier MBox tel que Apple Mail et Mozilla Thunderbird.

## Format de fichier MBOX ##

Le format de fichier MBox est resté non normalisé pendant assez longtemps jusqu'en 2005, date à laquelle l'application/mbox a été normalisée en tant que [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Messages, au format RFC 2822 , sont concaténés dans le format de fichier MBox l'un après l'autre. Chaque message commence par une ligne de séparation qui identifie l'expéditeur du message et identifie également la date et l'heure auxquelles le message a été reçu par le destinataire final (soit le système de dernier saut dans le chemin de transfert, soit le système qui sert de magasin de messagerie). Chaque message se termine généralement par une ligne vide. La fin de la base de données est généralement reconnue soit par l'absence de données supplémentaires, soit par la présence d'un marqueur de fin de fichier explicite.

## Lecture d'un message à partir d'un fichier MBox ##

Un lecteur parcourt un fichier mbox à la recherche de lignes From_. Toute ligne From_ marque le début d'un message. Le lecteur ne doit pas essayer de profiter du fait que chaque ligne From_ (après le début du fichier) est vide. Une fois que le lecteur a trouvé un message, il extrait un expéditeur d'enveloppe (éventuellement corrompu) et une date de livraison de la ligne From_. Il lit ensuite jusqu'à la prochaine ligne From_ ou fin de fichier, selon la première éventualité. Il supprime la dernière ligne vierge et supprime les guillemets des lignes >From_ et >>From_ lines et ainsi de suite. Le résultat est un message RFC 822.

## Considérations sur l'encodage ##

Le contenu d'un fichier MBox peut se confondre de manière irréversible lorsqu'un e-mail reçu contient un fichier Mbox en pièce jointe et est enregistré dans un autre fichier Mbox. Pour éviter cela, les systèmes de messagerie doivent coder une base de données mbox avec un codage de transfert non transparent (tel que BASE64 ou Quoted-Printable) chaque fois qu'un tel objet est transféré via des protocoles de messagerie. Les responsables de la mise en œuvre doivent également être prêts à coder les données mbox localement si des données non conformes sont reçues.

## Références ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - Wikipédia](https://en.wikipedia.org/wiki/Mbox)

