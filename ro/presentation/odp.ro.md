{
  "date" : "2019-10-11",
  "keywords" :[ "fișier odp", "format fișier odp", "ce este un fișier odp", "fișier", "exemplu odp", "extensie fișier odp", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - Format fișier de prezentare OpenOffice",
  "description":"Aflați despre formatul de fișier ODP și despre API-urile care pot crea și deschide fișiere ODP.",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier ODP?

Fișierele cu extensia .odp reprezintă formatul de fișier de prezentare utilizat de OpenOffice.org în standardul OASISOpen. Un fișier de prezentare este o colecție de diapozitive în care fiecare diapozitiv poate cuprinde text, imagini, formatare, animații și alte medii. Aceste diapozitive sunt prezentate publicului sub formă de prezentări de diapozitive cu setări de prezentare personalizate. Fișierele ODP pot fi deschise de aplicații care sunt conforme cu formatul OpenDocument (cum ar fi OpenOffice sau StarOffice).

## Scurt istoric

Specificațiile de format de fișier ODP se bazează pe standardul dezvoltat ca specificații ODF. Aceste specificații au evoluat în trecut sub forma a trei versiuni dezvoltate și publicate de OASIS, după cum urmează:

`2005` - Versiunea 1.0 a fost publicată în mai 2005
`2007` - Versiunea 1.1 a fost publicată în februarie 2007
`2011` - Versiunea 1.2 a fost publicată în septembrie 2011

Au existat modificări destul de minore în tranziția de la versiunile ODF 1.0 la 1.1. [Versiunea ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) este cea mai recentă versiune pentru specificațiile ODF și ar trebui să fie consultată de dezvoltatori pentru dezvoltarea aplicațiilor legate de citirea/scrierea ODS.

## Specificații de format de fișier

Formatul OpenDocument acceptă reprezentarea documentelor ca un singur document XML, precum și o colecție de mai multe subdocumente într-un pachet ca arhivă [ZIP](/compression/zip/). Fiecare dintre fișierele din arhiva ZIP stochează o parte din documentul complet. Fiecare subdocument stochează un anumit aspect al documentului. De exemplu, un subdocument conține informațiile despre stil, iar un alt subdocument conține conținutul documentului. Un document ODF tipic are următoarele componente:

* `content.xml` – Conținutul documentului și stilurile automate utilizate în conținut.
* `styles.xml` – Stiluri utilizate în conținutul documentului și stiluri automate utilizate în stilurile în sine.
* `meta.xml` – Meta informațiile documentului, cum ar fi autorul sau ora ultimei acțiuni de salvare.
* `settings.xml` – setări specifice aplicației, cum ar fi dimensiunea ferestrei sau informațiile despre imprimantă.

Pe lângă acestea, în pachet pot fi multe alte subdocumente, cum ar fi miniatură de document, imagini etc.

Fișierele documentului cu foi de calcul sunt subsetul de fișiere ODF în care conținutul (foile) este stocat în subdocumentul content.xml.

## Referințe

* [OpenDocument - Prin Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

