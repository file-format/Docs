{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier ADM - Format de fișier șablon administrativ",
  "description":"Aflați despre formatul fișierului ADM și despre cum să deschideți fișierele ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Ce este un fișier ADM?

Un fișier ADM este un fișier șablon utilizat de software-ul Politici de grup Microsoft pentru a specifica locația setărilor de politică bazate pe registry în fișierul de registru. Este folosit de administratorii de sistem pentru a defini politica de gestionare a unui grup de computere care fac parte din grup. Aceste informații devin parte din obiectele de politică de grup (GPO) care sunt create pentru gestionarea grupului.

Puteți deschide fișiere ADM utilizând Microsoft Group Policy Object Editor.

## Format de fișier ADM - Mai multe informații

Fișierele ADM sunt stocate ca fișiere text în format unicode. Acestea au fost utilizate în principal pentru a descrie locația setărilor de politică bazate pe registry în registry Windows Vista și Windows 7.

Fișierele ADM nu mai sunt acceptate și au fost înlocuite cu fișierele [ADMX](/ro/system/admx/). GPA ignoră următoarele fișiere ADM implicite pe computerele care rulează Microsoft Windows Vista Service Pack 1 sau o versiune ulterioară.

* sistem.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## Referințe

* [Fișiere șabloane administrative - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Gestionarea fișierelor șabloane administrative](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

