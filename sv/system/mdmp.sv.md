{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MDMP-fil - Windows Minidump-filformat",
  "description":"Läs mer om MDMP-filformat och API:er som kan skapa och öppna MDMP-filer.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Vad är en MDMP fil?

En MDMP-fil är en minnesdump av ett program på Microsoft Windows som skapas när programmet stängs onormalt eller kraschar. Den innehåller information och datadumpar som kan användas för att felsöka orsaken till kraschen. MDMP-filer är tillämpliga på applikationer skapade av alla plattformar som Java, C++, .NET och andra. Förutom MDMP,

Program som kan öppna MDMP-filer inkluderar Microsoft Visual Studio Debugger.

## MDMP filformat

MDMP-filer sparas som binära filer på skiva och kan öppnas med Microsoft Visual Studio debugger. Den innehåller följande information för att hjälpa till att identifiera orsaken till kraschen.

* Detaljer om stoppmeddelandet, dess parametrar och andra data
* Lista över laddade drivrutiner
* Processorkontext (PRCB) för processorn som slutade fungera
* Processinformation och kärnkontext (EPROCESS) för processen som stoppades
* Bearbeta information och kärnkontext (ETHREAD) för tråden som stoppade
* Anropsstack i kärnläge för tråden som stoppades

Denna information hjälper till att ta reda på vad som hände, åtgärda problemet och förhindra att det händer igen.

### Analysera Minidump

Windows kräver en växlingsfil på startvolymen för att skapa en minnesdumpfil. Personsökningsfilen skapas på startvolymen och bör vara minst 2 megabyte (MB) stor. Dumpfilen skapas när ett program kraschar. Vid ett andra problem skapas en andra liten minnesdumpfil medan den föregående hålls bevarad. Namnet på dumpfilen är distinkt för att undvika överskrivning.

Windows håller en lista över alla minnesdumpfiler i mappen %SystemRoot%\Minidump. Du kan analysera MDMP-filer genom att köra dem i Visual Studio Debugger enligt listan i stegen nedan.

## Hur öppnar jag en MDMP-fil i Visual Studio?

Följande steg kan användas för att öppna en MDMP-fil i Visual Studio.

* I Visual Studio, från Arkiv-menyn, välj Öppna | Crash Dump .
* Navigera till dumpfilen du vill öppna.
* Välj Öppna.

## Referens

* [Hur man läser den lilla minnesdumpfilen som skapas av Windows om en krasch inträffar](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -fil)

