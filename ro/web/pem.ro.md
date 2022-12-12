{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier PEM - Format de fișier certificat de e-mail îmbunătățit pentru confidențialitate",
  "description":"Aflați despre formatul de fișier PEM și despre API-urile care pot crea și deschide fișiere PEM.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Ce este un fișier PEM?

Un fișier PEM este un fișier de certificat de securitate care este utilizat pentru a stabili un canal de comunicare securizat între un server web și un browser. Este codificat în Base64 și poate conține o cheie privată, un certificat de server și/sau o combinație de alte certificate. Fișierele PEM sunt similare cu fișierele de certificat .der în ceea ce privește utilizarea, dar sunt stocate ca text codificat în Base64, mai degrabă decât date binare. Alte formate similare de fișiere de certificat includ fișierele [.cer](/ro/web/cer/) și [.crt](/ro/web/crt/).

Aplicațiile care pot **deschide fișierele PEM** includ editori de text, cum ar fi Microsoft Notepad și Apple TextEdit.

## Format de fișier PEM

PEM este un format de fișier container care definește structura și tipul de codificare a fișierului utilizat pentru stocarea datelor. Fișierele PEM sunt stocate pe disc ca format de fișier codificat în Base64, care nu poate fi citit de om. Standardul definește că un fișier PEM începe cu:

```
-----BEGIN <type>-----
```
si se termina cu:
```
-----END <type>-----
```

Toate celelalte conținuturi din acestea sunt codificate în bază64 (litere mari și mici, cifre, + și /). Un singur fișier PEM poate cuprinde mai multe blocuri care pot fi utilizate de alte programe. Dacă un fișier PEM conține mai multe certificate, fiecare certificat este separat prin blocuri individuale, după cum urmează:

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

### Exemplu de fișier PEM

Un fișier PEM cu bloc CERTIFICAT arată de obicei astfel:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Un fișier PEM cu RSA începe așa cum urmează.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Referințe ##

* [Public Key Criptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Cum se creează fișierul P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

