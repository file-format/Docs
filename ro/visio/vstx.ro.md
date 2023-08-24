{
  "date" : "2019-10-11",
  "keywords" :[ "fișier vstx", "format fișier vstx", "ce este un fișier vstx", "fișier", "exemplu vstx", "extensie fișier vstx", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTX - Format de fișier Microsoft Visio",
  "description":"Aflați despre formatul de fișier VSTX și despre API-urile care pot crea și deschide fișiere VSTX.",
  "linktitle" : "VSTX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier VSTX?

Fișierele cu extensii .vstx sunt fișiere șablon de desen create cu Microsoft Visio 2013 și versiuni ulterioare. Aceste fișiere VSTX oferă punctul de plecare pentru crearea desenelor Visio, salvate ca fișiere [.VSDX](/ro/visio/vsdx/), cu aspect și setări implicite. În general, fișierele Visio sunt folosite pentru a crea desene care conțin obiecte vizuale, diagrame de flux, diagramă UML, flux de informații, organigrame, diagrame software, aspect de rețea, modele de baze de date, cartografiere de obiecte și alte informații similare. Fișierele generate folosind Visio pot fi, de asemenea, exportate în diferite formate de fișiere, cum ar fi [PNG](/ro/image/png/), [BMP](/ro/image/bmp/), [PDF](/ro/pdf/) și altele. Programele care deschid fișiere VSTX includ Microsoft Visio pentru Windows și Mac care vă permit să deschideți aceste fișiere pentru vizualizare și editare. De asemenea, permite convertirea formatelor de fișiere Visio într-o serie de alte formate.

# Format fișier VSTX #

„X” din extensia de fișier se referă la formatul de fișier OpenOffice care a fost introdus de Microsoft ca format de fișier arhivă [ZIP](/ro/compression/zip/) pentru înlocuirea formatelor de fișiere binare acceptate anterior. Prin urmare, fișierele VSTX se bazează pe formatul de fișier XML al specificațiilor OpenOffice, spre deosebire de formatul de fișier [.VST](/ro/visio/vst/), care este în format binar.

Fișierele VSDX se bazează pe Convențiile de ambalare deschisă și XML, iar dezvoltatorii pot beneficia de acest format învățând cum să lucreze cu aceste fișiere în mod programatic. Formatul moștenește multe dintre aceleași structuri XML ca părțile sale din formatul de fișier Visio XML Drawing (.vdx). Interoperabilitatea cu fișierele Visio este mult crescută, deoarece software-ul terță parte poate manipula fișierele Visio la nivel de format de fișier.

Anumite alte tipuri de fișiere care cuprind formatul de fișier Visio 2013 includ:

* .vsdm (desen activat pentru macrocomandă Visio)
* .vssx (Șablon Visio)
* .vssm (şablon cu macrocomandă Visio)
* .vstx (șablon Visio)
* .vstm (șablon Visio activat pentru macrocomandă)

Sub capotă, formatul de fișier Visio 2013 utilizează un mijloc structurat pentru a stoca datele aplicației împreună cu resursele aferente într-o arhivă, cum ar fi [ZIP](/ro/compression/zip/). Fișierul ZIP poate fi extras folosind orice utilitar de extragere standard unde conține și alte tipuri de fișiere. Puteți înlocui doar extensia de fișier .VSTX cu .ZIP în Windows Explorer pentru a vedea conținutul din fișierul VSTX.

Fiecare fișier Visio este denumit pachet care conține alte fișiere sau părți. O parte a pachetului poate fi un fișier XML, o imagine sau chiar o soluție VBA. Părțile din pachet pot fi împărțite în părți „document” și „relație”.

### Document ###

Părțile documentului conțin conținutul real și metadatele fișierului Visio, cum ar fi numele fișierului, prima pagină și toate formele pe care le conține, și chiar conexiunile de date pentru forme. Imaginile și fișierele text din pachet sunt considerate părți ale documentului.

### Relații ###

Părțile de relație ale unui fișier Visio sunt stocate în folderul „_rels” și descriu modul în care părțile din pachet sunt legate de fiecare. De asemenea, oferă structura fișierului. Un document XML autonom folosește relația părinte/copil a elementelor pentru a determina relația entităților între ele. Un format de fișier Visio 2013 valid conține setul corect de părți, iar pachetul conține relațiile dintre părți.

Părțile de relație sunt documente XML care descriu relațiile dintre diferitele părți ale documentului din pachet. Ele definesc o asociere între două elemente: o sursă specificată (definită de numele și locația fișierului de relație) și o parte specificată a documentului țintă. De exemplu, părțile de relație sunt folosite pentru a descrie ce forme principale sunt asociate fișierului, modul în care paginile se raportează la fișier și între ele sau modul în care imaginile și obiectele se raportează la o anumită pagină.

## Referințe ##

* [Introducere în formatul de fișier Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

