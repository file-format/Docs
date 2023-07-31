{
  "date" : "2019-10-11",
  "keywords" :[ "fișier vstm", "format fișier vstm", "ce este un fișier vstm", "fișier", "exemplu vstm", "extensie fișier vstm", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTM - Format de fișier șablon Microsoft Visio",
  "description":"Aflați despre formatul de fișier VSTM și despre API-urile care pot crea și deschide fișiere VSTM.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier VSTM?

Fișierele cu extensia VSTM sunt fișiere șablon create cu Microsoft Visio care acceptă macrocomenzi. Spre deosebire de fișierele VSDX, fișierele create din șabloanele VSTM pot rula macrocomenzi care sunt dezvoltate în codul Visual Basic pentru aplicații (VBA). Un fișier șablon poate fi creat pentru a oferi setări de bază ale documentului care pot fi utilizate pentru a genera documente suplimentare cu aceste setări. Fișierele Visio sunt utilizate pentru a crea desene care conțin obiecte vizuale, diagrame de flux, diagramă UML, flux de informații, organigrame, diagrame software, aspect de rețea, modele de baze de date, cartografiere a obiectelor și alte informații similare. Fișierele generate folosind Visio pot fi, de asemenea, exportate în diferite formate de fișiere, cum ar fi PNG, BMP, PDF și altele.

## Tipul fisierului ##

Fișierele VSTM se bazează pe Convențiile de ambalare deschisă și XML, iar dezvoltatorii pot beneficia de acest format învățând cum să lucreze cu aceste fișiere în mod programatic. Formatul moștenește multe dintre aceleași structuri XML ca părțile sale din formatul de fișier Visio XML Drawing (.vdx). Interoperabilitatea cu fișierele Visio este mult crescută, deoarece software-ul terță parte poate manipula fișierele Visio la nivel de format de fișier.

Fiecare fișier Visio este denumit pachet care conține alte fișiere sau părți. O parte a pachetului poate fi un fișier XML, o imagine sau chiar o soluție VBA. Părțile din pachet pot fi împărțite în părți „document” și „relație”.

### Document ###

Părțile documentului conțin conținutul real și metadatele fișierului Visio, cum ar fi numele fișierului, prima pagină și toate formele pe care le conține, și chiar conexiunile de date pentru forme. Imaginile și fișierele text din pachet sunt considerate părți ale documentului.

### Relații ###

Părțile de relație ale unui fișier Visio sunt stocate în folderul „_rels” și descriu modul în care părțile din pachet sunt legate de fiecare. De asemenea, oferă structura fișierului. Un document XML autonom folosește relația părinte/copil a elementelor pentru a determina relația entităților între ele. Un format de fișier Visio 2013 valid conține setul corect de părți, iar pachetul conține relațiile dintre părți.

Părțile de relație sunt documente XML care descriu relațiile dintre diferitele părți ale documentului din pachet. Ele definesc o asociere între două elemente: o sursă specificată (definită de numele și locația fișierului de relație) și o parte specificată a documentului țintă. De exemplu, părțile de relație sunt folosite pentru a descrie ce forme principale sunt asociate fișierului, modul în care paginile se raportează la fișier și între ele sau modul în care imaginile și obiectele se raportează la o anumită pagină.

## Referințe ##

* [Introducere în formatul de fișier Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

