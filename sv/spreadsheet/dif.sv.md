{
  "date" : "2019-12-10",
  "keywords" :[ "DIF", "fil", "tillägg", "filformat", "Data Interchange File", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Din filformatguide för att veta vad som är ett DIF-filtillägg och API:er som kan skapa och öppna DIF-filer.",
  "title" :"DIF - Data Interchange File Format",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Vad är en DIF fil?

DIF står för Data Interchange Format som används för att importera/exportera kalkylbladsdata mellan olika applikationer. Dessa inkluderar Microsoft Excel, OpenOffice Calc, StarCalc och många andra. Den lagrar data som finns i ett enda kalkylblad vilket är den enda begränsningen för detta filformat.

## Kort historik över DIF-filformat ##

DIF-filformatet utvecklades av Software Arts, Inc. i början av 1980-talet. Filformatspecifikationerna för DIF ingick i VisiCalc som var det första kalkylprogram för persondatorer. Dessa specifikationer var upphovsrättsskyddade 1981 och var ett registrerat varumärke som tillhör Software Arts Products Corp.

## DIF-filformat ##

DIF lagrar kalkylbladsinnehåll i ASCII-textfil som gör att det kan visas och redigeras med en textredigerare. Formatet äger sin plats i listan över dataserialiseringsformat för dess egenskaper för datautbyte. En DIF-fil består av 2 sektioner; en rubrik och data.

Allt i DIF representeras av en 2- eller 3-radsbit. Rubriker får en 3-rads bit; data, 2.

* Rubrikbitar börjar med en textidentifierare som består av versaler, endast alfabetiska tecken och mindre än 32 bokstäver. Följande rad måste vara ett par siffror och den tredje raden måste vara en sträng med citattecken.
* Databitar börjar med ett nummerpar och nästa rad är en sträng med citattecken eller ett nyckelord.

### Värden ###

Ett värde upptar två rader, den första ett par siffror och den andra antingen en sträng eller ett nyckelord. Den första siffran i paret anger typ:

* −1 – direktivtyp, den andra siffran ignoreras, följande rad är ett av dessa nyckelord:
** BOT – början av tuppel (början av raden)
** EOD – slut på data
* 0 – numerisk typ, värde är det andra talet, följande rad är ett av dessa nyckelord:
** V – giltigt
** NA – ej tillgänglig
** FEL – fel
** TRUE – sant booleskt värde
** FALSK – falskt booleskt värde
* 1 – strängtyp, det andra numret ignoreras, följande rad är strängen inom dubbla citattecken

### DIF Header chunk ###

Rubrikbiten i en DIF-fil består av en identifierarrad följt av de två raderna i ett värde. De numeriska värdena i rubrikbitar använder bara en tom sträng istället för giltighetsnyckelorden. Detaljerna för dessa rubrikbitar är som följer.

* TABELL - ett numeriskt värde följer av versionen, den andra raden som inte används i värdet innehåller en generatorkommentar
* VEKTORER - antalet kolumner följer som ett numeriskt värde
* TUPLAR - antalet rader följer som ett numeriskt värde
* DATA - efter ett numeriskt dummyvärde 0 följer tabellens data, varje rad föregås av ett BOT-värde, hela tabellen avslutas med ett EOD-värde

### DIF Exempel ###

Följande exempel visar innehållet i ett enkelt kalkylblad och dess motsvarande DIF-representation.


|Namn|Ålder
---|---|
|Bob|34
|Sheetal|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Referenser ##

* [ DIF - av Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)

