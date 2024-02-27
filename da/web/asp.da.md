{
  "date": "2019-10-11",
  "keywords": [
"asp",
"asp fil",
"asp filformat",
"asp filtype",
"fil",
"type",
"hvad er en asp-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASP - Active Server Pages File Format",
  "description": "Lær om, hvad en ASP-fil og API'er er, der kan oprette og åbne dem.",
  "linktitle": "ASP",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-as-dap"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en ASP fil?

ASP står for Active Server Pages, som er en udviklingsramme til at skabe websider. Det gør det muligt at udføre computerkode af en intern server til at betjene webanmodningerne. Når en anmodning genereres for en ASP-fil af webbrowseren, læser serveren filen og udfører enhver kode/script inde i den for at generere resultatet **[HTML](/web/html/)**, som returneres til browseren til visning.

I modsætning til HTML-sider, som er statiske sider, der serveres af serveren, genererer ASP-filer dynamisk indhold under kørsel, der kan involvere anmodninger om data fra en database. ASP-sider bruger typisk .asp-udvidelsen i stedet for .html. Da kode/script inde i en ASP-fil udføres på serversiden, kan den anmodende browser ikke se den kode, der blev brugt til at bygge den serverede side. Alle moderne browsere er i stand til at vise sider genereret som resultat. Sider bygget med ASP er bygget på Microsoft-teknologi og hostes på Microsoft Internet Information Services (IIS)-servere.

## Kort historie om ASP-filformat
ASP har kun gennemgået få revisioner, og det blev afløst af ASP.NET, som er en mere moderne og mere effektiv måde at udvikle og administrere serversidesider på. Support til ASP er inkluderet som standard sammen med Internet Information Services (IIS). ASP blev udgivet i tre forskellige versioner med forbedringer i hver.

* ASP 1.0 blev udgivet i december 1996 som en del af IIS 3.0

* ASP 2.0 blev udgivet i september 1997 som en del af IIS 4.0

* ASP 3.0 blev udgivet i november 2000 som en del af IIS 5.0


## ASP funktionelle objekter

ASP-filer bruger objekter på serversiden til at behandle brugeranmodninger og generere outputsider, der skal vises til brugerne. Hvert objekt har et sæt af samlinger, egenskaber og metoder til behandling af anmodninger og svar. Disse objekter omfatter:

### Anmodningsobjekt

Når en browser beder om en side fra en server, kaldes det en anmodning. Request-objektet bruges til at få information fra en besøgende.

### Svarobjekt

ASP Response-objektet bruges til at sende output til brugeren fra serveren.

### Serverobjekt

ASP Server-objektet bruges til at få adgang til egenskaber og metoder på serveren. Det tillader forbindelser til databaser (ADO), filsystem og brug af komponenter installeret på serveren.

### Sessionsobjekt

Et sessionsobjekt er som et link mellem brugerens browser, der anmoder om en side fra serveren, og selve serveren. Dette opnås ved en cookie oprettet af ASP og sendt til brugerens computer. Sessionsobjektet gemmer information om eller ændrer indstillinger for en brugersession. Oplysninger, der er gemt i et Session-objekt, deles på tværs af alle sider i en applikation. Almindelige oplysninger gemt i sessionsvariabler er navn, id og præferencer. Serveren opretter et nyt sessionsobjekt for hver ny bruger og ødelægger sessionsobjektet, når sessionen udløber.

### Applikationsobjekt

Applikationsobjektet indeholder information, der vil blive brugt af mange sider i applikationen (såsom databaseforbindelsesoplysninger). Oplysningerne kan tilgås fra enhver side. Oplysningerne kan også ændres ét sted, og ændringerne vil automatisk blive afspejlet på alle sider. Applikationsobjektet bruges til at gemme og få adgang til variabler fra enhver side, ligesom Session-objektet.

### ASPError Object

ASPError-objektet blev implementeret i ASP 3.0 og er tilgængeligt i IIS5 og senere. ASPError-objektet bruges til at vise detaljerede oplysninger om enhver fejl, der opstår i scripts på en ASP-side.

**Bemærk:** ASPError-objektet oprettes, når Server.GetLastError kaldes, så fejlinformationen kan kun tilgås ved at bruge Server.GetLastError-metoden.

## Referencer

* [ASP - af W3C](https://www.w3schools.com/asp/default.asp)

* [Oprettelse af simple ASP-sider](https://learn.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))


