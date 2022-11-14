{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier PEM - Format de fichier de certificat de messagerie amélioré pour la confidentialité",
  "description":"En savoir plus sur le format de fichier PEM et les API qui peuvent créer et ouvrir des fichiers PEM.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Qu'est-ce qu'un fichier PEM ?

Un fichier PEM est un fichier de certificat de sécurité utilisé pour établir un canal de communication sécurisé entre un serveur Web et un navigateur. Il est encodé en Base64 et peut contenir une clé privée, un certificat de serveur et/ou une combinaison d'autres certificats. Les fichiers PEM sont similaires aux fichiers de certificat .der en termes d'utilisation, mais sont stockés sous forme de texte encodé en Base64 plutôt que de données binaires. D'autres formats de fichier de certificat similaires incluent les fichiers [.cer](/fr/web/cer/) et [.crt](/fr/web/crt/).

Les applications qui peuvent ** ouvrir les fichiers PEM ** incluent les éditeurs de texte tels que Microsoft Notepad et Apple TextEdit.

## Format de fichier PEM

PEM est un format de fichier conteneur qui définit la structure et le type de codage du fichier utilisé pour stocker les données. Les fichiers PEM sont stockés sur le disque sous un format de fichier encodé en Base64 qui n'est pas lisible par l'homme. La norme définit qu'un fichier PEM commence par :

```
-----BEGIN <type>-----
```
et se termine par :
```
-----END <type>-----
```

Tous les autres contenus à l'intérieur de ceux-ci sont encodés en base64 (lettres majuscules et minuscules, chiffres, + et /). Un seul fichier PEM peut comprendre plusieurs blocs qui peuvent être utilisés par d'autres programmes. Si un fichier PEM contient plusieurs certificats, chaque certificat est séparé par des blocs individuels comme suit :

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### Exemple de fichier PEM

Un fichier PEM avec le bloc CERTIFICATE ressemble généralement à ceci :

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Un fichier PEM avec RSA commence comme suit.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Références ##

* [Cryptage à clé publique] (https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Comment créer un fichier P7C ?] (https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

