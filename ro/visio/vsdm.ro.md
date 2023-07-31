{
  "date" : "2019-10-11",
  "keywords" :[ "fișier vsdm", "format fișier vsdm", "ce este un fișier vsdm", "fișier", "exemplu vsdm", "extensie fișier vsdm", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM - Microsoft Visio Drawing File Format",
  "description":"Aflați despre formatul de fișier VSDM și despre API-urile care pot crea și deschide fișiere VSDM.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier VSDM?

Fișierele cu extensia .vsdm sunt desene create cu aplicația Microsoft Visio care acceptă macrocomenzi. Fișierele VSDM sunt desene OPC/XML care sunt similare cu VSDX, dar oferă și capacitatea de a rula macrocomenzi atunci când fișierul este deschis. Macro-urile sunt acțiuni/etași definiți de utilizator care sunt dezvoltați în Visual Basic pentru aplicații (VBA) și pot fi utilizate pentru a efectua sarcini repetitive. Formatul de fișier VSDM a fost introdus odată cu lansarea Microsoft Visio 2013. Fișierele Visio sunt folosite pentru a crea desene care conțin obiecte vizuale, diagrame de flux, diagramă UML, flux de informații, organigrame, diagrame software, aspect de rețea, modele de baze de date, cartografiere a obiectelor și altele informatii similare. Fișierele generate folosind Visio pot fi, de asemenea, exportate în diferite formate de fișiere, cum ar fi [PNG](/ro/image/png/), [BMP](/ro/image/bmp/), [PDF](/ro/pdf/) și altele.

## Format de fișier VSDM

Fișierele VSDM se bazează pe Convențiile de ambalare deschisă și XML, iar dezvoltatorii pot beneficia de acest format învățând cum să lucreze cu aceste fișiere în mod programatic. Formatul moștenește multe dintre aceleași structuri XML ca părțile sale din formatul de fișier Visio XML Drawing (.vdx). Interoperabilitatea cu fișierele Visio este mult crescută, deoarece software-ul terță parte poate manipula fișierele Visio la nivel de format de fișier.

Fiecare fișier Visio este denumit pachet care conține alte fișiere sau părți. O parte a pachetului poate fi un fișier XML, o imagine sau chiar o soluție VBA. Părțile din pachet pot fi împărțite în părți „document” și „relație”.

### Document ###

Părțile documentului conțin conținutul real și metadatele fișierului Visio, cum ar fi numele fișierului, prima pagină și toate formele pe care le conține și chiar conexiunile de date pentru forme. Imaginile și fișierele text din pachet sunt considerate părți ale documentului.

### Relații ###

Părțile de relație ale unui fișier Visio sunt stocate în folderul „\_rels” și descriu modul în care părțile din pachet sunt legate de fiecare. De asemenea, oferă structura fișierului. Un document XML autonom folosește relația părinte/copil a elementelor pentru a determina relația entităților între ele. Un format de fișier Visio 2013 valid conține setul corect de părți, iar pachetul conține relațiile dintre părți.

Părțile de relație sunt documente XML care descriu relațiile dintre diferitele părți ale documentului din pachet. Ele definesc o asociere între două elemente: o sursă specificată (definită de numele și locația fișierului de relație) și o parte specificată a documentului țintă. De exemplu, părțile de relație sunt folosite pentru a descrie ce forme principale sunt asociate fișierului, modul în care paginile se raportează la fișier și între ele sau modul în care imaginile și obiectele se raportează la o anumită pagină.

## Referințe ##

* [Introducere în formatul de fișier Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

