{
  "date": "2022-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MDMP-fil - Windows Minidump-filformat",
  "description": "Lær om MDMP-filformat og API'er, der kan oprette og åbne MDMP-filer.",
  "linktitle": "MDMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-mdm-dap"
}
},
  "lastmod": "2022-08-19"
}

## Hvad er en MDMP fil?

En MDMP-fil er et hukommelsesdump af et program på Microsoft Windows, der oprettes, når programmet lukker unormalt eller går ned. Den indeholder information og datadumps, der kan bruges til at fejlfinde årsagen til nedbruddet. MDMP-filer kan anvendes på applikationer, der er oprettet af enhver platform, såsom Java, C++, .NET og andre. Ud over MDMP,

Programmer, der kan åbne MDMP-filer, inkluderer Microsoft Visual Studio Debugger.

## MDMP filformat

MDMP-filer gemmes som binære filer på disk og kan åbnes med Microsoft Visual Studio-debugger. Den indeholder følgende oplysninger for at hjælpe med at identificere årsagen til nedbruddet.

 * Detaljer om Stop-meddelelsen, dens parametre og andre data
 * Liste over indlæste drivere
 * Processorkontekst (PRCB) for den processor, der holdt op med at fungere
 * Procesinformation og kernekontekst (EPROCESS) for den proces, der stoppede
 * Behandle information og kernekontekst (ETHREAD) for den tråd, der stoppede
 * Kernel-mode call stack for den tråd, der stoppede

Disse oplysninger hjælper med at finde ud af, hvad der skete, løse problemet og forhindre, at det sker igen.

### Analyser Minidump

Windows kræver en personsøgningsfil på opstartsdiskenheden for at oprette en hukommelsesdumpfil. Personsøgningsfilen oprettes på opstartsvolumen og skal være mindst 2 megabyte (MB) stor. Dumpfilen oprettes, når et program går ned. I tilfælde af et andet problem oprettes en anden lille hukommelsesdumpfil, mens den forrige bevares. Navnet på dumpfilen er tydeligt for at undgå overskrivning.

Windows gemmer en liste over alle hukommelsesdumpfilerne i mappen %SystemRoot%\Minidump. Du kan analysere MDMP-filer ved at køre dem i Visual Studio Debugger som angivet i nedenstående trin.

## Hvordan åbner jeg en MDMP-fil i Visual Studio?

Følgende trin kan bruges til at åbne en MDMP-fil i Visual Studio.

 * I Visual Studio, fra menuen Filer, skal du vælge Åbn | Crash Dump.
 * Naviger til den dump-fil, du vil åbne.
 * Vælg Åbn.

## Reference

* [Sådan læser du den lille hukommelsesdumpfil, der oprettes af Windows, hvis der opstår et nedbrud](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -fil)


