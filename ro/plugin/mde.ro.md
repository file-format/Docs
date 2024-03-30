{
  "date" : "2023-12-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Fișier MDE - Ce este un fișier MDE și cum se deschide?",
  "description":"Aflați despre formatul de fișier MDE și despre API-urile care pot crea și deschide fișiere MDE.",
  "linktitle" : "MDE",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-ro-mde"
    }
  },
  "lastmod" : "2023-12-03"
}

Ce este un fișier MDE?

Un fișier .MDE este o versiune compilată a unei baze de date Access (.mdb sau .accdb). Când compilați o bază de date Access într-un fișier .MDE, aceasta nu mai poate fi editată folosind instrumentele standard de proiectare Access. Scopul principal al creării unui fișier .MDE este de a distribui o aplicație de bază de date fără a expune codul sursă original.

## Format de fișier MDE

Un fișier MDE este creat prin compilarea codului VBA, a formularelor, a rapoartelor și a altor obiecte. Acest lucru are ca rezultat crearea formatului de fișier binar MDE. Fișierul .MDE rezultat poate fi distribuit utilizatorilor care pot rula aplicația, dar nu pot modifica designul sau vizualiza codul original. Fișierul MDE este de fapt versiunea compilată a unui [fișier .MDA](/database/mda/). Distribuirea fișierelor .MDE poate ajuta la protejarea proprietății intelectuale, împiedicând utilizatorii să acceseze sau să modifice codul sursă. De asemenea, poate îmbunătăți performanța pe măsură ce codul este compilat și optimizat.

## Referințe

* [Specificații de acces](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
