{
  "date" : "2021-06-30",
  "keywords" :[ "exe-fil", "exe-filformat", "vad är en exe-fil", "fil", "exe-exempel", "exe-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En .exe-fil är en Microsoft Executable-fil som körs på Windows OS. Lär dig mer om EXE-filformat.",
  "title" :"Vad är en körbar EXE-fil?",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Vad är en EXE-fil?

Ordet EXE är en förkortning för **körbar**. En .exe-fil är ett program som kan köras på Microsoft Windows operativsystem. Applikationsutvecklare publicerar oftast sina program för Windows OS i körbart format som exe-filer. Det är standardfilformatet för att köra program på Windows. **Setup.exe**, **Install.exe** och **cmd.exe** är några vanliga och välbekanta namn på EXE-filer.

## EXE filformat

MS-DOS-kompilatorer introducerades med minnesmodellerna med 64K-minnesbegränsningen. Det allmänna konceptet är att ställa in olika segmentregister i x86-processorn (CS, DS, ES, SS) för att peka på de olika eller samma segmenten, och därför tillåta olika grader av åtkomst till minnet. Några specifika minnesmodeller var:

- **Tiny**: Alla minnesåtkomster är 16-bitars (segmentregister oförändrade). Producerar en .COM-fil istället för en .EXE-fil.
- **Liten**: Alla minnesåtkomster är 16-bitars (segmentregister oförändrade).
- **Kompakt**: Dataadresser inkluderar både segment och offset, laddar om DS- eller ES-registren vid åtkomst och tillåter upp till 1M data. Kodåtkomster ändrar inte CS-registret, vilket tillåter 64K kod.
- **Medium**: Kodadresser inkluderar segmentadressen, laddar om CS vid åtkomst och tillåter upp till 1M kod. Dataåtkomster ändrar inte DS- och ES-registren, vilket tillåter 64K data.
- **Large**: Både kod- och dataadresser är (segment, offset) par, som alltid laddar om segmentadresserna. Hela 1M byte minnesutrymme är tillgängligt för både kod och data.
- **Enormt**: Samma som den stora modellen, med ytterligare aritmetik som genereras av kompilatorn för att tillåta åtkomst till arrayer större än 64K.

Utvecklarna måste bestämma vilken modell som ska väljas när de skapar en exe-fil.

### Bärbart EXE-filformat

Det bärbara körbara filformatet (PE) innehåller ett antal informationsrubriker, följande är listan med rubriker:

- **DOS-rubrik**: MS-DOS-rubrik säkerställer antingen bakåtkompatibilitet eller graciös nedgång av nya filtyper.
- **PE-huvud**: Vid offset 60 (0x3C) från början av DOS-huvudet är en pekare till PE-filhuvudet
- **COFF Header**: COFF-huvudet har en del information som är användbar för en körbar fil, och en del information som är mer användbar för en objektfil.
- **PE Optional Header**: PE Optional Header inträffar direkt efter COFF-huvudet, och vissa källor visar till och med att de två rubrikerna är en del av samma struktur.
- **Sektionstabell**: Omedelbart efter PE Optional Header hittar vi en sektionstabell. Sektionstabellen består av en array av IMAGE_SECTION_HEADER-strukturer.
- **Mappbara sektioner**: Kan spara utrymme i minnet genom att mappa koden för ett bibliotek till mer än en process.

## Kan du köra en EXE-fil på en Mac?

Exe-filer används inte som körbara filer på Mac OS. Men om du vill köra en exe-fil på Mac OS kan följande metoder användas.

1. **Vin** - Vin är den perfekta lösningen för människor som vill använda sina PC-program på Mac-system. Det är en akronym som står för "Wine Is Not A Emulator", vilket betyder. Wine skapar samma miljö med kataloger som används av Microsoft så att du kan köra din Windows-applikation med den.
2. **Virtuella maskiner** - Skapa en virtuell Windows-maskin med Parallel Desktop eller VM Virtual Box och kör din applikation inuti den virtuella maskinen.
3. **Boot Camp** - Genom att installera och konfigurera Windows Boot Camp på Mac OS kan du köra Windows OS på en Mac-dator.

## Referenser

* [.exe- av Wikipewdia](https://en.wikipedia.org/wiki/.exe)
* [x86 Disassembly/Windows Executable Files](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

