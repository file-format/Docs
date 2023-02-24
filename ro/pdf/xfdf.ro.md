{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fișier XFDF - Ce este un fișier XFDF?",
  "description":"Aflați despre fișierul XFDF și API-urile care pot crea și deschide fișiere XFDF.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier XFDF?

Un fișier cu extensia .xfdf este un format de date XML Forms care este generat cu software-ul Adobe Acrobat. La fel ca [FDF](/ro/pdf/fdf/), XFDF conține descrierea elementelor de formular și valorile acestora în format XML. Aceasta poate include numele și valorile câmpurilor de text din formularul PDF. XFDF sunt salvate în format care poate fi citit de om și pot fi citite prin programare folosind limbaje de programare precum C#.

## Format de fișier XFDF - Mai multe informații

Fișierele XFDF sunt salvate în format de fișier XML, care este un format universal utilizat pentru importul și exportul de date. O structură de fișier XFDF constă dintr-un antet, urmat de valorile câmpului și datele elementelor, așa cum se arată mai jos.

|Element|Atribut|Conținut|
---|---|---|
|\<XFDF> ||Elementul cel mai de sus|
|\<fields> ||Toate valorile câmpurilor pentru acest șablon|
|<field (T)> |nume |Numele câmpului|
|<value (V)> |valoare |Valoare câmp|

## Referințe

* [FDF Format Support by Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Resurse pentru dezvoltatori Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

