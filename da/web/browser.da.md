{
  "date" : "2023-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "BROWSER-fil - ASP.NET Browser Definition File Format",
  "description":"Lær om BROWSER filformat og API'er, der kan oprette og åbne BROWSER filer.",
  "linktitle" : "BROWSER",
  "menu" : {
    "docs" : {
      "parent" : "web",
      "identifier": "web-browse-dar"
}
},
  "lastmod" : "22023-06-06"
}

## Hvad er en BROWSER fil?

En fil med .browser-udvidelsen bruges af ASP.NET-webapplikationer til at bestemme kapaciteten og konfigurationen af webbrowsere. Den indeholder oplysninger om browserens muligheder, begrænsninger og egenskaber. Disse egenskaber hjælper ASP.NET-rammeværket til at genkende den anmodende browser og præsentere websiden for brugerne i overensstemmelse hermed.

## BROWSER Filformat

BROWSER-definitionsfiler bruges af ASP.NET-applikationen til at bestemme browserens muligheder. Det er information indeholdt i denne fil, som bruges af serveren til at generere markup og andre ressourcer, der er kompatible med den anmodende browser.

BROWSER-filer gemmes i almindeligt tekstfilformat. Du kan åbne en BROWSER-fil i teksteditorer som Notepad, Notepad++, Apple TextEdit og Visual Studio IDE.

### Filstruktur af BROWSER-filformat

BROWSER-definitionsfilerne bruger en hierarkisk struktur. Hver .browser-fil indeholder en XML-opmærkning, der inkluderer mulighederne og funktionerne i en bestemt browser eller en gruppe af browsere. Disse detaljer omfatter karakteristika såsom agentstreng, versionsnumre og understøttelse af teknologier såsom JavaScript, CSS eller andre HTML-elementer. Ved at bruge disse browserdefinitionsfiler tilpasser ASP.NET-udviklere brugeroplevelser baseret på mulighederne i forskellige browsere.

## Referencer

 * [Arbejde med filer på en ASP.NET-websider](https://learn.microsoft.com/en-us/aspnet/web-pages/overview/data/working-with-files)



