{
"datum":"2023-07-20",
   "keywords":[
"BIN",
"BIN-fil",
"fil",
"BIN filtillägg",
"förlängning",
"fil"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"utkast":"falskt",
"toc":true,
"title":"BIN-filformat - Unix-körbar fil",
   "description":"Läs mer om BIN-format och API:er som kan skapa och öppna BIN-filer.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
         "parent":"executable"
}
},
"lastmod":"2023-07-20"
}

## Vad är en BIN fil?

En BIN-fil är en körbar fil på Unix-baserade operativsystem som Linux eller FreeBSD. Den innehåller ett kompilerat program som består av binär kod härledd från källkoden, vilket gör den kompatibel med den underliggande systemarkitekturen. Unix körbara BIN-filer kan jämföras med Windows .EXE-filer och macOS .APP-filer när det gäller deras roll som körbara format.

Inom området mjukvaruutveckling för Unix-system används BIN-filer vanligtvis av utvecklare för att paketera och distribuera program. De erbjuder ett bekvämt sätt att leverera programvara till användarna, vilket möjliggör enkel installation och exekvering. Vid sidan av BIN-filer finns det andra typer av Unix-körbara filer, inklusive [.ELF](/sv/executable/elf/), .X86, [.RUN](/sv/executable/run/) och .X86_64, var och en skräddarsydd för specifik hårdvara eller Systemkrav.

När det kommer till den interna strukturen för en BIN-fil, består den av kodad data som Unix-operativsystemet använder för att identifiera, läsa och köra det bifogade programmet. Systemet förlitar sig på specifika filsignaturer eller rubriker för att känna igen BIN-filen som en körbar fil, följt av tolkningen och exekveringen av de binära instruktionerna som finns däri.

BIN-filer kommer ofta med en medföljande **INSTALL.TXT**-fil, som ger detaljerade instruktioner om hur du korrekt installerar och konfigurerar programmet. Denna dokumentation säkerställer att användare kan navigera framgångsrikt i installationsprocessen och börja använda programvaran utan komplikationer.

## Hur öppnar man filen BIN?

BIN-filer är inte utformade för att direkt öppnas och visas. Du kan dock köra programmen eller extrahera data de innehåller. För att komma åt innehållet i en BIN-fil, följ dessa steg på kommandoraden, förutsatt att namnet på BIN-filen är "sample.bin":

1. **Se till körbara behörigheter:**

Innan du kör BIN-filen, se till att den har nödvändiga behörigheter för att köras som en körbar fil. Använd kommandot:

```
$ chmod +x sample.bin
```

Detta kommando ger filen körbara privilegier.

2. **Kör BIN-filen:**

Efter att ha ställt in de körbara behörigheterna kan du köra BIN-filen genom att ange följande kommando:

```
$ ./sample.bin
```

**Varning**

_Var försiktig när du hanterar nedladdade eller mailade BIN-filer, eftersom de potentiellt kan användas av cyberbrottslingar för att distribuera skadlig programvara. Kör bara BIN-filer från pålitliga källor för att minska risken för skadliga körbara attacker._

## Andra BIN-filer

Här är andra filtyper som använder filtillägget **.bin**.

- [BIN - MacBinary-kodad fil](/sv/compression/bin/)
- [BIN - Binary Disc Image File](/sv/disc-and-media/bin/)
- [BIN - BlackBerry IT Policy File](/sv/settings/bin/)
- [BIN - Sega Genesis Game ROM](/sv/game/bin/)
- [BIN - PSX PlayStation BIOS-bild](/sv/game/bin-pcsx/)

## Referenser

* [Hur man kör binära filer i Linux](https://linuxhint.com/execute-binary-files-in-linux/)


