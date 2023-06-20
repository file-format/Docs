{
  "date" : "2020-03-16",
  "keywords" :[ "PAT-fil", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om PAT-filformat och API:er som kan skapa och öppna PAT-filer.",
  "title" :"PAT filformat",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## Vad är en PAT fil?

En fil med filändelsen .pat är en CAD-fil som används av AutoCAD-programvaran. Applikationer som kan öppna PAT-filer använder det skräckmönster som lagras i dessa filer för att få information om strukturen/fyllningen av ett område. Mönstren som finns ger information om hur material ser ut på ritade föremål. PAT-filer kan öppnas i applikationer som Autodesk AutoCAD, CorelDRAW Graphics Suite och Ketron Software. PAT-filer kan konverteras till olika bildformat som JPG, PNG, BMP, etc.

## PAT filformat

PAT-filer är skrivna i vanligt textformat och kan öppnas i vilken textredigerare som helst. Hatchmönstren i dessa filer är vektorbaserade och följer syntaxen som beskrivs i AutoCAD-dokumentationen.

Alla mönster börjar vid punkten 0,0, mönstret beräknas för att täcka kläckningsgränsen.

### Mönsterdefinition

Alla mönsterdefinitioner består av följande fält:
* En ledande '\*'
* Ett namn – Namnet får inte ha mellanslag, skiljetecken, parentes eller snedstreck.
* En beskrivning

Standardformatet för kläckmönster är `<\*><name> <, beskrivning>`. Namnet och beskrivningen är åtskilda av ett kommatecken och beskrivningar får inte överstiga åttio teckenrader. Skräckmönstren definieras efter denna information.

### Hatch Pattern Exempel
Följande är ett exempel på kvadratiskt mönster
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Ett annat exempel som visar parallellogrammönster är följande.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Referenser ##

* [Hashmönster av Autodesk](https://help.autodesk.com/view/ACDLT/2018/ENU/?guid=GUID-A6F2E6FF-1717-44B6-A476-0CA817ADD77E)

