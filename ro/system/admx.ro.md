{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier ADMX - Format de fișier șablon administrativ al politicii de grup",
  "description":"Aflați despre formatul fișierului ADMX și despre cum să deschideți fișierele ADMX.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Ce este un fișier ADMX?

Un fișier ADMX este un fișier de configurare a politicii utilizat de software-ul Microsoft Windows Group Policy care gestionează un grup de computere dintr-un grup. Este un fișier șablon administrativ bazat pe XML și a fost introdus cu Windows Vista Service Pack 1. Fișierele ADMX conțin setări de configurare pentru conturile de utilizator, configurațiile sistemului de operare și aplicațiile. Fișierele ADMX sunt folosite pentru a stoca și implementa configurațiile pentru gestionarea centralizată a multor sisteme informatice.

Puteți crea sau edita fișiere ADMX utilizând orice editor de text compatibil XML, orice editor de obiecte de politici de grup Microsoft.

## Format de fișier ADMX - Mai multe informații

Fișierele ADMX sunt stocate în formatul de fișier universal [XML](/ro/web/xml/), care poate fi citit de om. Este un format de fișier multilingv și permite administratorilor de sistem din diferite limbi să lucreze cu aceleași fișiere ADMX. Fișierele ADMX au înlocuit vechiul format de fișier [ADM](/ro/system/adm/), care este un format de fișier text în format Unicode. Fișierele ADMX specifică cheile de registry care sunt modificate atunci când o anumită setare de politică de grup este modificată.

### Ce pot face cu fișierul ADMX?

Fișierele ADMX definesc ce acțiuni trebuie permise computerelor utilizatorilor care fac parte dintr-un grup. Politica de grup impune regulile setate în combinație cu software-ul Active Directory. Fișierele ADMX sunt gestionate din magazinul central pe sistemul de operare Windows, care este o locație centrală în domeniu.

Un fișier ADMX implementat într-un mediu de lucru poate permite administratorilor să implementeze politici precum:

* Controlați utilizarea internetului
* Descărcarea anumitor tipuri de fișiere
* Utilizarea dispozitivelor amovibile pe sisteme

## Referințe

* [Fișiere șabloane administrative - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Gestionarea fișierelor șabloane administrative](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

