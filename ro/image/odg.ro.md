{
  "date" : "2019-10-11",
  "keywords" :[ "fișier odg", "format fișier odg", "ce este un fișier odg", "fișier", "exemplu odg", "extensie fișier odg", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier ODG",
  "description":"Aflați despre formatul de fișier ODG și despre API-urile care pot crea și deschide fișiere ODG.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier ODG?

Formatul de fișier ODG este folosit de aplicația Draw a Apache OpenOffice pentru a stoca elemente de desen ca imagine vectorială. Urmează specificațiile de format de fișier bazate pe XML, prezentate de Advancement of Structural Information Standards (OASIS). ODG reprezintă desenele ca imagini vectoriale folosind puncte, linii și curbe. Pe lângă OpenOffice, LibreOffice și alte aplicații oferă și suport pentru lucrul cu formatul de fișier ODG. Alte formate acceptate de OpenOffice, de exemplu, includ [ODT](/ro/word-processing/odt/), ODF, [ODP](/ro/presentation/odp/) și [ODS](/ro/spreadsheet/ods/).


## Specificații de format de fișier ODG

Formatul de fișier ODG se bazează pe formatul OpenDocument, care este un format de document XML structurat cu o schemă bine definită.
Fiecare componentă structurală a unui format OpenDocument este reprezentată de un element care are atribute asociate. Structura bazată pe XML este comună pentru toate tipurile de documente, cum ar fi documentul text, foaia de calcul sau un desen. Un document poate conține diferite stiluri. O structură de fișier OpenDocument constă din următoarele elemente.
* Rădăcina documentului
* Metadatele documentului
* Tipuri de elemente de corp și documente
* Setările aplicației
* Scripturi
* Declarații cu fonturi
* Stiluri
* Stiluri de pagină și aspect

## Rădăcinile documentului ##

Un element rădăcină a documentului conține întregul document și este elementul principal al unui fișier în format OpenDocument. Aceleași tipuri de elemente rădăcină a documentului sunt aplicabile tuturor tipurilor de documente, cum ar fi text, documente, foi de calcul și documente desen.

### Elemente rădăcină ###
Un singur document XML este reprezentat de propriul său element rădăcină. Cele cinci elemente rădăcină suportate diferite sunt după cum urmează.

`<office:document>` - Document complet de birou într-un singur document XML.
`<office:document-content>` - Conținutul documentului și stilurile automate utilizate în conținut.
`<office:document-styles>` - Stiluri utilizate în conținutul documentului și stiluri automate utilizate în stilurile în sine.
`<office:document-meta>` - Meta informațiile documentului, cum ar fi autorul sau ora ultimei acțiuni de salvare.
`<office:document-settings>` - Setări specifice aplicației, cum ar fi dimensiunea ferestrei sau informațiile despre imprimantă.

### Metadatele documentului ODG ###
OpenDocument conține toate elementele de metadate din \<office:meta> element. Aceste informații generale despre un document sunt conținute la începutul documentului, iar aplicațiile pot actualiza mai multe instanțe ale acelorași elemente.

### Elemente de corp și tipuri de documente ###
Corpul documentului indică tipul de conținut conținut în document folosind elementul tip document. Aceste tipuri de documente sunt:
* documente text
* documente de desen
* documente de prezentare
* documente foaie de calcul
* documente grafice
* documente imagine

### Setările aplicației ###
Setările pentru aplicațiile de birou reprezintă setări diferite care sunt legate de configurația documentului sau aspectul vizual al documentului. Fiecare categorie este reprezentată de un `<config:config-item-set>`. Exemple de astfel de categorii de setări includ:
* Setări document, de exemplu, imprimantă implicită
* Vizualizare setări, de exemplu, nivelul de zoom

### Scripturi ###
Este obișnuit ca un document să conțină mai multe scripturi. Fiecare script dintr-un fișier OpenDocument este reprezentat de un `<office:script>` element. Aceste elemente de script sunt conținute într-un singur `<office:scripts>` element. Scripturile nu actualizează un document în timp ce documentul se încarcă.
### Declarații de font ###

O declarație a fontului conține informații despre fonturile utilizate de autorul unui document. Aceste informații ajută la localizarea acestor fonturi pe alte sisteme.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Stiluri ###
Următoarele stiluri sunt acceptate de formatul OpenDocument.

`Stiluri comune` - Reprezentările XML ale unor astfel de stiluri sunt denumite stiluri
`Stiluri automate` - Conține proprietăți de formatare care, în vizualizarea interfeței cu utilizatorul a unui document, sunt atribuite unui obiect, cum ar fi un paragraf.
„Stiluri de bază” - un stil comun care conține informații de formatare și conținut suplimentar care este afișat împreună cu conținutul documentului atunci când stilul este aplicat. Un exemplu de stil principal sunt paginile master.

## Referințe ##
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Format OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

