{
  "date" : "2019-10-11",
  "keywords" :[ "xpm-fil", "xpm-filformat", "vad är en xpm-fil", "fil", "xpm-exempel", "xpm-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - X PixMap filformat",
  "description":"Läs mer om XPM-filformat och API:er som kan skapa och öppna XPM-filer.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är XPM fil?

En fil med filtillägget .xpm är ett bildfilformat som användes av X Windows-systemet. Den stöder genomskinliga pixlar och är vanligtvis inriktad på att skapa ikon-pixmaps. Den stöder monokrom, gra-skala och färg pixmap-data. Dessa designades för att kunna redigeras för hand och kan inkluderas i [C](/sv/programming/c/)-koden. För detta ändamål är XPM-filer i vanlig textfilformat och följer programmeringsspråkets C-syntax. XPM-filer kan öppnas med en mängd olika bildvisningsprogram som t.ex
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView och Canvas X.

## XPM filformat

XPM-filformatet använder C-syntax för att dessa ska integreras i C- och C++-program. Den består av följande sex olika sektioner.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

Sektionerna är faktiskt en rad strängar enligt följande.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Nedan följer detaljerna för varje avsnitt.

`<Values> ` - Det här avsnittet är en sträng som innehåller fyra eller sex heltal som är i bas 10 och motsvarar:

* pixmap bredd och höjd
* antal färger
* antal tecken per pixel
* valfria hotspot-koordinater och XPMEXT-tagg

`<Colors> ` - Det här avsnittet innehåller lika många strängar som det finns färger. Varje sträng är som följer:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Denna sektion består av<height> strängar och<width> \*<chars_per_pixel> tecken. Varje<chars_per_pixel> längdsträngen bör vara en av de tidigare definierade grupperna i<Colors> sektion.

`<Extension> ` - Förlängningsdelen måste märkas, om den inte är tom, i<Values> sektion. Den kan bestå av flera<Extension> underavsnitt som kan vara av följande två typer:

* en fristående sträng sammansatt enligt följande: XPMEXT<extension-name><extension-data>
* eller ett block som består av flera strängar: XPMEXT<extension-name><related extension-data composed of several strings>

## Referenser

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [XPM-manual](http://www.xfree86.org/current/xpm.pdf)

