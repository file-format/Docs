{
  "date": "2019-10-11",
  "keywords": [
"asmx",
"asmx fil",
"asmx filformat",
"asmx filtype",
"fil",
"type",
"hvad er en asmx-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASMX - ASP.NET Web Service-fil",
  "description": "Lær om, hvad en ASMX-fil og API'er er, der kan oprette og åbne ASMX-filer.",
  "linktitle": "ASMX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asm-dax"
}
},
  "lastmod": "2021-06-10"
}

## Hvad er en ASMX fil?

En fil med .asmx-udvidelser er en ASP.NET Web Service-fil, der giver kommunikation mellem to objekter over internettet ved hjælp af Simple Object Access Protocol (SOAP). Den er implementeret som en tjeneste på den Windows-baserede webserver til at behandle indgående anmodninger og returnere svaret. I modsætning til [ASPX](/web/aspx/)-filer, der indeholder koden til visuel visning af ASP.NET-websider, kører ASMX-filer på serveren i baggrunden og udfører forskellige opgaver, såsom at oprette forbindelse til databasen, hente data og returnere dem i et format, hvor anmodning blev fremsat. Disse bruges specifikt til XML-webtjenester.

## ASMX filformat

ASMX-filer er i almindeligt tekstformat og kan åbnes eller redigeres i programmer som Microsoft Visual Studio eller teksteditorer. Det er et proprietært filformat fra Microsoft og har en veldefineret syntaks til oprettelse af webtjenester. Et svar fra en ASMX-fil i form af SOAP XML har følgende elementer.

 * `Envelop` - Et rodelement, der identificerer XML-dokumentet som en SOAP-meddelelse.
 * Header - Et valgfrit element, der indeholder applikationsspecifik information, såsom godkendelsesdata. Hvis Header-elementet er til stede, skal det være det første underordnede element i Envelope-elementet.
 * Body' - Indeholder SOAP-meddelelsen beregnet til modtageren.
 * Fejl - Et valgfrit element, der bruges til at angive fejlmeddelelser. Hvis Fault-elementet er til stede, skal det være et underordnet element af Body-elementet.

ASMX-filer kan skrives på .NET-sprog såsom [C#](/programming/cs/), [Visual Basic](/programming/vb/) eller JScript.

## Hvordan er ASMX anderledes end ASPX og ASCX?

ASMX-filer er anderledes end ASPX- og ASCX-filer.

 * ASPX, Active Server Pages, filer er programmeringsfiler, der er genereret ved hjælp af Microsoft ASP.NET framework, der kører på webservere. Disse gengives i klientens webbrowser, når brugeren anmoder om at få adgang til en sådan side.
 * ASCX, Active Server User Control, definerer brugerkontroller, der bruges til at definere genanvendelige kontroller på ASP.NET-websider eller hele webstedet.

## Referencer

 * [Forbruger ASMX-tjeneste](https://learn.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
 * [ASCX-brugerkontrol](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

