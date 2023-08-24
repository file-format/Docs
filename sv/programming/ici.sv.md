{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "fil", "tillägg", "filformat", "ICI-implementering", "Programmeringsguide", "ici-exempel", "ICI-programmeringsspråk", "moduler av ICI", "datamodell för ICI ", "dokumentation av ICI", "ICI-språk" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - Programmeringsspråkfil",
  "description":"Läs mer om ICI-filformat och API:er som kan skapa och öppna ICI-filer.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## Vad är ICI fil?

Ett allmänt programmeringsspråk som tolkas och innehåller flera funktioner såsom dynamisk typning tillsammans med de flexibla datatyperna är känt som ICI (inte en akronym) programmeringsspråk. Det anses likna språket [Perl](/sv/programming/pl/). Detta ICI-språk omfattar flödeskontrollkonstruktioner och innehåller även några operatorer för C-språket. Det är inte ett objektorienterat språk men några av funktionerna i OOP kan uppnås med en specifik nedärvningsmetod som kallas överbyggnader. I likhet med [C](/sv/programming/c) har detta ICI-programmeringsspråk samma systemgränssnitt och ett standardbibliotek för inbyggda funktioner.


## Kortfattad bakgrund ##

I slutet av 1980-talet utvecklades det av Tim Long som ett allmänt tolkat programmeringsspråk. De flesta funktionerna i detta språk liknar C och det kan också uppnå några av funktionerna genom att tillämpa några speciella metoder. Detta språk ägs som en allmän egendom och är tillgänglig som ett återförsäljningsbart språk och ingen är skyldig att nämna var han fick källkoden ifrån. Dokumentationen för ICI är under copyright av Canon Information System Research Australia.

## Teknisk specifikation ##

Det finns två olika datatyper som används på detta språk. Dessa två är primitiva och aggregerade datatyper. Båda dessa innehåller olika uttryck enligt deras fördefinierade sammansättning i språket. Olika moduler som kapslade och subrutiner stöds av detta språk. Eftersom vissa av dess egenskaper liknar Perl har den en strikt integration med de reguljära uttrycken.

Uppsättningar är begränsade till att vara heterogena och kapslade. Dessa uppsättningar ger stöd för vanliga setoperationer såsom Union och Intersection etc. Det används mestadels som ett språk för kärnimplementeringen av applikationer som ägs av multinationella organisationer.

Nästan alla typer av program kan skrivas på detta språk och mestadels de specifika programmen som involverar komplexa datastrukturer är skrivna i ICI-programmeringsspråket. Ansökningar kan involvera ICI-implementeringen på ett sätt som de borde skrivas i den. Funktionella delar av applikationen kan implementeras av modulerna i ICI. Språket i ICI liknar något C-språk men datamodellen för ICI är ganska högre och annorlunda med typer som ordböcker (struct), uppsättningar, dynamiska arrayer, reguljära uttryck och (riktiga) strängar.


## ICI filformat exempel ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Referens ##

* [ICI-programmeringsspråk](http://atrn.org/ici/doc/ici.html)



