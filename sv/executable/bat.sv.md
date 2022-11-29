{
  "date" : "2021-06-24",
  "keywords" :[ "bat-fil", "vad är en bat-fil", "fil", "exempel på bat-fil", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om BAT-filformat och API:er som kan skapa och öppna BAT-filer.",
  "title" :"BAT - Batch File Format",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## Vad är en BAT fil?
En BAT-fil är känd som en batchfil som körs med DOS och alla versioner av Windows, under cmd.exe. Den består av en serie radkommandon i vanlig text som ska utföras av kommandoradstolken för att utföra olika uppgifter, som att köra underhållsverktyg i Windows eller starta typiska program. En batchfil kan innehålla vilket kommando som helst som kan accepteras av tolken interaktivt och använda kodstrukturen som möjliggör villkorlig förgrening och looping som skrivs i batchfilen.
## BAT filformat
Ett BAT-filformat är helt enkelt ett skript som är inbyggt för att automatisera kommandosekvenser som är repetitiva till sin natur. Termen "batch" används för batchbearbetning, det kan betraktas som "icke-interaktiv exekvering". Därför kanske en batchfil inte bearbetar en batch med flera data. I det gamla diskoperativsystemet (DOS) kördes batchfilen under kommandoradsgränssnittet genom att skriva in filnamnet och filtillägget .bat. Det tidigare Microsofts grafiska gränssnittsbaserade operativsystemet som Microsoft Windows var beroende av DOS. Användarna var tvungna att använda DOS för att utföra typiska operationer som att reparera, optimera eller ominstallera Windows. Senare introducerade Microsoft Windows NT som inte var beroende av DOS-operativsystemet. Därför kan batchfilerna köras genom att använda kommandotolken eller **cmd.exe** i dagens Microsofts operativsystem.
### Batchfilparametrar
Kommandotolken stöder ett antal specialvariabler som **%0, %1 till %9** för att referera till namnet och sökvägen till batchjobbet och de nio anropsparametrarna från batchjobbet. Icke-existerande parametrar ersätts av en sträng med noll längd. Även om de kan användas på samma sätt som miljövariabler, men sparas inte i miljön. Microsoft och IBM hänvisar till dessa variabler som ersättningsparametrar, medan Novell, Digital Research och Caldera introducerade termen ersättningsvariabler för dem.

Här är några användbara batchfilkommandon:
| Kommando | Beskrivning |
------|------------|
| VER | Det här batchkommandot visar vilken version av MS-DOS du använder. |
|ASSOC| Detta är ett batch-kommando som associerar ett tillägg med en filtyp (FTYPE), visar befintliga associationer eller tar bort en association. |
|CD| Detta batchkommando hjälper till att göra ändringar i en annan katalog, eller visar den aktuella katalogen. |
|CLS| Detta batchkommando rensar skärmen. |
|KOPIERA| Detta batch-kommando används för att kopiera filer från en plats till en annan. |
|DEL| Detta batchkommando tar bort filer och inte kataloger. |
|DIR| Detta batch-kommando listar innehållet i en katalog. |
|DATUM| Detta batchkommando hjälper till att hitta systemdatumet. |
|EKO| Detta batch-kommando visar meddelanden eller slår på eller av kommandoeko. |
|AVSLUTA| Detta batchkommando avslutar DOS-konsolen. |
|MD| Detta batchkommando skapar en ny katalog på den aktuella platsen. |
|FLYTTA| Detta batch-kommando flyttar filer eller kataloger mellan kataloger. |
|PATH| Detta batchkommando visar eller ställer in sökvägsvariabeln. |
|PAUS| Detta batchkommando frågar användaren och väntar på att en rad med inmatning ska matas in. |
|FRÅGA| Det här batchkommandot kan användas för att ändra eller återställa cmd.exe-prompten. |
|RD| Detta batchkommando tar bort kataloger, men katalogerna måste vara tomma innan de kan tas bort. |
|REN| Byter namn på filer och kataloger |
|REM| Detta batchkommando används för anmärkningar i batchfiler, vilket förhindrar att innehållet i anmärkningen exekveras. |
|START| Detta batchkommando startar ett program i ett nytt fönster eller öppnar ett dokument. |
|TID| Detta batch-kommando ställer in eller visar tiden. |
|TYP| Detta batch-kommando skriver ut innehållet i en fil eller filer till utgången. |
|VOL| Detta batch-kommando visar volymetiketterna. |
|ATTRIB| Visar eller ställer in attributen för filerna i den aktuella katalogen |
|CHKDSK| Detta batchkommando kontrollerar disken för eventuella problem. |
|VAL| Detta batch-kommando ger användaren en lista med alternativ. |
|CMD| Detta batchkommando anropar en annan instans av kommandotolken. |
|KOMP| Detta batchkommando jämför 2 filer baserat på filstorleken. |
|KONVERTERA| Detta batchkommando konverterar en volym från FAT16- eller FAT32-filsystem till NTFS-filsystem. |
|DRIVERQUERY| Detta batchkommando visar alla installerade drivrutiner och deras egenskaper. |
|EXPANDA| Det här batchkommandot extraherar filer från komprimerade .cab-kabinettfiler. |
|HITTA| Det här batchkommandot söker efter en sträng i filer eller indata och matar ut matchande rader. |
|FORMAT| Det här batchkommandot formaterar en disk för att använda Windows-stödda filsystem som FAT, FAT32 eller NTFS, och skriver därmed över det tidigare innehållet på disken. |
|HJÄLP| Detta batch-kommando visar listan över Windows-levererade kommandon. |
|IPCONFIG| Det här batchkommandot visar Windows IP-konfiguration. Visar konfiguration efter anslutning och namnet på den anslutningen. |
|LABEL| Detta batchkommando lägger till, ställer in eller tar bort en disketikett. |
|MER| Detta batch-kommando visar innehållet i en fil eller filer, en skärm i taget. |
|NET| Tillhandahåller olika nätverkstjänster, beroende på vilket kommando som används. |
|PING| Detta batchkommando skickar ICMP/IP "eko"-paket över nätverket till den angivna adressen. |
|STÄNGNING| Detta batchkommando stänger av en dator eller loggar ut den aktuella användaren. |
|SORTERA| Detta batch-kommando tar indata från en källfil och sorterar dess innehåll alfabetiskt, från A till Ö eller Ö till A. Det skriver ut utdata på konsolen. |
|SUBST| Detta batchkommando tilldelar en enhetsbeteckning till en lokal mapp, visar aktuella tilldelningar eller tar bort en tilldelning. |
|SYSTEMINFO| Detta batchkommando visar konfigurationen av en dator och dess operativsystem. |
|TASKKILL| Detta batchkommando avslutar en eller flera uppgifter. |
|UPPGIFTSLISTA| Detta batch-kommando listar uppgifter, inklusive uppgiftsnamn och process-id (PID). |
|XCOPY| Detta batchkommando kopierar filer och kataloger på ett mer avancerat sätt. |
|TRÄD| Detta batchkommando visar ett träd med alla underkataloger i den aktuella katalogen till valfri nivå av rekursion eller djup. |
|FC |Detta batchkommando listar de faktiska skillnaderna mellan två filer. |
|DISKPART |Detta batchkommando visar och konfigurerar egenskaperna för diskpartitioner. |
|TITLE |Detta batchkommando ställer in titeln som visas i konsolfönstret. |
|SET | Visar listan över miljövariabler på det aktuella systemet. |

## Exempel på BAT-fil
Batch-skript sparas vanligtvis som enkla textfiler; som innehåller kommandon som exekveras i en sekvens. Dessa filer sparas med tillägget .bat; igenkänns och körs med hjälp av programvaran **Command Interpreter**. Denna programvara är inbyggd tillgänglig i Microsoft Windows med namnet **cmd.exe**.

Här är ett exempel på batchskript som tar bort alla filer i den aktuella katalogen:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Referenser

* [Batch Script - Quick Guide](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [Batchfil - av Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

