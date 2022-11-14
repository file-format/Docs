{
  "date" : "2019-10-11",
  "keywords" :[ "crt","fichier crt", "format de fichier crt", "type de fichier crt", "fichier", "type", "qu'est-ce qu'un fichier crt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - Format de fichier de certificat de sécurité",
  "description":"En savoir plus sur le format de fichier CRT et les API qui peuvent créer et ouvrir des fichiers CRT.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier CRT ?

Un fichier avec l'extension .crt est un fichier de certificat de sécurité utilisé par les sites Web sécurisés pour établir des connexions sécurisées du serveur Web à un navigateur. Les sites sécurisés permettent de sécuriser les transferts de données, les connexions, les transactions par carte de paiement, et offrent une navigation sécurisée sur le site. Si vous ouvrez un site Web sécurisé, vous voyez une icône "cadenas" dans la barre d'adresse. Si vous cliquez dessus, vous pouvez voir les détails du certificat installé. Des sociétés internationales telles que Verisign et Thawte distribuent ces certificats SSL.

## Format de fichier CRT

Les fichiers CRT sont au format ASCII et peuvent être ouverts dans n'importe quel éditeur de texte pour afficher le contenu du fichier de certificat. Il suit la norme de certification X.509 qui définit la structure du certificat. Il définit les champs de données qui doivent être inclus dans le certificat SSL. CRT appartient au format PEM des certificats qui sont des fichiers codés Base64 ASCII.

### Structure du fichier PEM

Un fichier PEM peut avoir plusieurs certificats. Dans un tel cas, chaque certificat du fichier PEM suit la structure suivante.

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

### Exemple de format de fichier CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Références ##

* [Clés publiques, clés privées et certificats](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

