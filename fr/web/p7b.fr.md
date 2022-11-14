{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - Fichier de certificat PKCS 7",
  "description":"En savoir plus sur le format de fichier P7C et les API qui peuvent créer et ouvrir des fichiers P7C.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier P7B ?

Un fichier P7B est un fichier de certificat de sécurité qui contient un certificat numérique sécurisé pour authentifier une personne ou un appareil. Semblable à un fichier de certificat [.cer](/fr/web/cer/), un fichier P7B peut être installé à l'aide de l'option "Installer le certificat" en utilisant l'option de clic droit sur le fichier. P7B utilise une option de formatage différente de celle du format de fichier CER. Il contient un ou plusieurs fichiers de certificat numérique X.509 qui utilisent le codage base64 (ASCII). Les fichiers P7B sont reçus sous forme de fichier [ZIP](/fr/compression/zip/) ou reçus de l'autorité de certification.

## Format de fichier P7B

Les fichiers P7B sont stockés sous forme de fichiers ASCII simples pouvant être ouverts dans n'importe quel éditeur de texte. Il contient la clé publique qui est une chaîne codée qui n'a pas de sens du point de vue de la lisibilité.

### Exemple de format de fichier P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Références ##

* [Cryptage à clé publique] (https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Comment créer un fichier P7C ?] (https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

