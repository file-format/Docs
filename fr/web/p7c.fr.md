{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - Fichier de certificat PKCS 7",
  "description":"En savoir plus sur le format de fichier P7C et les API qui peuvent créer et ouvrir des fichiers P7C.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier P7C ?

Un fichier P7C, comme les autres fichiers de certificat de sécurité, est un certificat numérique utilisé pour authentifier l'identité sur le réseau. Les applications utilisant des certificats authentifient l'identité à l'aide de la clé publique incluse dans ces fichiers de certificat. La cryptographie à clé publique, ou cryptographie asymétrique, utilise une paire de clés dont l'une est la clé publique et l'autre est dite clé privée. La clé privée est conservée en lieu sûr pour une sécurité efficace, tandis que la clé publique peut être partagée avec d'autres. Les autres formats de fichier de certificat courants incluent [CRT](/fr/web/crt/), DER et PEM.

## Format de fichier P7C - Plus d'informations

Les fichiers P7C sont enregistrés sur le disque en tant que fichiers binaires et incluent les informations de clé publique générées à l'aide d'algorithmes cryptographiques basés sur des problèmes mathématiques. Ceux-ci peuvent être ouverts dans n'importe quel éditeur de texte, mais leur contenu n'est pas sous une forme lisible par l'homme. Certaines des applications pouvant ouvrir les fichiers P7C incluent Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager et Microsoft Windows Contacts.

### Exemple de format de fichier P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Références ##

* [Cryptage à clé publique] (https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Comment créer un fichier P7C ?] (https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

