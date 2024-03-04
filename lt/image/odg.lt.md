{
  "date": "2019-10-11",
  "keywords": [
"odg failą",
"odg failo formatas",
"kas yra odg failas",
"failą",
"keistas pavyzdys",
"odg failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODG failo formatas",
  "description": "Sužinokite apie ODG failo formatą ir API, kurios gali kurti ir atidaryti ODG failus.",
  "linktitle": "ODG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-od-ltg"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra ODG failas?

ODG failo formatą naudoja Apache OpenOffice programa Draw, kad išsaugotų piešimo elementus kaip vektorinį vaizdą. Ji atitinka XML failo formato specifikacijas, nurodytas Struktūrinės informacijos standartų pažangoje (OASIS). ODG vaizduoja brėžinius kaip vektorinius vaizdus naudojant taškus, linijas ir kreives. Be OpenOffice, LibreOffice ir kitos programos taip pat palaiko darbą su ODG failo formatu. Kiti OpenOffice palaikomi formatai, pavyzdžiui, yra [ODT](/word-processing/odt/), ODF, [ODP](/presentation/odp/) ir [ODS](/spreadsheet/ods/).


## ODG failo formato specifikacijos

ODG failo formatas yra pagrįstas OpenDocument formatu, kuris yra struktūrinio XML dokumento formatas su gerai apibrėžta schema.
Kiekvienas OpenDocument formato struktūrinis komponentas yra pavaizduotas elementu, turinčiu susijusius atributus. XML pagrįsta struktūra yra bendra visiems dokumentų tipams, pvz., tekstiniam dokumentui, skaičiuoklei ar piešinio failui. Dokumente gali būti įvairių stilių. OpenDocument failo struktūrą sudaro šie elementai.
  * Dokumento šaknis
  * Dokumento metaduomenys
  * Kūno elementų ir dokumentų tipai
  * Programos nustatymai
  * Scenarijai
  * Šrifto veidų deklaracijos
  * Stiliai
  * Puslapių stiliai ir išdėstymai

##  Dokumento šaknys ##

Dokumento šakniniame elemente yra visas dokumentas ir jis yra pagrindinis OpenDocument formato failo elementas. Tie patys dokumentų šakninių elementų tipai taikomi visų tipų dokumentams, tokiems kaip tekstas, dokumentai, skaičiuoklės ir piešimo dokumentai.

### Šakniniai elementai ###
Vieną XML dokumentą vaizduoja jo šakninis elementas. Penki skirtingi palaikomi šakniniai elementai yra tokie.

`<office:document> ` - Užbaigti biuro dokumentą viename XML dokumente.
`<office:document-content> ` – dokumento turinys ir turinyje naudojami automatiniai stiliai.
`<office:document-styles> ` – dokumento turinyje naudojami stiliai ir pačiuose stiliuose naudojami automatiniai stiliai.
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings> ` – konkrečios programos nustatymai, pvz., lango dydis arba spausdintuvo informacija.

### ODG dokumento metaduomenys ###
The OpenDocument contains all metadata elements in the \<office:meta> element. This general information about a document is contained at the start of the document and applications can update multiple instances of the same elements.

### Kūno elementai ir dokumentų tipai ###
Dokumento turinys nurodo dokumente esančio turinio tipą, naudodamas dokumento tipo elementą. Šie dokumentų tipai yra:
  * tekstinius dokumentus
  * piešimo dokumentus
  * pristatymo dokumentai
  * skaičiuoklės dokumentai
  * diagramos dokumentus
  * vaizdo dokumentai

### Programos nustatymai ###
The settings for office applications represent different settings that are related to the document configuration or visual appearance of the document. Each category is represented by a `<config:config-item-set>`. Examples of such setting categories include:
  * Dokumento nustatymai, pvz., numatytasis spausdintuvas
  * Peržiūrėti nustatymus, pvz., priartinimo lygį

### Scenarijai ###
It is common for a document to contain several scripts. Each script in an OpenDocument file is represented by an `<office:script>` element. These script elements are contained in a single `<office:scripts>` element. Scripts do not update a document while the document is loading.
### Šrifto veido deklaracijos ###

Šrifto veido deklaracijoje pateikiama informacija apie dokumento autoriaus naudojamus šriftus. Ši informacija padeda rasti šiuos šriftus kitose sistemose.
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
### Stiliai ###
OpenDocument formatas palaiko šiuos stilius.

Bendrieji stiliai – tokių stilių XML atvaizdai vadinami stiliais
Automatiniai stiliai – yra formatavimo ypatybių, kurios dokumento vartotojo sąsajos rodinyje priskiriamos objektui, pvz., pastraipai.
Mater Styles – įprastas stilius, kuriame yra formatavimo informacijos ir papildomo turinio, kuris rodomas kartu su dokumento turiniu, kai taikomas stilius. Pagrindinio stiliaus pavyzdys yra puslapiai.

## Nuorodos Nr.
  * [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
  * [OpenDocument formatas – Vikipedija](https://en.wikipedia.org/wiki/OpenDocument)

