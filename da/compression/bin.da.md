{
   "date":"2023-07-20",
   "keywords":[
"BEHOLDER",
"BIN fil",
"fil",
"BIN filtypenavn",
"udvidelse",
"fil"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"BIN-filformat - MacBinary-kodet fil",
   "description":"Lær om BIN-format og API'er, der kan oprette og åbne BIN-filer.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin-da",
         "parent":"compression"
}
},
   "lastmod":"2023-07-20"
}

## Hvad er en BIN fil?

En BIN-fil, i sammenhæng med Macintosh-computere, kan henvise til en fil, der er gemt i MacBinary-formatet. MacBinary er et filformat, der er specielt designet til at overføre Macintosh-filer over internettet, e-mail, FTP eller bærbare medier. Formålet med MacBinary er at bevare den komplette filstruktur og attributter for Macintosh-filer, inklusive både datagaffel og ressourcegaffel, i en enkelt fil.

MacBinary-formatet opnår dette ved at indkapsle Macintosh Hierarchical File System (HFS) ressourcegaffel og datagaffel i en komprimeret fil. Det inkluderer også en finder-header, der indeholder vigtige metadata om filen. Ved at kombinere alle disse komponenter i én fil sikrer MacBinary, at filen bevarer sin integritet og nemt kan overføres og deles på tværs af forskellige platforme.

Med fremskridt i Apples filsystemer og filoverførselsprotokoller er brugen af BIN-filer og MacBinary-format blevet mindre almindelig. Introduktionen af filformater som ZIP og overgangen til mere moderne filsystemer, såsom HFS+ og APFS, har reduceret behovet for MacBinary-kodede filer. Disse nyere filsystemer giver mere effektive måder at håndtere filattributter, ressourcegafler og datagafler på, hvilket gør MacBinary-formatet mindre nødvendigt i nutidens computerlandskab.

## BIN-filformat - flere oplysninger 

I de tidlige dage af Macintosh-computere blev filer gemt i to separate gafler på grund af databegrænsninger. Ressourceforken indeholdt strukturerede data, mens datagaffelen indeholdt ustrukturerede data. Mens Classic Mac OS behandlede disse gafler som en enkelt fil, resulterede overførsel af filer til ikke-Mac-systemer i datatab, fordi de ikke genkendte gaflerne som en enkelt enhed. For at løse dette blev MacBinary-formatet skabt af personer som Dennis Brothers, Harry Chesley og Yves Lempereur. MacBinary komprimerede og kombinerede gaflerne til en enkelt fil, kendt som en BIN-fil, til overførsel til ikke-Mac-systemer. Ved tilbagevenden til Mac OS ville gaflerne blive adskilt igen. Med overgangen væk fra den gaffelbaserede HFS i 2000'erne, faldt brugen af MacBinary-format markant. I dag er det sjældent at støde på en MacBinary-kodet BIN-fil, medmindre du støder på en gammel fil på et ikke-Mac-system eller downloader en fra internettet.

The MacBinary format has gone through several versions over time to accommodate changes in Macintosh systems and file handling. Here are some of the different versions of the MacBinary format:

- **MacBinary I:** Den første version af MacBinary, introduceret i slutningen af 1980'erne. Den kombinerede ressourcegaffel og datagaffel til en enkelt binær fil, hvilket muliggjorde overførsel af Macintosh-filer på tværs af platforme.

- **MacBinary II:** Denne version, udgivet i begyndelsen af 1990'erne, forbedrede det originale MacBinary-format ved at tilføje yderligere oplysninger, såsom filtype og skaberkoder, til den binære fils header. Disse koder hjalp med at opretholde integriteten og identifikationen af Macintosh-filer under overførsel.

- **MacBinary III:** The MacBinary III format, introduced in the mid-1990s, further enhanced the previous versions by including additional metadata, such as file name and file creation and modification dates, in the binary file's header. This allowed for more comprehensive preservation of Macintosh file attributes during transfer.

- **MacBinary IV:** MacBinary IV blev udviklet til at løse kompatibilitetsproblemer med det nye Mac OS X-operativsystem i begyndelsen af 2000'erne. Det inkorporerede ændringer for at tilpasse sig den nye filsystemstruktur og attributter introduceret i Mac OS X.

## Hvordan åbner jeg en BIN fil?

De MacBinary Encoded BIN-filer kan åbnes ved hjælp af forskellige komprimeringsværktøjer. For macOS-brugere er **Apple Archive Utility** en passende mulighed. Windows-brugere kan bruge software som **Smith Micro StuffIt Deluxe** til at udtrække indholdet af en MacBinary Encoded BIN-fil. En anden mulighed for macOS-brugere er **The Unarchiver**, som er et alsidigt værktøj, der kan håndtere flere filformater, inklusive MacBinary.

Det er vigtigt at bemærke, at filtypen .bin bruges af forskellige filformater, ikke kun MacBinary. Derfor, hvis du støder på en BIN-fil, der ikke kan åbnes med de førnævnte hjælpeprogrammer, kan den blive gemt i et andet format. I sådanne tilfælde skal du muligvis identificere det specifikke filformat og bruge den passende software eller værktøj designet til det pågældende format for at få adgang til filindholdet.

## Hvad er Macbinary Archive?

Et MacBinary-arkiv er et filformat designet til tidlige Macintosh-computere, der adresserer den dobbelte gaffelstruktur af Macintosh-filer. Macintosh-filsystemer består af en datagaffel og en ressourcegaffel, der holder data og metadata adskilt. For at lette tværsystemkompatibilitet og netværksoverførsler koder MacBinary begge gafler til en enkelt binær fil. Dette format bevarer integriteten af data og tilknyttede ressourcer under overførsler til ikke-Macintosh-systemer.

## Kan jeg slette Macbinary-arkiv?

Ja, du kan slette MacBinary-arkivfiler, hvis du ikke længere har brug for dem, eller hvis du har udtrukket indholdet og gemt dem i et andet format. MacBinary-arkiver er simpelthen en metode til at pakke Macintosh-filer til specifikke formål som overførsel på tværs af systemer eller lagring. Sletning af arkivet påvirker ikke filerne i det.

## Hvordan åbner man Macbinary-arkiv på iPhone?

Åbning af et MacBinary-arkiv på en iPhone kan kræve brug af tredjepartsapps, da iOS ikke har indbygget understøttelse af dette format.

## Macbinary Archive Extract - Hvordan udpakkes Macintosh Bin-filer?

For at udpakke MacBinary (bin) filer på en moderne computer, bruger du typisk et filudtræksværktøj eller software, der understøtter dette format.

På Windows skal du bruge et filarkiveringsværktøj, der understøtter MacBinary-filer. Populære muligheder inkluderer WinRAR, 7-Zip eller WinZip.

Mac OS kommer med et indbygget arkivværktøj, der kan håndtere forskellige arkivformater, inklusive MacBinary. Find MacBinary-filen i Finder. Dobbeltklik på MacBinary-filen. Arkivværktøjet bør automatisk starte og udpakke indholdet. Når udpakningen er fuldført, kan du finde de udpakkede filer på samme placering som den originale MacBinary-fil eller på en bestemt destination.

## Andre BIN-filer

Her er andre filtyper, der bruger filtypen **.bin**.

- [BIN - Binary Disc Image File](/disc-and-media/bin/)
- [BIN - Unix Executable File](/executable/bin/)
- [BIN - BlackBerry IT Policy File](/settings/bin/)
- [BIN - Sega Genesis Game ROM](/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/game/bin-pcsx/)

## Referencer

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)


