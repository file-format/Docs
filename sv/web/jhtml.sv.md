{
  "date" : "2019-10-11",
  "keywords" :[ "jhtml","jhtml-fil", "jhtml-filformat", "jhtml-filtyp", "fil", "typ", "vad är en jhtml-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JHTML - Java HTML-fil",
  "description":"Läs mer om JHTML-filformat och API:er som kan skapa och öppna JHTML-filer.",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-09"
}

## Vad är en JHTML-fil?

En fil med filtillägget .jhtml är en [HTML](/sv/web/html/)-fil med [Java](/sv/programming/java/)-kod som körs på servern när en klient begär den här sidan i en webbläsare. Servern bearbetar förfrågningarna, utför Java-funktionerna som finns i funktionen och returnerar sidan till klientens webbläsare. Java-objekten som är inbäddade i JHTML-sidorna körs på servern för att hantera förfrågningar om sidor av denna typ. JHTML-filer kan också komma åt information från databasen med JDBC-anslutningen (Java [Databas](/sv/database/) Connectivity). JHTML-filer kan öppnas i vilken textredigerare som helst och visas i webbläsare som Google Chrome, Firefox och Safari.

## JHTML filformat

JHTML är en egenutvecklad teknologi från ATG och kan skapas med hjälp av ATG (Art Technology Group) Dynamo Document Editor. JHTML-filer skrivs i vanlig textfilformat med standard HTML- och Java-kod. Dessa innehåller vanliga HTML-taggar utöver egna taggar som refererar till Java-objekt. När en sådan sida efterfrågas av användaren vidarebefordrar HTTP-servern begäran till en Java-applikationsserver. JHTML-sidan konverteras först till en .java-fil och kompileras för att generera en [.class](/sv/programming/class/)-fil som exekveras som en servlet. Detta genererar en ström av standard HTTP- och HTML-data som returneras till den begärda webbläsaren för visning för användaren. Detta är användbart för att köra databasrelaterade frågor på servern och returnera det slutförda ackumulerade resultatet till klientens webbläsare.

## Referenser

* [The Global Structure of HTML-dokument](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

