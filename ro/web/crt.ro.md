{
  "date" : "2019-10-11",
  "keywords" :[ "crt","fișier crt", "format fișier crt", "tip fișier crt", "fișier", "tip", "ce este un fișier crt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - Format de fișier certificat de securitate",
  "description":"Aflați despre formatul de fișier CRT și despre API-urile care pot crea și deschide fișiere CRT.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier CRT?

Un fișier cu extensia .crt este un fișier certificat de securitate care este utilizat de site-urile web securizate pentru a stabili conexiuni securizate de la serverul web la un browser. Site-urile web securizate fac posibilă securizarea transferurilor de date, autentificărilor, tranzacțiilor cu cardul de plată și oferă navigare protejată pe site. Dacă deschideți un site web securizat, veți vedea o pictogramă „lacăt” în bara de adrese. Dacă faceți clic pe el, puteți vizualiza detaliile certificatului instalat. Companii internaționale precum Verisign și Thawte distribuie aceste certificate SSL.

## Format de fișier CRT

Fișierele CRT sunt în format ASCII și pot fi deschise în orice editor de text pentru a vizualiza conținutul fișierului certificat. Urmează standardul de certificare X.509 care definește structura certificatului. Acesta definește câmpurile de date care ar trebui incluse în certificatul SSL. CRT aparține formatului PEM al certificatelor care sunt fișiere codificate ASCII Base64.

### Structura fișierului PEM

Un fișier PEM poate avea mai multe certificate. Într-un astfel de caz, fiecare certificat din fișierul PEM urmează următoarea structură.

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

### Exemplu de format de fișier CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referințe ##

* [Chei publice, chei private și certificate](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

