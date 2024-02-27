{
  "date": "2019-10-11",
  "keywords": [
"jhtml",
"jhtml fil",
"jhtml filformat",
"jhtml filtype",
"fil",
"type",
"hvad er en jhtml-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JHTML - Java HTML-fil",
  "description": "Lær om JHTML-filformat og API'er, der kan oprette og åbne JHTML-filer.",
  "linktitle": "JHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-jhtm-dal"
}
},
  "lastmod": "2021-06-09"
}

## Hvad er en JHTML fil?

En fil med filtypen .jhtml er en [HTML](/web/html/)-fil med [Java](/programming/java/)-kode, der udføres på serveren, når en klient anmoder om denne side i en browser. Serveren behandler anmodningerne, udfører Java-funktionerne i funktionen og returnerer siden til klientens browser. Java-objekterne, der er indlejret i JHTML-siderne, kører på serveren for at håndtere anmodninger om sider af denne type. JHTML-filer kan også få adgang til oplysninger fra databasen ved hjælp af JDBC-forbindelsen (Java [Database](/database/) Connectivity). JHTML-filer kan åbnes i enhver teksteditor og ses i webbrowsere som Google Chrome, Firefox og Safari.

## JHTML filformat

JHTML er en proprietær teknologi af ATG og kan oprettes ved hjælp af ATG (Art Technology Group) Dynamo Document Editor. JHTML-filer er skrevet i almindeligt tekstfilformat ved hjælp af standard HTML- og Java-kode. Disse indeholder standard HTML-tags ud over proprietære tags, der refererer til Java-objekter. Når en sådan side anmodes af brugeren, videresender HTTP-serveren anmodningen til en Java-applikationsserver. JHTML-siden konverteres først til .java-filen og kompileres til at generere en [.class](/programming/class/)-fil, der udføres som en servlet. Dette genererer en strøm af standard HTTP- og HTML-data, der returneres tilbage til den anmodende browser til visning for brugeren. Dette er nyttigt til at køre databaserelaterede forespørgsler på serveren og returnere det endelige akkumulerede resultat til klientens browser.

## Referencer

* [The Global Structure of HTML-dokument](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)


