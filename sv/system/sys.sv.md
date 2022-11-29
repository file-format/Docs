{
  "date" : "2021-07-08",
  "keywords" :[ "SYS", "tillägg", "fil", "format", "system", "drivrutin", "systemfil", "program", "dator", "applikation" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Systemfilformat",
  "description":"Läs mer om SYS-filformat och API:er som kan skapa och öppna SYS-filer.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Vad är SYS fil? ##

SYS-filerna är "Systemfiler" som används i Windows OS och MS-DOS-applikationer. Dessa filer kan inte öppnas direkt och består av drivrutinen och enhetens konfiguration. SYS-filerna är ansvariga för att innehålla filer med kärnfunktioner i operativsystemet. Dessa anses vara kritiska filer för enhetsföraren och kan också användas när alla problem med racerföraren ska lösas. Dessa är ansvariga för att ett datorsystem fungerar korrekt och .sys-filerna måste vara korrekta och fullständiga.


## Teknisk specifikation ##

.sys-filerna är faktiskt en delmängd av formatet [BMP](/sv/image/bmp) eftersom det bara tillåter specifika kombinationer. Det vanliga formatet för dessa filer är som LOGOS.SYS, LOGOW.SYS och LOGO.SYS. Andra filer har inte detta format.

Dessa filer används oftast i katalogen *C* i Windows vid installationstillfället. De flesta problem som kretsar kring drivrutiner löses genom att uppdatera Windows OS. Detaljerna och informationen om dessa filer kan ses med hjälp av de inbyggda programmen i Windows OS. Dessa omfattar även referenserna till olika moduler i ett operativsystem.
Några av exemplen på systemfiler är:

* IO.SYS (Dessa lagrar drivrutiner för diskoperativsystem)
* MSDOS.SYS (Dessa innehåller kärnan eller operativsystemets kärnkod)
* CONFIG.SYS (dessa innehåller olika konfigurationsalternativ)
* KEYBOARD.SYS (Dessa innehåller information om tangentbordslayout)
* COUNTRY.SYS (Dessa innehåller land- och teckentabellsrelaterad information)

## SYS-filformat ##

Microsoft utvecklade filerna med .sys-tillägg. Variabler och funktioner ingår i SYS-filer. Dessa används mest av Microsofts operativsystem. Dessa filer finns huvudsakligen i rotkatalogen på disken:

* C:\Windows\system32\drivrutiner
* C:\Windows\WinSxS

Några vanliga varningar om SYS-filer är följande:

* Namnen på dessa filer bör inte ändras eftersom dessa filer är ansvariga för kärnfunktioner och variabler i operativsystemet
* Dessa filer bör inte raderas eftersom deras frånvaro av dessa filer kan orsaka fel
* .sys-filerna ska inte laddas ner från internet förrän du är säker på källans legitimitet
* Man bör inte bråka med dessa filer eftersom att ändra dem eller bråka med dessa orsakar allvarliga systemfel
* Om dessa filer skadas av något virus eller skadlig programvara bör dessa installeras om

## SYS Exempel ##

Följande är ett exempel på en enkel SYS-systemkonfigurationsfil:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
