{
  "date" : "2023-01-16",
  "keywords" : [ "DLIS", "what is a DLIS file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lär dig mer om DLIS-filformat och API:er som kan skapa och öppna DLIS-filer.",
  "title" : "DLIS-filformat - Brunnsloggdatafil",
  "linktitle" : "DLIS",
  "menu" : {
    "docs" : {
      "identifier":"database-dlis-sv",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Vad är en DLIS fil?

Filformatet .dlis är ett standardfilformat för lagring och utbyte av brunnsloggdata inom olje- och gasindustrin. Formatet har utvecklats av LIDS-kommittén (Logging Industry Data Standard) och det står för Digital Log Information Standard. Formatet är utformat för att lagra brunnsloggdata på ett sätt som är lätt att läsa, skriva och utbyta mellan olika system.

DLIS-filer innehåller en uppsättning logiska poster som beskriver brunnsloggdata och dess egenskaper, såsom typen av loggdata (t.ex. resistivitet, gammastrålning), mätenheterna och platsen för data i brunnen. Den faktiska loggdatan lagras i separata binära filer och refereras av de logiska posterna i DLIS-filen.

## Kort information om brunnsloggdata

Brunnsloggdata är en registrering av mätningar gjorda på olika djup i en brunn, vanligtvis under borrningsprocessen eller efter att brunnen har borrats. Dessa mätningar kan innefatta olika fysikaliska, kemiska och/eller geofysiska egenskaper hos berget och vätskorna i brunnen. Några exempel på brunnsloggdata inkluderar:

- Elektrisk resistivitet: ett mått på bergets förmåga att motstå flödet av en elektrisk ström
- Gammastrålning: ett mått på bergets naturliga radioaktivitet
- Porositet: ett mått på mängden öppna ytor eller porer i berget
- Sonic: ett mått på den tid det tar för en ljudvåg att färdas genom berget
- Densitet: ett mått på en stens massa per volymenhet
- Litologi: ett mått på bergarten eller formationen

Brunnsloggdata används för olika ändamål inom olje- och gasindustrin, såsom:

- Identifiera läget och kvaliteten på kolväteförande formationer
- Utvärdera produktionspotentialen för en brunn
- Planering och övervakning av färdigställande och stimulering av en brunn
- Övervaka brunnens beteende över tid

## Relation med PPDM

PPDM (Professional Petroleum Data Management) är en datahanteringsstandard för olje- och gasindustrin som tillhandahåller en gemensam datamodell för hantering av brunns- och produktionsdata. PPDM-datamodellen definierar en uppsättning standarddataobjekt och relationer som kan användas för att organisera och hantera brunnsloggdata, inklusive DLIS-data.

PPDM-datamodellen inkluderar dataobjekt för brunns- och produktionsdata, såsom brunnar, brunnshuvuden, brunnsloggar och produktionsdata. Det inkluderar också relationer mellan dessa dataobjekt, såsom relationen mellan en brunn och brunnloggarna som är associerade med den.

PPDM-datamodellen ger ett konsekvent branschstandard sätt att organisera och hantera brunnsloggdata, inklusive DLIS-data. Det tillåter olika organisationer att dela och utbyta data med hjälp av en gemensam datamodell, vilket förbättrar datakompatibiliteten och minskar kostnaderna för dataintegrering.

Att använda PPDM-datamodell och DLIS-data tillsammans gör det möjligt att lagra och hantera brunnsloggdata på ett sätt som överensstämmer med industristandarder och lättillgängligt för andra system och applikationer.


