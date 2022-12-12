{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "fișier", "extensie", "format fișier", "OpenDocument Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ghidul dvs. de format de fișier pentru a afla ce este un fișier ODS și API-urile care le pot crea și deschide.",
  "title" :"Ce este un fișier ODS?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Ce este un fișier ODS?

Fișierele cu extensia .ods reprezintă formatul OpenDocument Spreadsheet Document care poate fi editat de către utilizator. Datele sunt stocate în fișierul ODF în rânduri și coloane. Este un format bazat pe XML și este unul dintre numeroasele subtipuri din familia Open Document Formats (ODF). Formatul este specificat ca parte a specificațiilor ODF 1.2 publicate și menținute de OASIS. O serie de aplicații pe Windows, precum și alte sisteme de operare pot deschide fișiere ODS pentru editare și manipulare, inclusiv Microsoft Excel, NeoOffice și LibreOffice. Fișierele ODS pot fi, de asemenea, convertite în alte formate de foi de calcul, precum [XLS](/ro/spreadsheet/xls/), [XLSX](/ro/spreadsheet/xlsx/) și altele prin diferite aplicații.

## Scurt istoric ##

Specificațiile de format de fișier ODS se bazează pe standardul dezvoltat ca specificații ODF. Aceste specificații au evoluat în trecut sub forma a trei versiuni dezvoltate și publicate de OASIS, după cum urmează:

`2005`- Versiunea 1.0 a fost publicată în mai 2005

`2007` - Versiunea 1.1 a fost publicată în februarie 2007

`2011` - Versiunea 1.2 a fost publicată în septembrie 2011

Au existat modificări destul de minore în tranziția de la versiunile ODF 1.0 la 1.1. [Versiunea ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) este cea mai recentă versiune pentru specificațiile ODF și ar trebui să fie consultată de dezvoltatori pentru dezvoltarea aplicațiilor legate de citirea/scrierea ODS.

## Format fișier ODS ##

Formatul OpenDocument acceptă reprezentarea documentelor ca un singur document XML, precum și o colecție de mai multe subdocumente într-un pachet ca arhivă [ZIP](/ro/compression/zip/). Fiecare dintre fișierele din arhiva ZIP stochează o parte din documentul complet. Fiecare subdocument stochează un anumit aspect al documentului. De exemplu, un subdocument conține informațiile de stil și un alt subdocument conține conținutul documentului. Un document ODF tipic are următoarele componente:

* `content.xml` – Conținutul documentului și stilurile automate utilizate în conținut.
* `styles.xml` – Stiluri utilizate în conținutul documentului și stiluri automate utilizate în stilurile în sine.
* `meta.xml` – Meta informațiile documentului, cum ar fi autorul sau ora ultimei acțiuni de salvare.
* `settings.xml` – setări specifice aplicației, cum ar fi dimensiunea ferestrei sau informațiile despre imprimantă.

Pe lângă acestea, în pachet pot fi multe alte subdocumente, cum ar fi miniatură de document, imagini etc.

Fișierele documentului cu foi de calcul sunt subsetul de fișiere ODF în care conținutul (foile) este stocat în subdocumentul content.xml.

## Referințe ##

* [OpenDocument - Prin Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

