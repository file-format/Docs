{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INC filtillägg - Vad är en INC-fil?",
  "description":"Läs mer om INC Inkludera filformat och API:er som kan skapa och öppna INC-filer.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## Vad är INC fil?

En INC-fil är en include-fil som används av programvarans källkod för att referera till rubrikinformation. Det liknar filformatet [.h](/sv/programming/h/) och innehåller deklarationer, funktioner, rubriker eller makron som kan återanvändas av källkodsfiler som C++. INC-filer används av en mängd olika programmeringsspråk som C, [C++](/sv/programming/cpp/), Pascal, [PHP](/sv/programming/php/) och [Java](/sv/programming/java/). Textredigerare som Microsoft Notepad, Notepad++ och TextEdit kan användas för att öppna INC-filer.

## INC-filformat - Mer information

En INC-fil sparas som vanlig textfil med alla deklarationer inkluderade enligt deklarationssyntaxen. En INC-fil kan också referera till andra INC-filer. När den väl har skapats blir INC-filen en del av projektet och kan refereras från källfiler som C++. Det kan refereras av flera källfiler för att undvika dubbelarbete.

## INC Filinnehåll

INC-filer kan innehålla följande information.

**`Variables`** - När det gäller objektorienterad programmering (OOP), innehåller en klasshuvudfil definitioner av alla klassnivåvariabler som är tillgängliga över implementeringens källkodsfiler

**`Methods Declaration`** - Alla metoddeklarationer ingår i .h-huvudfilerna för att vara tillgängliga över flera implementeringsfiler.

**`Non-Inline Function Definitions`** - Header-filer kan också innehålla definitioner av icke-inline-metoder.

## Nackdel med att använda INC-fil i PHP

PHP är skript på serversidan som körs på servern och returnerar resultaten till de anropande webbsidorna. Om en PHP-fil refererar till en INC-fil och servern inte är konfigurerad att analysera .inc-filer (vilket är mycket vanligt), kan en användare se php-källkoden i .inc-filen genom att besöka URL-katalogen. Så man måste vara försiktig när man använder INC-filer som inkluderar filer i PHP.

## Referenser

* [Använder INC i PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

