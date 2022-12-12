{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "fișier", "extensie", "format fișier", "Excel", "Foaie de calcul"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier OTS și despre API-urile care pot crea și deschide fișiere OTS.",
  "title" :"OTS – Format de fișier șablon de foaie de calcul OpenDocument",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Ce este un fișier OTS?

Un fișier cu extensia .ots este un fișier OpenDocument Spreadsheet Template care este creat cu aplicația software Calc inclusă în Apache OpenOffice. Aplicația software Calc este similară cu Excel disponibil în Microsoft Office. Formatul de fișier OTS este utilizat pentru a crea șabloane care conțin setări predefinite legate de stiluri, font, date, aspectul foii de calcul și formatare. Fișierele OTF au `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. Aceste fișiere șablon pot fi folosite ca punct de plecare pentru a genera și salva fișiere de date reale care sunt salvate în [format de fișier ODS](/ro/spreadsheet/ods/). Fișierele OTS pot fi utilizate cu aplicații precum OpenOffice și LibreOffice.

## Format de fișier OTS

Fișierele OTS sunt salvate în formatul de fișier OASIS OpenDocument bazat pe XML, care cuprinde o colecție de mai multe subdocumente cu un pachet ca arhivă [ZIP](/ro/compression/zip/). Fiecare arhivă zip stochează o parte din documentul complet și fiecare subdocument stochează un anumit aspect al documentului. De exemplu, un subdocument conține informațiile de stil și un alt subdocument conține conținutul documentului. Un document ODF tipic are următoarele componente:

### OTS Content.xml

Fișierul content.xml conține conținutul real al documentului. Totuși, aceasta nu include date binare, cum ar fi imagini.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml din formatul de fișier OTS

Fișierul styles.xml conține informații de stil și este utilizat intens pentru formatare și aspect. Tipurile de stiluri includ:

* Stiluri de paragraf
* Stiluri de pagină
* Stiluri de caractere
* Stiluri de cadru
* Listează stiluri

### Meta.xml

Fișierul meta.xml conține informații despre metadatele fișierului, cum ar fi Autor, Data ultimei modificări etc.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

Fișierul `settings.xml` include setări la nivel de document, cum ar fi factorul de zoom și poziția cursorului.

## Referințe ##

* [Specificație OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - Prin Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

