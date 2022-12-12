{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "Specificații hârtie XML", "Fișier", "Extensie", "Format fișier", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - Format de fișier cu aspect de pagină",
  "description":"Aflați despre formatul de fișier XPS și despre API-urile care pot crea și deschide fișiere XPS.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Ce este un fișier XPS? ##

Un fișier XPS reprezintă fișiere de aspect de pagină care se bazează pe specificațiile XML Paper create de Microsoft. A fost dezvoltat ca înlocuitor al formatului de fișier EMF și este similar cu formatul de fișier [PDF](/ro/pdf/), dar folosește XML în aspectul, aspectul și informațiile de tipărire ale unui document. Este, de fapt, mai justificat să spunem că XPS este o încercare de PDF, dar nu a putut obține suficientă popularitate așa cum este deținut de PDF din multe motive. Microsoft furnizează XPS Document Writer în mod implicit de la Windows 7 înainte pentru crearea de fișiere XPS. Fișierele XPS pot fi generate selectând „Microsoft XPS Document Writer” ca imprimantă în timpul tipăririi documentului.

Vizualizatoarele XPS sunt integrate ca parte a Windows Vista, Windows 7, Windows 8 și Internet Explorer 6 sau o versiune ulterioară. Fișierele XPS devin numai pentru citire odată ce sunt generate. Acest lucru sporește încrederea utilizatorului în documentele primite trimise ca XPS pentru autenticitatea documentului. Un document XPS poate conține una sau mai multe pagini așa cum au fost convertite din documentul original.

## Scurt istoric ##

Microsoft a transmis specificația XPS către Ecma International. În iunie 2007, Ecma Technical Committee 46 (TC46) a fost înființat pentru a dezvolta un standard bazat pe OpenXPS Paper Specifications. Ecma International a aprobat Standardul Ecma (ECMA-388) [specificații XPS](http://www.ecma-international.org/publications/standards/Ecma-388.htm) în iunie 2009 la cea de-a 97-a Adunare Generală.

## Format fișier XPS ##

Formatul XPS constă dintr-un marcaj XML care definește compoziția unui document și aspectul vizual al fiecărei pagini, împreună cu regulile de randare pentru afișarea sau tipărirea documentului. Reține toate informațiile pentru a recrea un document pe orice sistem, ceea ce îl face independent de resursele disponibile pe acel sistem. Formatul este în esență o arhivă ZIP și dacă redenumiți extensia fișierului în ZIP, veți vedea fișierele constitutive care conțin datele documentului. Aceste documente includ:

* fișiere de pagină de document (.fpage) - Conține conținutul documentului și setările de format ale documentului. Fiecare pagină din documentul XPS are un fișier FPAGE.
* fișier de setări document (.fdoc) - Stochează setările incluse în arhiva XPS.
* fișiere fragment de document (.frag) - Definește setările pentru fișierul XPS real și fiecare pagină din document are propriul fișier .frag.

{{< figure src="../XPS-1.png" alt="Format de fișier XPS" >}}

Aceste fișiere păstrează conținutul documentului în așa fel încât, dacă, de exemplu, cineva nu are aceleași fonturi instalate pe computerul său, vizualizatorul XPS va reda în continuare acele fonturi originale. Aceasta implică includerea fișierului de markup XML pentru fiecare:

* Pagina
* Text
* Fonturi încorporate
* Imagini raster
* Grafică vectorială 2D
* Gestionarea drepturilor digitale

Formatul de document XPS include un set bine definit de părți și relații, fiecare îndeplinind un anumit scop în document. Formatul extinde, de asemenea, caracteristicile pachetului, inclusiv semnături digitale, miniaturi și intercalare.

Un document XPS tipic arată după cum urmează și poate fi analizat în lumina formatului de fișier XPS [specificații](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="Format de fișier XPS" >}}


## Referințe ##

* [Specificații de format de fișier XPS](http://www.ecma-international.org/publications/standards/Ecma-388.htm)
* [XPS - Prin Wikipedia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

