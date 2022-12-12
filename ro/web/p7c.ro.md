{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - Fișier de certificat PKCS 7",
  "description":"Aflați despre formatul de fișier P7C și despre API-urile care pot crea și deschide fișiere P7C.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier P7C?

Un fișier P7C, ca și alte fișiere cu certificat de securitate, este un certificat digital care este folosit pentru a autentifica identitatea în rețea. Aplicațiile care utilizează certificate autentifică identitatea folosind cheia publică inclusă în aceste fișiere de certificat. Criptografia cu cheie publică, sau criptografia asimetrică, utilizează perechi de chei dintre care una este cheia publică, iar cealaltă este cunoscută ca cheie privată. Cheia privată este păstrată în siguranță pentru o securitate eficientă, în timp ce cheia publică poate fi partajată altora. Alte formate comune de fișiere de certificat includ [CRT](/ro/web/crt/), DER și PEM.

## Format de fișier P7C - Mai multe informații

Fișierele P7C sunt salvate pe disc ca fișiere binare și includ informațiile cheii publice generate folosind algoritmi criptografici bazați pe probleme matematice. Acestea pot fi deschise în orice editor de text, dar conținutul lor nu este într-o formă care poate fi citită de om. Unele dintre aplicațiile care pot deschide fișiere P7C includ Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager și Microsoft Windows Contacts.

### Exemplu de format de fișier P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referințe ##

* [Public Key Criptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Cum se creează fișierul P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

