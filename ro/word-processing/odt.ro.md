{
  "date" : "2019-10-11",
  "keywords" :[ "fișier odt", "format fișier odt", "ce este un fișier odt", "fișier", "exemplu odt", "extensie fișier odt", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODT – fișier text OpenDocument",
  "description":"Aflați despre formatul de fișier ODT și despre API-urile care pot crea și deschide fișiere ODT.",
  "linktitle" : "ODT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier ODT?

Fișierele ODT sunt tipuri de documente create cu aplicații de procesare de text care se bazează pe formatul OpenDocument Text File. Acestea sunt create cu aplicații de procesor de text, cum ar fi OpenOffice Writer gratuit și pot conține conținut precum text, imagini, obiecte și stiluri. Fișierul ODT este pentru procesorul de text Writer ceea ce este [DOCX](/ro/word-processing/docx/) pentru Microsoft Word. Mai multe aplicații, inclusiv Google Docs și procesorul de text de la Google, inclus în Google Drive, pot deschide fișierele ODT pentru editare. De asemenea, Microsoft Word poate deschide fișiere ODT și le poate salva în alte formate, cum ar fi [DOC](/ro/word-processing/doc/) și DOCX.

## Scurt istoric ##

Specificațiile de format de fișier ODP se bazează pe standardul dezvoltat ca specificații ODF. Aceste specificații au evoluat în trecut sub forma a trei versiuni dezvoltate și publicate de OASIS, după cum urmează:

**2005** Versiunea 1.0 a fost publicată în mai 2005

**2007:** Versiunea 1.1 a fost publicată în februarie 2007

**2011:** Versiunea 1.2 a fost publicată în septembrie 2011

Au existat modificări destul de minore în tranziția de la versiunile ODF 1.0 la 1.1. [Versiunea ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) este cea mai recentă versiune pentru specificațiile ODF și ar trebui să fie consultată de dezvoltatori pentru dezvoltarea aplicațiilor legate de citirea/scrierea ODS.

## Specificații de format de fișier ##

Formatul OpenDocument acceptă reprezentarea documentelor ca un singur document XML, precum și o colecție de mai multe subdocumente într-un pachet ca arhivă [ZIP](/ro/compression/zip/). Fiecare dintre fișierele din arhiva ZIP stochează o parte din documentul complet. Fiecare subdocument stochează un anumit aspect al documentului. De exemplu, un subdocument conține informațiile despre stil, iar un alt subdocument conține conținutul documentului. Un document ODF tipic are următoarele componente:

* content.xml – Conținutul documentului și stilurile automate utilizate în conținut.
* styles.xml – Stiluri utilizate în conținutul documentului și stiluri automate utilizate în stilurile în sine.
* meta.xml – Meta informațiile documentului, cum ar fi autorul sau ora ultimei acțiuni de salvare.
* settings.xml – Setări specifice aplicației, cum ar fi dimensiunea ferestrei sau informațiile despre imprimantă.

Pe lângă acestea, în pachet pot fi multe alte subdocumente, cum ar fi miniaturile documentului, imaginile etc. Fișierele document sunt subsetul de fișiere ODF în care conținutul (foile) este stocat în subdocumentul //content.xml//.

## Referințe ##

* [OpenDocument - Prin Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

