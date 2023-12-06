{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH File - iPhone/iPod Touch SHSH Blob File Format",
  "description":"Aflați despre ce este un fișier SHSH.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Ce este un fișier SHSH?

Un fișier SHSH, cunoscut și sub numele de Signature HaSH, este o semnătură digitală utilizată de Apple pentru a autentifica și verifica actualizările de firmware pentru dispozitive iOS, cum ar fi iPhone-uri, iPad-uri și iPod-uri.

## Diferența dintre formatele de fișiere SHSH și SHSH2

Asemenea unui fișier SHSH2, fișierul SHSH conține un identificator unic pentru dispozitiv numit "ECID" (Exclusive Chip ID), precum și informații despre versiunea de firmware instalată pe dispozitiv. Cu toate acestea, fișierele SHSH au fost folosite în versiuni mai vechi de iOS (înainte de iOS 10) și de atunci au fost înlocuite cu fișiere SHSH2.

## Format de fișier SHSH - Mai multe informații

Fișierele SHSH sunt salvate pe disc în format de fișier binar. Detaliile interne ale structurii fișierelor din acest format de fișier nu sunt disponibile public.

Fișierele SHSH sunt importante pentru utilizatorii care doresc să downgrade firmware-ul dispozitivului lor la o versiune anterioară care nu mai este semnată de Apple. Prin salvarea fișierelor SHSH pentru o anumită versiune de firmware atunci când aceasta este încă semnată de Apple, utilizatorii le pot folosi ulterior pentru a ocoli verificarea semnăturii Apple și pentru a instala acea versiune de firmware pe dispozitivul lor. Acest proces este cunoscut și sub denumirea de "jailbreaking".

## Referințe

* [SHSH Blob - După Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Saver](https://tsssaver.1conan.com/v2/)

