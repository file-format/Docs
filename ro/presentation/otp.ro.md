{
  "date" : "2021-01-21",
  "keywords" :[ "fișier otp", "format fișier otp", "ce este un fișier otp", "fișier", "exemplu otp", "extensie fișier otp", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTP – șablon de prezentare OpenDocument",
  "description":"Aflați despre formatul de fișier OTP și despre API-urile care pot crea și deschide fișiere OTP.",
  "linktitle" : "OTP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2021-01-21"
}

## Ce este un fișier OTP?

Fișierele cu extensia .otp reprezintă fișiere șablon de prezentare create de aplicații în format standard OASIS OpenDocument. Conținutul unui astfel de fișier include informații de prezentare sub formă de diapozitive cu text, imagini, forme, conținut multimedia, efecte de tranziție și alte elemente de diapozitiv. Aceste fișiere șablon sunt folosite pentru a crea rapid prezentări noi pe baza informațiilor de stil stocate în șablonul însuși. Fișierele OTP pot fi create și salvate cu mai multe aplicații diferite, cum ar fi Impress, care vine cu suita OpenOffice și Microsoft PowerPoint. Formatul de fișier OTP este similar cu fișierele șablon Microsoft PowerPoint [.pot](/ro/presentation/pot/) și [.potx](/ro/presentation/potx/).

## Format de fișier OTP

Formatul de fișier OTP se bazează pe standardul OpenDocument care acceptă reprezentarea documentelor ca un singur document XML, precum și colectarea mai multor sub-documente într-un singur pachet arhivat în formatul [ZIP](/ro/compression/zip/). Conținutul fișierului este distribuit în mai multe fișiere xml împachetate împreună. Aceste mai multe fișiere [XML](/ro/web/xml/) conțin informații despre stilul, conținutul, metainformațiile și setările documentului, așa cum este menționat mai jos.

* `content.xml` – Conținutul documentului și stilurile automate utilizate în conținut.
* `styles.xml` – Stiluri utilizate în conținutul documentului și stiluri automate utilizate în stilurile în sine.
* `meta.xml` – Meta informațiile documentului, cum ar fi autorul sau ora ultimei acțiuni de salvare.
* `settings.xml` – setări specifice aplicației, cum ar fi dimensiunea ferestrei sau informațiile despre imprimantă.

## Referințe

* [OpenDocument - Prin Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

