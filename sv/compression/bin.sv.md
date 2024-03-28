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
"title":"BIN-filformat - MacBinary-kodad fil",
   "description":"Läs mer om BIN-format och API:er som kan skapa och öppna BIN-filer.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
         "parent":"compression"
}
},
"lastmod":"2023-07-20"
}

## Vad är en BIN fil?

En BIN-fil i Macintosh-datorer kan referera till en fil som sparats i MacBinary-formatet. MacBinary är ett filformat speciellt utformat för att överföra Macintosh-filer över internet, e-post, FTP eller bärbara media. Syftet med MacBinary är att bevara hela filstrukturen och attributen för Macintosh-filer, inklusive både datagaffeln och resursgaffeln, i en enda fil.

MacBinary-formatet uppnår detta genom att kapsla in Macintosh Hierarchical File System (HFS) resursgaffel och datagaffel i en komprimerad fil. Den innehåller också ett sökhuvud som innehåller viktig metadata om filen. Genom att kombinera alla dessa komponenter till en fil säkerställer MacBinary att filen behåller sin integritet och enkelt kan överföras och delas mellan olika plattformar.

Med framstegen inom Apples filsystem och filöverföringsprotokoll har användningen av BIN-filer och MacBinary-format blivit mindre vanligt. Införandet av filformat som ZIP och övergången till mer moderna filsystem, som HFS+ och APFS, har minskat behovet av MacBinary-kodade filer. Dessa nyare filsystem ger effektivare sätt att hantera filattribut, resursgaffel och datagaffel, vilket gör MacBinary-formatet mindre nödvändigt i dagens datorlandskap.

## BIN-filformat - Mer information

I början av Macintosh-datorer lagrades filer i två separata "gafflar" på grund av databegränsningar. "Resursgaffeln" innehöll strukturerad data, medan "datagaffeln" innehöll ostrukturerad data. Medan Classic Mac OS behandlade dessa gafflar som en enda fil, resulterade överföring av filer till icke-Mac-system i dataförlust eftersom de inte kände igen gafflarna som en enda enhet. För att ta itu med detta skapades MacBinary-formatet av individer som bröderna Dennis, Harry Chesley och Yves Lempereur. MacBinary komprimerade och kombinerade gafflarna till en enda fil, känd som en BIN-fil, för överföring till icke-Mac-system. När de återvände till Mac OS skulle gafflarna separeras igen. Med övergången från gaffelbaserade HFS på 2000-talet minskade användningen av MacBinary-formatet avsevärt. Idag är det sällsynt att stöta på en MacBinary-kodad BIN-fil om du inte stöter på en gammal fil på ett icke-Mac-system eller laddar ner en från internet.

MacBinary-formatet har gått igenom flera versioner över tiden för att klara förändringar i Macintosh-system och filhantering. Här är några av de olika versionerna av MacBinary-formatet:

- **MacBinary I:** Den första versionen av MacBinary, introducerad i slutet av 1980-talet. Den kombinerade resursgaffeln och datagaffeln till en enda binär fil, vilket möjliggjorde överföring av Macintosh-filer över flera plattformar.

- **MacBinary II:** Denna version, som släpptes i början av 1990-talet, förbättrade det ursprungliga MacBinary-formatet genom att lägga till ytterligare information, såsom filtyp och skaparkoder, till den binära filens rubrik. Dessa koder bidrog till att upprätthålla integriteten och identifieringen av Macintosh-filer under överföringen.

- **MacBinary III:** MacBinary III-formatet, som introducerades i mitten av 1990-talet, förbättrade de tidigare versionerna ytterligare genom att inkludera ytterligare metadata, såsom filnamn och filskapande och ändringsdatum, i den binära filens rubrik. Detta möjliggjorde mer omfattande bevarande av Macintosh-filattribut under överföringen.

- **MacBinary IV:** MacBinary IV utvecklades för att lösa kompatibilitetsproblem med det framväxande operativsystemet Mac OS X i början av 2000-talet. Det inkorporerade ändringar för att anpassa sig till den nya filsystemstrukturen och attributen som introducerades i Mac OS X.

## Hur öppnar man filen BIN?

De MacBinary-kodade BIN-filerna kan öppnas med olika komprimeringsverktyg. För macOS-användare är **Apple Archive Utility** ett lämpligt alternativ. Windows-användare kan använda programvara som **Smith Micro StuffIt Deluxe** för att extrahera innehållet i en MacBinary-kodad BIN-fil. Ett annat alternativ för macOS-användare är **The Unarchiver**, som är ett mångsidigt verktyg som kan hantera flera filformat, inklusive MacBinary.

Det är viktigt att notera att filtillägget .bin används av olika filformat, inte bara MacBinary. Därför, om du stöter på en BIN-fil som inte kan öppnas med ovannämnda verktyg, kan den sparas i ett annat format. I sådana fall kan du behöva identifiera det specifika filformatet och använda lämplig programvara eller verktyg som utformats för det formatet för att komma åt filinnehållet.

## Andra BIN-filer

Här är andra filtyper som använder filtillägget **.bin**.

- [BIN - Binary Disc Image File](/sv/disc-and-media/bin/)
- [BIN - Unix körbar fil](/sv/executable/bin/)
- [BIN - BlackBerry IT Policy File](/sv/settings/bin/)
- [BIN - Sega Genesis Game ROM](/sv/game/bin/)
- [BIN - PSX PlayStation BIOS-bild](/sv/game/bin-pcsx/)

## Referenser

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)

