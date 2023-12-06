{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier OAM - Format fișier Adobe Edge Animate Widget",
  "description" :"Aflați despre ce este un fișier OAM și API-urile care pot crea și deschide fișierul OAM.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## Ce este un fișier OAM?

Un fișier .oam un fișier widget animat exportat din Adobe Edge Animate Widget. Animațiile exportate ca format de fișier widget OAM pot fi inserate în alte aplicații Adobe, cum ar fi InDesign Documents ([INDD file](/ro/page-description-language/indd/), Dreamweaver și Muse. Fișierele OAM sunt ca pachete de implementare care pot fi ușor inserate în alte proiecte Adobe pentru a le folosi. Fișierele OAM conțin informații despre activele, comportamentele și codul de script de acțiune ale animației. Puteți crea un fișier OAM publicând un proiect Adobe Animate [fișier .AN](/ro/web/an/) .
Utilizatorii pot crea fișiere OAM publicând dintr-un proiect Edge Animate (fișier .AN).

## Format de fișier OAM

Un fișier OAM este salvat pe disc ca arhivă [ZIP](/ro/compression/zip/) comprimată. Acest lucru implică faptul că puteți redenumi extensia fișierului în .zip și puteți extrage cu orice utilitar de compresie, cum ar fi WinZIP sau WinRAR. Dimensiunea redusă a fișierului facilitează transferul și partajarea animației cu alți utilizatori pe internet.

### Structura fișierului OAM

Structura internă de fișiere a unui fișier .oam este proprietară și nu este documentată public de Adobe. Cu toate acestea, se știe că fișierele .oam conțin o colecție de fișiere și resurse (cum ar fi grafică, audio și cod ActionScript) împachetate într-un singur fișier. Conținutul unui fișier .oam poate include fișiere [XML](/ro/web/xml/), fișiere SWF și alte fișiere de resurse. Structura exactă a fișierului .oam depinde de versiunea specifică de Adobe Animate utilizată pentru a-l crea, precum și de tipul de animație și de elementele incluse în fișier.

Un fișier OAM conține următoarele informații.

"Active:" informații despre elementele grafice, audio și video utilizate în animație.

`Comportamente:` Descrieri ale acțiunilor și interacțiunilor care au loc în animație.

`Cod ActionScript:` Codul folosit pentru a controla comportamentul și interactivitatea animației.

`Setări de publicare:` Informații despre platforma și formatul în care va fi publicată animația, cum ar fi HTML5 sau AIR.

`Metadate:` informații suplimentare, cum ar fi autorul animației, data creării și numărul versiunii.

## Cum se deschide fișierul OAM?

Puteți utiliza următoarele aplicații pentru a deschide fișiere OAM.

* Adobe Edge Animate CC (Întrerupt)
* Adobe Animate 2023
* Adobe InDesign 2023
* Adobe Dreamweaver 2021

## Referințe

* [OAM Publishing](https://helpx.adobe.com/animate/using/OAM-publishing.html)

