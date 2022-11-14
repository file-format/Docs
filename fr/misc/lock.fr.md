{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier LOCK - Qu'est-ce qu'un fichier Lock ?",
  "description":"En savoir plus sur le format de fichier LOCK et son .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Qu'est-ce qu'un fichier LOCK ?

Un fichier **LOCK** est un fichier renommé utilisé par les applications et les systèmes d'exploitation pour marquer un fichier ou un périphérique comme verrouillé. Cela indique aux autres applications de ne pas utiliser le fichier à moins qu'il ne soit indépendant de l'application qui l'utilise. Dans la plupart des cas, ces fichiers de verrouillage sont vides, mais dans d'autres cas, ils peuvent contenir des informations relatives au verrouillage telles que les propriétés et les paramètres.

Parfois, le fichier .lock est utilisé par le .NET Framework de Microsoft pour créer des copies ** verrouillées ** d'un fichier de base de données. Dans un tel cas, une copie du fichier de base de données s'ouvrira avec l'extension .lock. Cela ne permet pas à l'utilisateur d'apporter des modifications au fichier pendant qu'il est utilisé par un autre utilisateur.

## Format de fichier LOCK - Plus d'informations

Un fichier LOCK est créé par chaque application et son format de fichier est spécifique à l'application. Ces fichiers de verrouillage peuvent être enregistrés à la fois au format texte et au format de fichier binaire.

La présence de fichiers de verrouillage empêche l'accès simultané d'une ressource à plusieurs fichiers tentant d'accéder à cette ressource. Une copie du fichier d'origine est créée avec l'extension .lock suffixée à son nom. Cela indique aux autres applications d'avoir un accès en lecture seule au fichier. Par exemple, resource.dat deviendra resource.data.lock.

Pour le langage de programmation Ruby, vous pouvez rencontrer le fichier **gemfile.lock**. C'est là que Bundler enregistre les versions exactes qui ont été installées. Ainsi, lorsqu'un projet/une bibliothèque est déplacé vers une autre machine, l'exécution du bundle recherchera dans le Gemfile la version exacte appropriée.

## Verrouiller le fichier sous Linux

Linux prend en charge deux types de verrous de fichiers : les verrous consultatifs et les verrous obligatoires.

* **Verrouillage consultatif** : type de verrouillage qui n'est pas appliqué. Dans ce cas, les processus participants coopèrent les uns avec les autres en acquérant explicitement des verrous. Si cela n'est pas possible, les verrous consultatifs sont ignorés.

* **Verrous obligatoires** : en cas de verrouillage obligatoire, le système d'exploitation applique le verrouillage du fichier en empêchant les autres processus de lire ou d'écrire le fichier. Cela ne nécessite aucune coopération entre les processus.

le verrouillage obligatoire ne nécessite aucune coopération entre les processus participants. Une fois qu'un verrou obligatoire est activé sur un fichier, le système d'exploitation empêche les autres processus de lire ou d'écrire le fichier.

## Références

* [GemFile et Gemfile.lock dans Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Verrouillage sous Linux](https://www.baeldung.com/linux/file-locking#:~:text=File%20locking%20is%20a%20mechanism,very%20dangerous%20command%20in%20Linux.)

