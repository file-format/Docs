{
  "date" : "2021-07-12",
  "keywords" :[ "cmd-fil", "vad är en cmd-fil", "fil", "cmd-exempel", "cmd-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om CMD-filformat och API:er som kan skapa och öppna CMD-filer.",
  "title" :"CMD - Windows Command File Format",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## Vad är en CMD fil?
En CMD-fil består av ett skript som innehåller ett eller flera kommandon i form av ren text som körs för att utföra olika uppgifter. Den liknar en [BAT](/sv/executable/bat/)-fil, som också vanligtvis används för att lagra en grupp körbara kommandon. CMD-filerna används ofta i operativsystemet Microsoft Windows. Dessa filer introducerades på nästan 90-talet men används fortfarande i det senaste Windows-operativsystemet. Dessa filer är vanligtvis skrivna för att utföra mer än ett kommando i en sekvens.

## CMD-filformat
CMD är ett filformat som används av körbara program i CP/M-stil. Det är i allmänhet jämförbart med [COM](/sv/executable/com/) i CP/M-80 och [EXE](/sv/executable/exe/) i DOS. En CMD-fil innehåller 1 till 8 grupper av kod eller data och en 128-byte header. Varje grupp kan vara upp till 1 mb stor. CMD-filer kan också innehålla omlokaliseringsinformation och Resident System Extensions (RSX) i senare versioner. CMD är en nykomling jämfört med [BAT](/sv/executable/bat/)-fil; används för MS-DOS före lanseringen av Windows i MS-DOS. Även om du fortfarande kan spara filer med tillägget .bat idag, använder många människor tillägget .cmd för att spara sina körbara skript.

### CMD-formatspecifikation

Början av rubriken innehåller listan över de grupper som finns i filen tillsammans med deras typer. Varje typ kan användas högst en gång. Dessa typer är:

- Kod
- Data
- Extra
- Stack
- Användare 1
- Användare 2
- Användare 3
- Användare 4
- Delad kod

På samma sätt Program Segment Prefix i DOS, de första 256 byten i datagruppen är noll. De kommer att fyllas i av CP/M-86 med nollsidan. Om det inte finns någon datagrupp kommer de första 256 byten av kodgruppen att användas istället.
## Exempel på CMD-fil
Följande är ett exempel på ett CMD-skript för att visa systeminformation.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Referenser

* [Hur man skriver ett CMD-skript](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [CMD-fil (CP/M) - av Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

