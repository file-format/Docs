{
  "date" : "2019-10-11",
  "keywords" :[ "fișier vssx", "format fișier vssx", "ce este un fișier vssx", "fișier", "exemplu vssx", "extensie fișier vssx", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSSX - Format de fișier Visio Stencil",
  "description":"Aflați despre formatul de fișier VSSX și despre API-urile care pot crea și deschide fișiere VSSX.",
  "linktitle" : "VSSX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vssx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier VSSX?

Fișierele cu extensia .vssx sunt șabloane de desen create cu [Microsoft Visio](https://products.office.com/en/visio/flowchart-software) 2013 și mai sus. Formatul de fișier VSSX poate fi deschis cu Visio 2013 și versiuni ulterioare. Fișierele Visio sunt cunoscute pentru reprezentarea unei varietăți de elemente de desen, cum ar fi colecția de forme, conectori, diagrame de flux, aspect de rețea, diagrame UML, diagrame software, modele de baze de date, cartografiere de obiecte și alte informații similare. Microsoft Visio oferă, de asemenea, capacitatea de a converti fișiere Visio în diferite formate de fișiere, cum ar fi [PNG](/ro/image/png/), [BMP](/ro/image/bmp/), [PDF](/ro/pdf/) și altele. Este disponibil atât pentru Windows, cât și pentru Mac OS.

## Format de fișier VSSX

Formatul de fișier VSSX se bazează pe formatul OpenOffice adoptat de Microsoft din 2007. Se bazează pe arhiva [ZIP](/ro/compression/zip/) care reprezintă formatul general de fișier bazat pe specificațiile formatului de fișier XML. Echivalentul formatului de fișier binar al VSSX a fost VSS, care a fost acceptat până în Visio 2007. Puteți vizualiza conținutul formatului de fișier VSSX înlocuind extensia acestuia cu .ZIP și deschideți în orice format de fișier de arhivare, cum ar fi WinZIP.

Fișierele VSDX se bazează pe Convențiile de ambalare deschisă și XML, iar dezvoltatorii pot beneficia de acest format învățând cum să lucreze cu aceste fișiere în mod programatic. Formatul moștenește multe dintre aceleași structuri XML ca părțile sale din formatul de fișier Visio XML Drawing (.vdx). Interoperabilitatea cu fișierele Visio este mult crescută, deoarece software-ul terță parte poate manipula fișierele Visio la nivel de format de fișier.

Anumite alte tipuri de fișiere care cuprind formatul de fișier Visio 2013 includ:

* .vsdm (desen activat pentru macrocomandă Visio)
* .vssx (Șablon Visio)
* .vssm (şablon cu macrocomandă Visio)
* .vstx (șablon Visio)
* .vstm (șablon Visio activat pentru macrocomandă)

Fiecare fișier Visio este denumit pachet care conține alte fișiere sau părți. O parte a pachetului poate fi un fișier XML, o imagine sau chiar o soluție VBA. Părțile din pachet pot fi împărțite în părți „document” și „relație”.

## Referințe ##

* [Introducere în formatul de fișier Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)
* [Hartă Schema - Visio XML](https://docs.microsoft.com/en-us/office/client-developer/visio/schema-mapvisio-xml)

