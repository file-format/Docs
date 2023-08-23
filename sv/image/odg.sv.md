{
  "date" : "2019-10-11",
  "keywords" :[ "odg-fil", "odg-filformat", "vad är en odg-fil", "fil", "odg-exempel", "odg-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODG-filformat",
  "description":"Läs mer om ODG-filformat och API:er som kan skapa och öppna ODG-filer.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en ODG fil?

ODG-filformatet används av Apache OpenOffices Draw-applikation för att lagra ritelement som en vektorbild. Den följer de XML-baserade filformatspecifikationerna som beskrivs av Advancement of Structural Information Standards (OASIS). ODG representerar ritningar som vektorbilder med hjälp av punkter, linjer och kurvor. Förutom OpenOffice ger LibreOffice och andra applikationer även stöd för att arbeta med ODG-filformat. Andra format som stöds av OpenOffice, till exempel, inkluderar [ODT](/sv/ordbehandling/odt/), ODF, [ODP](/sv/presentation/odp/) och [ODS](/sv/spreadsheet/ods/).


## ODG filformatspecifikationer

ODG-filformat är baserat på OpenDocument-format som är strukturerat XML-dokumentformat med väldefinierat schema.
Varje strukturell komponent i ett OpenDocument-format representeras av ett element som har associerade attribut. Den XML-baserade strukturen är gemensam för alla dokumenttyper såsom textdokument, kalkylblad eller en ritfil. Ett dokument kan innehålla olika stilar. En OpenDocument-filstruktur består av följande element.
* Dokumentrot
* Dokumentmetadata
* Kroppselement och dokumenttyper
* Applikationsinställningar
* Manus
* Teckensnittsdeklarationer
* Stilar
* Sidstilar och layouter

## Dokumentrötter ##

Ett dokumentrotelement innehåller hela dokumentet och är det primära elementet i en fil i OpenDocument-format. Samma typer av dokumentrotelement är tillämpliga på alla typer av dokument som text, dokument, kalkylblad och ritdokument.

### Rotelement ###
Ett enda XML-dokument representeras av ett eget rotelement. De fem olika stödda rotelementen är följande.

`<office:document>` - Komplett office-dokument i ett enda XML-dokument.
`<office:document-content>` - Dokumentinnehåll och automatiska stilar som används i innehållet.
`<office:document-styles>` - Stilar som används i dokumentinnehållet och automatiska stilar som används i själva stilarna.
`<office:document-meta>` - Dokumentmetainformation, såsom författaren eller tidpunkten för den senaste sparande åtgärden.
`<office:document-settings>` - Programspecifika inställningar, såsom fönsterstorlek eller skrivarinformation.

### ODG Document MetaData ###
OpenDocumentet innehåller alla metadataelement i \<office:meta> element. Denna allmänna information om ett dokument finns i början av dokumentet och applikationer kan uppdatera flera instanser av samma element.

### Brödelement och dokumenttyper ###
Dokumentets brödtext anger vilken typ av innehåll som finns i dokumentet med hjälp av elementet dokumenttyp. Dessa dokumenttyper är:
* textdokument
* rita dokument
* presentationsdokument
* Kalkylbladsdokument
* kartdokument
* bilddokument

### Applikationsinställningar ###
Inställningarna för kontorsprogram representerar olika inställningar som är relaterade till dokumentets konfiguration eller visuella utseende. Varje kategori representeras av en `<config:config-item-set>`. Exempel på sådana inställningskategorier inkluderar:
* Dokumentinställningar t.ex. standardskrivare
* Visa inställningar t.ex. zoomnivå

### Skript ###
Det är vanligt att ett dokument innehåller flera skript. Varje skript i en OpenDocument-fil representeras av en `<office:script>` element. Dessa skriptelement finns i en enda `<office:scripts>` element. Skript uppdaterar inte ett dokument medan dokumentet laddas.
### Teckensnittsdeklarationer ###

En teckensnittsdeklaration innehåller information om de typsnitt som används av författaren till ett dokument. Denna information hjälper till att hitta dessa typsnitt på andra system.
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
### Stilar ###
Följande stilar stöds av OpenDocument-formatet.

`Common Styles` - XML-representationerna av sådana stilar kallas stilar
`Automatiska formatmallar` - Innehåller formateringsegenskaper som, i användargränssnittsvyn av ett dokument, tilldelas ett objekt som ett stycke.
`Mater Styles` - en vanlig stil som innehåller formateringsinformation och ytterligare innehåll som visas med dokumentinnehållet när stilen tillämpas. Ett exempel på en masterstil är master-sidor.

## Referenser ##
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument Format - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

