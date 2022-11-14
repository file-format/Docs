{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier KEY et les API qui peuvent créer et ouvrir des fichiers KEY.",
  "title" :"Format de fichier KEY - Fichier de clé privée de messagerie à confidentialité améliorée",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Qu'est-ce qu'un fichier KEY ?

Un fichier KEY est la partie privée d'un mécanisme de sécurité qui est enregistré sur un disque au format de fichier PEM (Privacy-Enhanced Mal). Il est utilisé pour déchiffrer les informations échangées entre un navigateur Web et le serveur Web qui sert les requêtes de navigation. Un fichier KEY contient des chaînes codées qui sont inutiles pour l'œil humain mais qui sont l'essence même du cryptage/décryptage de l'échange d'informations dans le cadre du certificat SSL sur les serveurs Web. Les fichiers KEY sont automatiquement générés et installés côté client.

Vous pouvez ouvrir les fichiers **KEY** avec n'importe quel éditeur de texte tel que Microsoft Notepad (Windows), Apple TextEdit (Mac) ou GitHub Atom (multiplateforme). Les fichiers KEY sont similaires aux formats de fichier [CRT](/fr/web/crt/) et [CER](/fr/web/cer/).

## Format de fichier KEY - Plus d'informations

Les fichiers KEY sont stockés sur le disque sous forme de fichiers texte brut, mais sont des chaînes codées qui ne sont pas faciles à lire. Pratiquement, les utilisateurs n'ont aucune compréhension des chaînes lorsqu'elles sont ouvertes dans un éditeur de texte. Le certificat de clé privée est confidentiel et ne doit être partagé avec personne. Le processus complet de sécurisation des échanges d'informations sur Internet implique :

* **Clé publique** - utilisée pour crypter les informations de l'utilisateur pour l'échange de données entre le navigateur et les serveurs Web
* **Clé privée** - utilisée pour déchiffrer les informations telles qu'elles sont reçues par le serveur Web

Les certificats SSL, également appelés certificats X.509, sont uniques pour chaque site Web. Fichiers KEY utilisant la syntaxe suivante :

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### Exemple de fichier KEY

Voici un exemple de fichier de clé privée.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Références

* [Clés publiques, clés privées et certificats](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

