{
  "date" : "2021-05-25",
  "keywords" :[ "DML","DML-fil", "DML-filformat", "DML-filtyp", "fil", "typ", "vad är en DML-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML - DynaScript HTML-fil",
  "description":"Läs mer om DML-filformat och API:er som kan skapa och öppna DML-filer.",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## Vad är en DML fil?

En fil med filtillägget .dml är en kodfil för webbskriptsidor som skapats med DyanScript. DynaScript är ett dynamiskt [HTML](/sv/web/html/) skriptspråk som är kompatibelt med ECMAScript och ger de flesta av samma funktioner som andra skriptspråk. Det liknar ColdFusion-kod och Microsoft Active Server Pages (ASP)-kod. DML-filer kan öppnas och visas i vanliga webbläsare som liknar andra HTML-sidor.

## DML filformat

DML-filer skapas i vanligt textfilformat och kan öppnas med en textredigerare för att se koden. Kodskrivning med DML-skriptspråk kan användas för att dynamiskt generera HTML på DML-sidor på serversidan. DynaScripts är byggda från följande språkelement:


* SCRIPT-tagg - Dessa är inbäddade i dokument som HTML-kommentarer. En HTML-kommentar markeras med en \ <!-- tag.
* Literals - Dessa är fasta värden i DynaScript-filer. Exempel på dessa inkluderar heltal som s 123 , 0x3F , 0123, flyttal som 456.789 , 3.2e-8, Boolean som sant eller falskt och sträng som "Regnet i Spanien"
* Variabler - DynaScript-variabler behöver inte definieras eller tilldela dem till en fast datatyp. En variabel måste ha ett värde innan du använder den i ett uttryck; annars genereras en körtidsvarning.
* Uttryck - Dessa är kombinationer av variabler, bokstavliga värden, operatorer och andra uttryck. Den högra sidan av en uppdragsbeskrivning är ett uttryck.
* Operatorer - Dessa fungerar på ett eller flera uttryck som kallas operander. Dessa kan vara antingen ternära, binära eller unära: ternära operatorer agerar på tre uttryck, binära operatorer agerar på två uttryck och unära operatorer agerar på ett.
* Uttalanden - Dessa styr skriptflöden, manipulerar objekt och allmän programmering. I allmänhet följer dessa påståenden standard C och Java-syntax. Exempel är if-else, do-while loops, switch, break, continue, etc. som alla andra skriptspråk.
* Funktioner - Funktioner, precis som alla andra skriptspråk, låter dig kapsla in en uppsättning instruktioner en gång i ett dokument som en funktion och sedan använda den flera gånger genom hela dokumentet (genom att anropa funktionen). DynaScript stöder också funktioner.
* Objekt - DynaScript är objektorienterat och stöder "objekt" och de grundläggande objektorienterade begreppen inkapsling, polymorfism och arv.

