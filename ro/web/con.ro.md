{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier CON - Formatul fișierului sursă al aplicației concept",
  "description" :"Aflați despre ce este un fișier CON și API-urile care pot crea și deschide fișiere CON.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## Ce este un fișier CON?

Un fișier CON este un fișier de cod sursă pentru aplicația dezvoltată pentru **Concept Application Server**. Este folosit pentru scrierea aplicațiilor pentru schimbul de date între server și utilizator. Fișierele CON găzduite pe server sunt accesibile cu un browser Web, cu condiția ca Concept Client să fie instalat la nivelul utilizatorului. Serverul Concept Application este un server web cu limbaj de programare la scară mică care poate avea un motor de bază de date subset [SQL](/ro/database/sql/) (TinDB).

Fișierele CON se pot deschide/rula cu RadGs Concept Application Server.

## Format de fișier CON - Mai multe informații

Fișierele CON sunt găzduite pe server și sunt accesate folosind browser-ul web de pe computerul utilizatorului. Conceptul [URL-urile](/ro/web/url/) sunt diferite de adresele URL HTTP normale și încep cu **concept://**.

### CON Exemplu de adresă URL a fișierului

Un fișier CON găzduit pe Concept Application Server poate fi accesat prin browser web folosind URL-uri precum:

```
concept://domain.server.com/web_application/main.con.
```
## Referințe

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

