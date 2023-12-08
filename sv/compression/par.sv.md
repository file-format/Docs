{
"datum":"2023-07-18",
   "keywords":[
"PAR",
"PAR-fil",
"hur man öppnar en par-fil",
"fil",
"PAR filtillägg",
"förlängning",
"fil"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"utkast":"falskt",
"toc":true,
"title":"PAR-filformat - Parchive Index File",
   "description":"Läs mer om PAR-format och API:er som kan skapa och öppna PAR-filer.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
         "parent":"compression"
}
},
"lastmod":"2023-07-18"
}

## Vad är PAR fil?

Inom Parchive (PAR)-arkiv hänvisar en .par-fil till en indexfil som innehåller en grupp paritetsvolymer eller paritetsblock. Denna indexfil används för feldetektering och återställning när en eller flera filer i arkivet försvinner eller skadas.

Ett arkivarkiv består vanligtvis av både originaldatafilerna och motsvarande paritetsvolymer. Paritetsvolymer skapas med hjälp av Reed-Solomon felkorrigeringsalgoritmer. Dessa paritetsvolymer innehåller redundant information som kan användas för att återställa de ursprungliga datafilerna.

.par-filen, även känd som en paritetsvolymuppsättning, innehåller information om strukturen och placeringen av paritetsvolymerna i arkivet. Det fungerar som ett index eller karta för återställningsprocessen. Genom att använda .par-filen kan specialiserad PAR-programvara bestämma vilka paritetsvolymer som behövs och hur de ska användas för att rekonstruera de saknade eller skadade filerna.

När en eller flera filer i Parchive-arkivet blir otillgängliga eller korrupta, kan .par-filen användas tillsammans med tillgängliga paritetsvolymer för att återställa förlorad data. PAR-programvaran läser .par-filen, identifierar de saknade eller skadade filerna och använder paritetsvolymerna för att rekonstruera dem.

## Hur öppnar man filen PAR?

För att öppna och använda .par-filer behöver du specialiserad PAR-programvara. Här är några populära programvarualternativ som kan hantera .par-filer:

- **QuickPar:** QuickPar är en mycket använd PAR-programvara för Windows. Det låter dig skapa, verifiera och reparera PAR-filer. Du kan öppna en .par-fil i QuickPar för att verifiera dess integritet eller använda den för att reparera skadade eller saknade filer i ett Parchive-arkiv.

- **MultiPar:** MultiPar är en annan populär PAR-programvara tillgänglig för Windows. Den stöder både PAR- och PAR2-filformat och tillhandahåller avancerade funktioner för att skapa, verifiera och reparera arkiv. MultiPar kan öppna .par-filer och utföra feldetektering och återställning baserat på de angivna paritetsvolymerna.

- **MacPAR deLuxe:** MacPAR deLuxe är en PAR-programvara designad speciellt för macOS. Den stöder filformaten PAR och PAR2 och ger liknande funktionalitet som QuickPar och MultiPar. MacPAR deLuxe kan öppna .par-filer och hjälpa till med att verifiera arkiv och återställa skadade eller saknade filer.

## PAR-filformat - Mer information

PAR-filformatet, vanligtvis kallat Parchive, är ett specifikt filformat som används för att skapa paritetsdata och utföra feldetektering och återställning i filarkiv. PAR-filformatet består vanligtvis av tre typer: PAR, PAR2 och PAR3.

- **PAR:** Det ursprungliga PAR-filformatet, även känt som PAR1, utvecklades av Parchive-projektet. Den inkluderar paritetsdata som genererats från de ursprungliga datafilerna. PAR-filer ger en grundläggande nivå av feldetektering och återställning men har begränsningar när det gäller felkorrigeringsmöjligheter.

- **PAR2:** PAR2 är en förbättrad version av PAR-filformatet. Den erbjuder mer avancerade felkorrigeringsfunktioner och förbättrade återställningsfunktioner. PAR2-filer används vanligtvis för att skapa paritetsdata som kan återställa förlorade eller skadade filer i ett arkiv. PAR2-filer ger bättre skydd mot datakorruption och används ofta för filarkiveringsändamål.

- **PAR3:** PAR3 är den senaste versionen av PAR-filformatet och ger ytterligare förbättringar i felkorrigering och återställning. Den erbjuder ännu högre nivåer av redundans och felkorrigeringsmöjligheter jämfört med PAR2. PAR3-filer är designade för att ge mer robusta skydds- och återställningsalternativ för data som lagras i arkiv.

Både PAR2- och PAR3-filformaten stöds brett av PAR-programvaran och erbjuder möjligheten att verifiera integriteten hos filer i ett arkiv och återställa förlorad eller skadad data. PAR- och PAR2-filer används fortfarande ofta, medan PAR3-filer gradvis börjar användas på grund av deras förbättrade felkorrigeringsmöjligheter.

## Referenser
* [Parchive](https://en.wikipedia.org/wiki/Parchive)

