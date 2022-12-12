{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul fișierului KEY și despre API-urile care pot crea și deschide fișiere KEY.",
  "title" :"Format fișier cheie - Fișier cu cheie privată de e-mail cu confidențialitate îmbunătățită",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Ce este un fișier KEY?

Un fișier KEY este partea privată a unui mecanism de securitate care este salvat pe disc în format de fișier Privacy-Enhanced Mal (PEM). Este folosit pentru a decripta informațiile schimbate între un browser web și serverul web care servește cererile de navigare. Un fișier KEY conține șiruri codificate care sunt inutile pentru ochiul uman, dar reprezintă esența schimbului de informații de criptare/decriptare ca parte a certificatului SSL pe serverele web. Fișierele KEY sunt generate automat și sunt instalate la sfârșitul clientului.

Puteți deschide fișiere **KEY** cu orice editor de text, cum ar fi Microsoft Notepad (Windows), Apple TextEdit (Mac) sau GitHub Atom (multplatform). Fișierele KEY sunt similare cu formatele de fișiere [CRT](/ro/web/crt/) și [CER](/ro/web/cer/).

## Format de fișier CHEIE - Mai multe informații

Fișierele KEY sunt stocate pe disc ca fișiere text simplu, dar sunt șiruri codificate care nu sunt ușor de citit pentru oameni. Practic, utilizatorii nu înțeleg șirurile atunci când sunt deschise într-un editor de text. Certificatul cheii private este confidențial și nu trebuie partajat nimănui. Procesul complet de securizare a schimbului de informații prin internet implică:

* **Cheie publică** - folosită pentru a cripta informațiile utilizatorului pentru schimbul de date între browser și serverele web
* **Cheie privată** - folosită pentru a decripta informațiile pe măsură ce sunt primite de serverul web

Certificatele SSL, cunoscute și ca certificate X.509, sunt unice pentru fiecare site web. Fișierele KEY utilizând următoarea sintaxă:

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

### Exemplu de fișier KEY

Următorul este un exemplu de fișier cheie privată.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referințe

* [Chei publice, chei private și certificate](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

