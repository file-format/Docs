{
  "date": "2021-05-24",
  "keywords": [
"zul",
"Fil",
"Udvidelse",
"Filformat",
"Filudvidelse",
"åben"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZUL - ZK brugergrænsefladefil",
  "description": "Lær om ZUL filformat og API'er, der kan oprette og åbne ZUL filer.",
  "linktitle": "ZUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-zu-dal"
}
},
  "lastmod": "2021-05-24"
}

## Hvad er ZUL fil?

En fil med filtypen .zul er en webfil, der er oprettet med User Interface Markup Language (ZUML) og indeholder definitioner for brugergrænsefladeelementer. Ajax- og Java-klasser understøtter brug af den [XML](/web/xml/)-baserede ZUML til udvikling af serversidefiler. ZUL-filformatet er udviklet af ZK, en UI-ramme, der giver dig mulighed for at bygge web- og mobilapplikationer uden kendskab til JavaScript eller AJAX.

## ZUL filformat

ZUL files are XML-based, consisting of different elements to construct user interface. The ZK loader uses each XML element to create a component. The overall processing of the page elements such as page title, description, etc. are described by each XML processing instruction of ZUML.

### ZUL Eksempel

I det følgende eksempel på ZUML-kode angiver den første linje sidetitlen, den anden linje opretter en rodkomponent med titel og kant, og den tredje linje opretter en knap med etiket og en begivenhedslytter.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
ZUL-skemaet kan downloades fra https://www.zkoss.org/2005/zul/zul.xsd.
## Referencer

* [ZUL - Af ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)

* [ZUL-skema](https://www.zkoss.org/2005/zul/zul.xsd)


