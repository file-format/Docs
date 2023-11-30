{
"date": "2023-06-05",
  "keywords": [
"nsp fil",
"vad är en nsp-fil",
"hur man öppnar en nsp-fil",
"vad innehåller nsp-filen",
"vilket är formatet på nsp-filen",
"fil",
"nsp filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "NSP-filformat - Nintendo Submission Package",
  "description":"Läs mer om NSP-format och API:er som kan skapa och öppna NSP-filer.",
"linktitle": "NSP",
  "menu": {
    "docs": {
      "identifier": "game-nsp",
      "parent": "game"
}
},
"lastmod": "2023-06-05"
}

## Vad är NSP fil?

NSP-filformat är i första hand associerat med Nintendo Switch-konsolen. NSP står för "Nintendo Submission Package." Det är filformat som används av Nintendo för att distribuera och installera spel, uppdateringar och DLC (nedladdningsbart innehåll) på Nintendo Switch-systemet.

NSP-filer är i huvudsak behållare som innehåller all nödvändig data och tillgångar för ett visst spel eller innehåll. Detta inkluderar körbara spel, grafik, ljud och eventuella ytterligare filer som krävs för att spelet ska köras. NSP-filer kan installeras på Nintendo Switch på olika sätt, inklusive officiell Nintendo eShop eller anpassad mjukvara för hembryggning.

NSP-filer är vanligtvis krypterade eller signerade med digital signatur för att förhindra otillåten distribution eller manipulering. Detta säkerställer att endast legitima kopior av spel eller innehåll kan installeras och köras på Nintendo Switch-konsolen.

## Hur öppnar man filen NSP?

NSP-filer är designade för att installeras och köras på Nintendo Switch-konsolen, så de kan inte direkt öppnas eller köras på dator eller andra enheter utan lämplig mjukvara eller hårdvaraemulering.

Det finns dock få mjukvaruverktyg och verktyg tillgängliga som kan hantera NSP-filer för olika ändamål, som att extrahera eller manipulera innehåll i filer. Här är några exempel:

- **Hactool:** Hactool är kommandoradsverktyg som låter dig se innehållet i NSP-filer, extrahera enskilda filer eller dekryptera/kryptera filer. Det används främst för utveckling av hembryggning eller forskningsändamål.
- **NUT:** NUT är ett verktyg för grafiskt användargränssnitt (GUI) byggt ovanpå Hactool. Det ger ett mer användarvänligt gränssnitt för att hantera NSP-filer, inklusive möjligheten att extrahera filer, visa metadata och hantera uppdateringar och DLC.
- **Tinfoil:** Tinfoil är ett hembryggt program för Nintendo Switch som kan installera NSP-filer från olika källor, inklusive USB, SD-kort eller nätverk. Den har också funktioner som titelhantering, firmwareuppdateringar och mer.

## Vad innehåller NSP-filen?

NSP-filen (Nintendo Submission Package) innehåller vanligtvis följande komponenter:

- **Game Executable:** NSP-filen innehåller den huvudsakliga körbara filen för spelet, som är ansvarig för att köra spelet på Nintendo Switch-konsolen.
- **Speltillgångar:** Detta inkluderar olika filer som grafik, ljud, videor och andra medietillgångar som krävs för spelets bilder och ljudeffekter.
- **Metadata:** NSP-filen innehåller metadatainformation om spelet som dess titel, versionsnummer, utgivare, releasedatum, språk som stöds och annan relevant information.
- **Speldata:** NSP-filer lagrar även speldata, inklusive sparade spelfiler, konfigurationsinställningar och eventuella ytterligare filer som krävs för att spelet ska fungera korrekt.
- **DLC (nedladdningsbart innehåll):** Om NSP-filen innehåller DLC kommer den att innehålla ytterligare innehåll som kan läggas till basspelet. Detta kan inkludera nya nivåer, karaktärer, föremål eller andra funktioner som utökar spelupplevelsen.
- **Uppdateringar och patchar:** NSP-filer kan innehålla uppdateringar eller patchar till spel, som kan ge buggfixar, prestandaförbättringar, nya funktioner eller andra förbättringar av originalspelet.

## Vilket är formatet på NSP-filen?

NSP-filformatet som används av Nintendo för Nintendo Switch-konsolen är ett containerformat. Det är i huvudsak ett paket som innehåller flera filer och data relaterade till spel eller innehåll. NSP-filformatet följer specifik struktur och organisation för att säkerställa kompatibilitet och korrekt installation på Nintendo Switch-systemet.

NSP-filformatet är inte offentligt dokumenterat av Nintendo, eftersom det är proprietärt och avsett att användas med deras officiella mjukvara och hårdvara. Genom omvänd ingenjörskonst och analys av homebrew-gemenskapen har vissa detaljer om NSP-formatet upptäckts.

Strukturen för NSP-filen inkluderar vanligtvis:

- **Rubrik:** NSP-filen börjar med en rubriksektion som innehåller information om filen såsom filformatversion, storlek och krypteringsdetaljer (om tillämpligt).
- **Filsystemmetadata:** Det här avsnittet innehåller metadata relaterade till filsystemstrukturen i NSP-filen. Den definierar katalogstruktur, filnamn och attribut.
- **Innehållsfiler:** Huvuddelen av NSP-filen innehåller faktiska innehållsfiler, inklusive spelexekverbara filer, tillgångar, datafiler, DLC och uppdateringar. Dessa filer är vanligtvis komprimerade eller krypterade för att förhindra obehörig åtkomst eller manipulering.
- **Biljett:** NSP-filen kan innehålla en biljett, vilket är ett digitalt certifikat som verifierar innehållets legitimitet och godkänner installationen på Nintendo Switch-konsolen.

## Referenser
* [Nintendo Switch](https://en.wikipedia.org/wiki/Nintendo_Switch)

