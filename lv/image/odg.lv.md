{
  "date": "2019-10-11",
  "keywords": [
"odg fails",
"odg faila formāts",
"kas ir odg fails",
"failu",
"dīvains piemērs",
"odg faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODG faila formāts",
  "description": "Uzziniet par ODG faila formātu un API, kas var izveidot un atvērt ODG failus.",
  "linktitle": "ODG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-od-lvg"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir ODG fails?

ODG faila formātu izmanto Apache OpenOffice lietojumprogramma Draw, lai saglabātu zīmēšanas elementus kā vektora attēlu. Tas atbilst XML faila formāta specifikācijām, kas izklāstītas Advancement of Structural Information Standards (OASIS). ODG attēlo zīmējumus kā vektora attēlus, izmantojot punktus, līnijas un līknes. Papildus OpenOffice, LibreOffice un citas lietojumprogrammas nodrošina arī atbalstu darbam ar ODG failu formātu. Citi OpenOffice atbalstītie formāti, piemēram, ietver [ODT](/word-processing/odt/), ODF, [ODP](/presentation/odp/) un [ODS](/spreadsheet/ods/).


## ODG faila formāta specifikācijas

ODG faila formāts ir balstīts uz OpenDocument formātu, kas ir strukturēts XML dokumenta formāts ar labi definētu shēmu.
Katru OpenDocument formāta strukturālo komponentu attēlo elements, kam ir saistīti atribūti. Uz XML balstīta struktūra ir izplatīta visiem dokumentu veidiem, piemēram, teksta dokumentiem, izklājlapām vai zīmējuma failiem. Dokumentā var būt dažādi stili. OpenDocument faila struktūra sastāv no šādiem elementiem.
  * Dokumenta sakne
  * Dokumenta metadati
  * Ķermeņa elementu un dokumentu veidi
  * Lietojumprogrammu iestatījumi
  * Skripti
  * Fonta sejas deklarācijas
  * Stili
  * Lapu stili un izkārtojumi

##  Dokumenta saknes ##

Dokumenta saknes elements satur visu dokumentu un ir OpenDocument formāta faila primārais elements. Viena veida dokumenta saknes elementi ir piemērojami visu veidu dokumentiem, piemēram, tekstam, dokumentiem, izklājlapām un zīmēšanas dokumentiem.

### Saknes elementi ###
Atsevišķs XML dokuments tiek attēlots ar savu saknes elementu. Pieci dažādi atbalstītie saknes elementi ir šādi.

`<office:document> ` - Pabeigt biroja dokumentu vienā XML dokumentā.
`<office:document-content> ` - dokumenta saturs un saturā izmantotie automātiskie stili.
`<office:document-styles> ` — dokumenta saturā izmantotie stili un pašos stilos izmantotie automātiskie stili.
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings> ` — lietojumprogrammai specifiski iestatījumi, piemēram, loga izmērs vai informācija par printeri.

### ODG dokumenta metadati ###
The OpenDocument contains all metadata elements in the \<office:meta> element. This general information about a document is contained at the start of the document and applications can update multiple instances of the same elements.

### Virsbūves elementi un dokumentu veidi ###
Dokumenta pamatteksts norāda dokumentā ietvertā satura veidu, izmantojot dokumenta tipa elementu. Šie dokumentu veidi ir:
  * teksta dokumenti
  * zīmēšanas dokumentus
  * prezentācijas dokumenti
  * izklājlapu dokumenti
  * diagrammu dokumenti
  * attēlu dokumenti

### Lietojumprogrammas iestatījumi ###
The settings for office applications represent different settings that are related to the document configuration or visual appearance of the document. Each category is represented by a `<config:config-item-set>`. Examples of such setting categories include:
  * Dokumenta iestatījumi, piemēram, noklusējuma printeris
  * Skatīt iestatījumus, piemēram, tālummaiņas līmeni

### Skripti ###
It is common for a document to contain several scripts. Each script in an OpenDocument file is represented by an `<office:script>` element. These script elements are contained in a single `<office:scripts>` element. Scripts do not update a document while the document is loading.
### Fonta sejas deklarācijas ###

Fonta sejas deklarācija satur informāciju par dokumenta autora izmantotajiem fontiem. Šī informācija palīdz atrast šos fontus citās sistēmās.
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
### Stili ###
OpenDocument formāts atbalsta šādus stilus.

Kopējie stili — šādu stilu XML attēlojumi tiek saukti par stiliem
Automātiskie stili — satur formatējuma rekvizītus, kas dokumenta lietotāja interfeisa skatā tiek piešķirti objektam, piemēram, rindkopai.
`Mater Styles` — izplatīts stils, kas satur formatēšanas informāciju un papildu saturu, kas tiek parādīts kopā ar dokumenta saturu, kad stils tiek lietots. Galvenā stila piemērs ir galvenās lapas.

## Atsauces Nr.
  * [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
  * [OpenDocument formāts — Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

