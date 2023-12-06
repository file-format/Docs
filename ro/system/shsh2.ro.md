{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH2 File - iOS SHSH Blob File Format",
  "description":"Aflați despre ce este un fișier SHSH2.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Ce este un fișier SHSH2?

Un fișier SHSH2, cunoscut și sub numele de blob SHSH sau ECID SHSH, este o semnătură digitală utilizată de Apple pentru a autentifica și verifica actualizările de firmware pentru dispozitive iOS, cum ar fi iPhone-uri, iPad-uri și iPod-uri. Conține un identificator unic pentru dispozitiv, care este cunoscut sub numele de ECID (Exclusive Chip ID). De asemenea, conține informații despre versiunea de firmware instalată pe dispozitiv.

## Format de fișier SHSH2 - Mai multe informații

Fișierele SHSH2 sunt salvate pe disc în format de fișier binar, iar detaliile interne ale structurii fișierelor din acest format de fișier nu sunt disponibile public.

Când o nouă versiune de iOS este instalată pe un dispozitiv Apple, cum ar fi iPhone, iPad sau Mac, este generat un fișier SHSH2. Acest fișier SHSH2 este trimis către serverele Apple care citesc și verifică acest fișier de semnătură digitală. Pe baza acestor informații, serverul permite sau împiedică instalarea.

Același lucru se întâmplă atunci când se solicită o actualizare. Când un utilizator solicită o actualizare sau restaurare a dispozitivului său prin iTunes sau alt software, serverele Apple vor verifica dacă fișierul SHSH2 se potrivește cu ECID și versiunea de firmware a dispozitivului înainte de a permite actualizarea să continue.

## Referințe

* [SHSH Blob - După Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Saver](https://tsssaver.1conan.com/v2/)

