{
  "date" : "2021-05-24",
  "keywords" :["xul", "Fișier", "Extensie", "Format fișier", "Extensie fișier", "Limba interfeței utilizator XML"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - Fișier XML pentru limbajul interfeței utilizator",
  "description":"Aflați despre formatul de fișier XUL și despre API-urile care pot crea și deschide fișiere XUL.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Ce este un fișier XUL?

Un fișier cu extensia .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) înseamnă XML User Interface Language) este un fișier de limbaj de marcare bazat pe [XML](/ro/web/xml/) pentru crearea de interfețe cu utilizatorul. A fost dezvoltat de Mozilla pentru dezvoltatori pentru a crea elemente de interfață grafică cu utilizatorul similare altor limbaje de marcare utilizate pentru crearea paginilor web. XUL a fost utilizat pe scară largă de Mozilla în browserul său Firefox, unde a folosit baza de cod Mozilla. Redarea XUL se realizează folosind
[Motorul Gecko](https://en.wikipedia.org/wiki/Gecko_(software)). Furcăturile Firefox, cum ar fi Pale Moon, Basilisk și Waterfox, păstrează suport pentru suplimentele XUL. Fișierele XUL sunt identificate cu tip MIME: application/vnd.mozilla.xul+xml.

## Format de fișier XUL

Fișierele XUL sunt scrise în text simplu pe baza formatului de fișier XML și sunt redate folosind motorul Gecko. Cele trei părți principale ale unei structuri XUL sunt:

* `Conținut` - Aceasta include declarațiile ferestrei și elementele de interfață cu utilizatorul conținute în acestea.
* `Skin` - Include orice foi de stil, imagini și alte fișiere legate de teme. Aspectul unei ferestre este descris în foile de stil.
* `Locale` - Textul afișat într-o fereastră este stocat separat și seturi multiple de fișiere de limbă pot fi folosite de utilizatori.

### Exemplu XUL

Următorul exemplu creează trei butoane care sunt stivuite unul peste altul în direcție verticală.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Referințe

* [XUL - După Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [Documentație arhivată XUL - de Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

