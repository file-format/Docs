{
  "date" : "2019-10-11",
  "keywords" :[ "vdw", "fișier vdw", "format fișier vdw", "tip fișier vdw", "fișier", "tip", "ce este un fișier vdw"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - Format de fișier Visio Graphics Service",
  "description":"Aflați despre formatul de fișier VDW și despre API-urile care pot crea și deschide fișiere VDW.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## Ce este un fișier VDW?

VDW este formatul de fișier Visio Graphics Service care specifică fluxurile și stocările necesare pentru redarea unui desen Web. Un desen web este o colecție de pagini de desen, forme, fonturi, imagini, conexiuni de date și informații de actualizare a diagramei care pot fi redate ca desen vectorial sau raster. Fișierele VDW pot fi deschise și în Microsoft Visio, dar sunt salvate în principal pentru utilizare pe web. Microsoft Visio oferă capacitatea de a converti fișierele Visio într-un număr de formate de fișiere diferite, inclusiv [PNG](/ro/Image/PNG/), [BMP](/ro/Image/BMP/), [PDF](/ro/pdf/) și altele.

## **VDW** Format de fișier

Specificațiile tehnice ale formatului de fișier VDW sunt disponibile online de către [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) și pot fi consultate de dezvoltatori pentru a crea aplicatii. Documentul tehnic descrie datele conținute într-un fișier compus care conține stocări și fluxuri. Reprezentarea unui Desen Web este posibilă printr-un flux, denumit VisioServerData, printr-o arhivă ZIP. O parte ShapGraphic XML din arhivă descrie elementele grafice afișate în desenul Web și sunt exprimate în Extensible Application Markup Language (XAML). O colecție de părți XML din arhiva ZIP descrie conexiunea de date a desenului Web, informații despre forma acestuia și logica actualizării diagramei. Aceste părți sunt exprimate ca XML. Partea DataGraphic XML descrie proprietățile recalculate care urmează să fie evaluate după ce datele din desenul Web au fost reîmprospătate din sursa de date. Elementele suplimentare din arhiva ZIP conțin informații pentru fonturile și imaginile utilizate în desenul Web.

|![Posibilă implementare a unui fișier](/ro/web/vdw.png „Posibilă implementare a unui fișier”)

## Referințe

* [[MS-VGSFF]: Format de fișier Visio Graphics Service (.vdw)](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

